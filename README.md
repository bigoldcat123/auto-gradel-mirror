## this it a tool for adding gradle mirrors

``` shell
gradle init
```

## usage
```shell
app // run this inside the root of your project
```

int the root dir run app it will add the code below to the settings.gradle.kts
, remove the mavenCentral() inside the build.gradle.kts, and change the distributionUrl inside gradle/wrapper/gradle-wrapper.properties
```kotlin
dependencyResolutionManagement {
    repositories{
        maven("https://mirrors.cloud.tencent.com/nexus/repository/maven-public/")
    }
}
pluginManagement {
    repositories{
        maven("https://maven.aliyun.com/repository/gradle-plugin")
    }
}

```