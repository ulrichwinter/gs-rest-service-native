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
mvn  mvn clean spring-boot:build-image
docker run --rm -p 8080:8080 rest-service-complete:0.0.2-SNAPSHOT
```
