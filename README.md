# Getting Started Project

This project uses Quarkus, the Supersonic Subatomic Java Framework.

If you want to learn more about Quarkus, please visit its website: https://quarkus.io/ .

## Benchmark

Quarkus booted in **0.016 seconds** and operated with **10 MB memory** footprint.

The example uses REST API and dependency injection provided out-of-the-box by Quarkus.

#### Total boot time

<img src="docs/startup.png" width="400">

#### Total memory

<img src="docs/memory.png" width="300">

## Required software

Follow the steps in [Getting Started](https://quarkus.io/guides/getting-started) tutorial.

You'll need to download some tools such as:

- GraalVM + native image
- JDK 11
- An IDE

## Running the application in dev mode

You can run your application in dev mode that enables live coding using:
```
./mvnw quarkus:dev
```

## Packaging and running the application

The application is packageable using `./mvnw package`.
It produces the executable `getting-started-1.0-SNAPSHOT-runner.jar` file in `/target` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/lib` directory.

The application is now runnable using `java -jar target/getting-started-1.0-SNAPSHOT-runner.jar`.

## Creating a native executable

You can create a native executable using: `./mvnw package -Pnative`.

Or you can use Docker to build the native executable using: `./mvnw package -Pnative -Dquarkus.native.container-build=true`.

You can then execute your binary: `./target/getting-started-1.0-SNAPSHOT-runner`

If you want to learn more about building native executables, please consult https://quarkus.io/guides/building-native-image-guide .

## References

[Getting Started](https://quarkus.io/guides/getting-started)

[Building Native Image](https://quarkus.io/guides/building-native-image)