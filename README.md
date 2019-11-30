# SpringBoot

Spring Boot makes it easy to create stand-alone, production-grade Spring based Applications that you can "just run".

It take an opinionated view of the Spring platform and third-party libraries so you can get started with minimum fuss. Most Spring Boot applications need very little Spring configuration.


# Features
 1. Create stand-alone Spring applications

 2. Embed Tomcat, Jetty or Undertow directly (no need to deploy WAR files)

 3. Provide opinionated 'starter' dependencies to simplify your build configuration

 4. Automatically configure Spring and 3rd party libraries whenever possible

 5. Provide production-ready features such as metrics, health checks and externalized configuration

 6. Absolutely no code generation and no requirement for XML configuration
 
 # Spring Boot Documentation
 Please refer to https://docs.spring.io/spring-boot/docs/2.2.1.RELEASE/reference/html/documentation-overview.html#boot-documentation
 
# Getting Started
https://docs.spring.io/spring-boot/docs/2.2.1.RELEASE/reference/html/getting-started.html#getting-started-introducing-spring-boot
# versions of Spring boot
Currently there are 2 types of versions-
1. Spring boot 1.x 
   compatible upto java 1.7
   supports only for synchronous based microservices

2. Spring boot 2.x
   compatible from java 8 + versions.
   supports both synchronous and asynchronous (Reactive) micro services
   
 # Why microservices  
 In a software industry there are 2 most popular architecture models are available for designing a software system.
   1. Monolithic architecture
   2. Microservices architecture
   
   
   1. Monolithic architecture-
   In this model where whole project is deployed to a single server and it contains a single database.
   According to our business requirement we must need to configure multiple server inftastructure across multiple region on the globe.
   A server infrastructure means configuring networking monitoring team, a dedicated server machine(which contains application server  like tomcat/jboss etc.).
   The above process increases the budget of project and also load balancing or clustering is a challenging task to meet our current/future market conditions.
   In monolithic architecture all type of user requests submitted to same server .eg. booking ticket, cancelling ticket,user login, user logout etc. and this process increases a load on server which affects the performance of application/project.
   
   To overcome these above problems we need to decompose monolithic ystem into mini services and must be deployed as self contained environment. This type of architecture is known as Microservices architecture.
   

# Developing Your First Spring Boot Application


 
 
