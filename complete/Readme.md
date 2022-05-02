# build sample as native app
## using gradle and buildpack

setup see: 

https://docs.spring.io/spring-native/docs/current/reference/htmlsingle/#getting-started-buildpacks

```bash
./gradlew clean bootBuildImage
docker run --rm -p 8080:8080 rest-service:0.0.1-SNAPSHOT
```
