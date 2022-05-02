# build sample as native app
## using gradle and buildpacks

setup see: 

https://docs.spring.io/spring-native/docs/current/reference/htmlsingle/#getting-started-buildpacks

```bash
./gradlew clean bootBuildImage
docker run --rm -p 8080:8080 rest-service:0.0.1-SNAPSHOT
```


## using maven and buildpacks

```bash
mvn clean spring-boot:build-image
docker run --rm -p 8080:8080 rest-service-complete:0.0.2-SNAPSHOT
```

some performance measures:

* maven build time (without image): `mvn clean install`: 13 sec
* service startup time (non native): `Started RestServiceApplication in 1.234 seconds (JVM running for 1.646)`
* image build times (default setup): 03:55 min
* image build times using the "Quick Build" mode: 03:26 min 

image build time is measured as of the complete duration for `mvn clean spring-boot:build-image`
