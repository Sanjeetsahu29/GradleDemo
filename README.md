# Setup of Basic Gradle Project using CLI 
```agsl
gradle init --use-default --type java-application
```
The above command will setup a basic gradle project
```agsl
./gradlew build (for Linux or macOS)
./gradlebat build (for window)
```
To prepare a jar which is executable, you need to setup manifest property in `build.gradle` to identify what is the main class to execute
```groovy
jar{
    manifest{
        attributes(
                "Main-Class":"org.example.Main"
        )
    }
}
```
The above command can build your project
```agsl
./gradlew jar 
```
The above command create a new jar(java archive) file in `build/libs` directory

```agsl
java -jar build/libs/filename.jar
```
the above command will execute your code. 
