# gradle-artifactory-plugin
## Usage
```groovy
apply from: "https://raw.githubusercontent.com/lotosbin/gradle-artifactory-plugin/master/main.gradle"
```

/build.gradle
```groovy
ext {
    GROUP_ID='xxxxx'
}
```
/gradle.propertie or ~/.gradle/gradle.properies
```properties
artifactory_contextUrl=xxxxx
artifactory_user=xxx
artifactory_password=xxxx
```
## Library Publish
```shell
./gradlew artifactoryPublish
```

### Generate POM file
```shell
./gradlew generatePomFileForAarPublication
```

## Ref
https://github.com/sky-uk/gradle-maven-plugin