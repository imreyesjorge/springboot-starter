# Spring Boot Starter
Learn how to create a basic REST response using *Java* with *Spring Boot*.

## Pre-requirements
[] Your preferred Java IDE
[] Internet connection

## What's Spring?
Essentially [Spring](https://spring.io/why-spring) is a framework for [Inversion of Control (IoC)](https://en.wikipedia.org/wiki/Inversion_of_control), and usually it comes with the use of the pattern of [Dependecy Injection (DI)](https://en.wikipedia.org/wiki/Dependency_injection).

Spring can make our projects development way more easy and fast, and in this short guide we'll see Spring in action while creating some REST responses.

## What's IoC?
In software engineering, **Inversion of Control (IoC)** is a programming principle. It does just like the name says, it *inverts* the flow of control. In the regular flow of the program, the custom code calls the library to resolve generic tasks, but with inversion of control, it is the framework that calls into the custom, or task-specific code.

## What's DI?
[Dependency Injection (DI)](https://www.freecodecamp.org/news/a-quick-intro-to-dependency-injection-what-it-is-and-when-to-use-it-7578c84fa88f/) is an IoC technique in wich an object receives other object that it depends on. These other objects are called dependencies.

## Creating your first Java Spring REST responses
1. Go to [start.spring.io](https://start.spring.io/) and create a new Spring project with the *Spring Web* dependency.
2. Open the downloaded project in your preferred IDE.
3. Using the next annotations, create the REST example:
   + **@SpringBootApplication:** This annotation is equivalent to using *@Configuration*, *@EnableAutoConfiguration* and *@ComponentScan*
   + **@RestController:** This annotation tells Spring that this code describes an endpoint that should be made available on the web.
   + **@GetMapping("/"):** This annotation tells Spring to use the method below as a response to a GET petition to the `/` route. (There's also *@Post
   Mapping*, *@PutMapping*, *@DeleteMapping*, etc...)
   + **@RequestParam(value="name", defaultValue="unnamed"):** This annotation is telling spring to expect a `name` value in the request.
4. Try the app with `/.mvnw spring-boot:run`, you can build the JAR with `./mvnw clean package`.   
