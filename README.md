## Ex-23 Create an API to print HELLO WORLD
## AIM:
To Create an API to print HELLO WORLD using sping boot.
## ALGORITHM:
### STEP 1:
Generate the spring API using spring initializr.
### STEP 2:
create HelloController class through which hello world is displayed.
### STEP 3:
Add dependencies in build.gradle.
### STEP 4:
Run the API in browser.
### STEP 5:
Verify whether API running properly.
## PROGRAM:
HelloworldApplication.java
```java
package com.spring.helloworld;
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
@SpringBootApplication
public class HelloworldApplication {
     public static void main(String[] args) {
            SpringApplication.run(HelloworldApplication.class, args);
       }
 }
 ```
HelloController.java
```java
package com.spring.helloworld.controller;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;
@RestController
public class HelloController {
    @GetMapping("/hello")
    public String helloWorld() {
            return "Hello, World!";
    }
}
```
build.gradle
```java
plugins {
    id 'java'
    id 'org.springframework.boot' version '3.1.0'
    id 'io.spring.dependency-management' version '1.1.0'
}
group = 'com.spring'
version = '0.0.1-SNAPSHOT'
java {
    sourceCompatibility = '17'
}
repositories {
    mavenCentral()
}
dependencies {
     // implementation 'org.springframework.boot:spring-boot-starter-data-jpa'
     implementation 'org.springframework.boot:spring-boot-starter-web'
     // runtimeOnly 'org.postgresql:postgresql'
     testImplementation 'org.springframework.boot:spring-boot-starter-test'
}
tasks.named('test') {
      useJUnitPlatform()
}
```
## OUTPUT:
![image](https://github.com/SarankumarJ/Create-an-API-to-print-HELLO-WORLD/assets/94778101/12e2a706-5ee3-4576-a82e-bdc76eeb4f84)

## RESULT:
An API to print HELLO WORLD using sping boot has been executed successfully.
