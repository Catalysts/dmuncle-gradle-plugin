# dmuncle-gradle-plugin

Analyses your project and reports dependency information to a configured server.

# Usage

In your build.gradle file add the following to buildscript repositories
```
jcenter() // or mavenCentral()
maven { url "https://plugins.gradle.org/m2/" }
```

Add the following to buildscript dependencies
```
buildscript {
  dependencies {
    classpath 'cc.catalysts.gradle:cat-gradle-dmuncle-plugin:' + catGradleVersion
  }
}
```

Apply the plugin by adding this
```
apply plugin: 'cc.catalysts.dmuncle'

dmuncle {
    server = 'https://public.dmuncle.io/'
    requestTimeout = 100000
}
```
From terminal run: 
```
gradle -q dmUncleWatch
```
