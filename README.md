# gradle-artifactory-plugin
## Usage

/build.gradle
```groovy
ext {
    GROUP_ID='xxxxx'
}
```
```groovy
apply from: "${GRADLE_ARTIFACTORY_PLUGIN_URL}/main.gradle"
```

/gradle.propertie or ~/.gradle/gradle.properies
```properties
artifactory_contextUrl=xxxxx
artifactory_user=xxx
artifactory_password=xxxx
GRADLE_ARTIFACTORY_PLUGIN_URL=https://raw.githubusercontent.com/lotosbin/gradle-artifactory-plugin/master
```
## Library Publish
```shell
./gradlew artifactoryPublish
```

### Generate POM file
```shell
./gradlew generatePomFileForAarPublication
```

## other
- project name 'app' is skipped
- project dependency will handle as dependency ,ex. implementation project(':aaa') will handle as implementation '{GROUP_ID}:aaa:{currentVersion}'
- same repository has same version

## Ref
https://github.com/sky-uk/gradle-maven-plugin