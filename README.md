# java-hello-world

A barebones Java app using [Apache Maven](https://maven.apache.org/).


## Running Locally

Make sure you have [Apache Maven](https://maven.apache.org/) and [Java](https://openjdk.org/) installed.

```sh
$ git clone https://github.com/migetapp/java-hello-world.git # or clone your own fork
$ cd java-hello-world
$ mvnw --batch-mode -Dmaven.test.skip=true --no-transfer-progress package
$ java -jar target/java-hello-world-1.0.0-SNAPSHOT.jar
```
Your app should now be running on [localhost:5000](http://localhost:5000/).

## Running Locally using Paketo Buildpack and Docker
Make sure you have [pack CLI](https://github.com/buildpacks/pack) and [Docker](https://www.docker.com/) installed.

```sh
$ pack config default-builder paketobuildpacks/builder-jammy-base
$ pack build java-hello-world
$ docker run -p 5000:5000 java-hello-world
```
Your app should now be running on [localhost:5000](http://localhost:5000/).