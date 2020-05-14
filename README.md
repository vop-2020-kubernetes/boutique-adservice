**NOTE:** This repository is part of an example deployment, the original application you can find here: https://github.com/GoogleCloudPlatform/microservices-demo

This deployment has been adapted to fit our GitOps flow.
The original application has been split, creating a git repository per microservice.

Check https://github.com/vop-2020-kubernetes/boutique-ci-cd for more info about our project.




# Ad Service

The Ad service provides advertisement based on context keys. If no context keys are provided then it returns random ads.

## Building locally

The Ad service uses gradlew to compile/install/distribute. Gradle wrapper is already part of the source code. To build Ad Service, run:

```
./gradlew installDist
```
It will create executable script src/adservice/build/install/hipstershop/bin/AdService

### Upgrading gradle version
If you need to upgrade the version of gradle then run

```
./gradlew wrapper --gradle-version <new-version>
```

## Building docker image

From `src/adservice/`, run:

```
docker build ./
```

 
