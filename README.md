# Micronaut Weather CLI application

### Micronaut 2.2.1 and GraalVM 20.3.0 Java 11
### use below steps to generate native-image
* Register https://www.weatherbit.io/ to get api key
* export WEATHER_API_KEY=your api key
* export JAVA_HOME=graalvm home directory 
* use $./gradlew nativeImage
* to run $build/native-image/application forecast --country CA --city montreal

### Docker
* Docker Image $./gradlew dockerBuild
* Docker with native-image $ ./gradlew dockerBuildNative
* Check out this link for more information 
The goal of this repository is to demonstrate a real-world use case of Micronaut with Picocli and GraalVM to generate powerful yet simple native images of a command-line application.

This application is built:

* With **Micronaut** as its base:  to show how to use HTTP Clients & other Micronaut such as auto-config
* With **Picocli** to handle all CLI specificities such as options and positional parameters parsing or displaying useful help messages
* With **GraalVM** "native-image" feature enabled in Micronaut so we can easily compile this application down to a native binary.
* With **Weatherbit.io** [weather API](https://www.weatherbit.io/api/) to show interactions with remote services
* With ♥️, but there can still be bugs or problems, contributions are more than welcome !