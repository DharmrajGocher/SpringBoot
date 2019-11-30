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
   
   
 
   In this model where whole project is deployed to a single server and it contains a single database.
   According to our business requirement we must need to configure multiple server inftastructure across multiple region on the globe.
   A server infrastructure means configuring networking monitoring team, a dedicated server machine(which contains application server  like tomcat/jboss etc.).
   The above process increases the budget of project and also load balancing or clustering is a challenging task to meet our current/future market conditions.
   In monolithic architecture all type of user requests submitted to same server .eg. booking ticket, cancelling ticket,user login, user logout etc. and this process increases a load on server which affects the performance of application/project.
   
   To overcome these above problems we need to decompose monolithic ystem into mini services and must be deployed as self contained environment. This type of architecture is known as Microservices architecture.

# Rules of microservices
 1. Application must be self contained .i.e it must run in its own process.
 2. It must have its own server.
 3. It must have its own memory
 4. It must have its own database.
 
 Note- A microservice menas a webservice implemented either by SOAP/RESTful and must contains only one operation.
 
 # Components of Spring Boot
 1. Starters
 2. AutoConfiguration
 3. CLI
 4. Actuators
 
 
    1.Starters:-

 Starters are a set of convenient dependency descriptors that you can include in your application. You get a one-stop shop for all the Spring and related technologies that you need without having to hunt through sample code and copy-paste loads of dependency descriptors. For example, if you want to get started using Spring and JPA for database access, include the spring-boot-starter-data-jpa dependency in your project.

The starters contain a lot of the dependencies that you need to get a project up and running quickly and with a consistent, supported set of managed transitive dependencies.

All official starters follow a similar naming pattern; spring-boot-starter-*, where * is a particular type of application. This naming structure is intended to help when you need to find a starter.
 
 All the predefined starters of spring boot belongs to org.springframework.boot package.
 
 2. Auto Configuration:-
 Every spring boot starter comes with a auto configuration class & which is responsible to perform integration/configuration setup for our application according to given input.
 E.g.-
 Suppose if we add spring-boot-starter-jdbc in our pom.xml, internally the auto configuration class of the given starter performs a below operations.
     1. It finds whether a JDBC driver is present in CLASSPATH or NOT.
     2. If it is present then based on given DB inputs like DB URL, User, Password etc, it perform DataSource Configuration with help of Hikari datasource connection pool.
     
 3. Command Line interface(CLI):-
 It is a special tool used for groovy based developers for generating grrovy script for spring boot application quickly.
 For Srping boot CLI NO need to work with starters concept because depends on the coding, required libraries are automatically bundled during the execution process.
 
 4. Actuators:-
 Once a product is deployed in production environment then memory management, health checkup is by defaultly provided by actuators.
 We can develop a custom actuators. Infact an actuators are also a microservice.
     

# Developing Your First Spring Boot Application
There are 2 ways we can configure our project from https://start.spring.io/.
1. A project skeleton can be downloaded as a zip file from  https://start.spring.io/ and we can import it to our IDE.
2. By using IDE with help of spring boot plugin, we can configure our project and which will be passed internally to start.spring.io
website in the background and automaticall the zip file is downloaded into IDE.
Spring Tool Suite (STS) and Intellij IDEs by default comes with Spring boot plugin and for other iDES like Eclipse we need to configure spring boot plugin.

<code>
package com.dharma.SampleApp;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class SampleAppApplication {

	public static void main(String[] args) {
		SpringApplication.run(SampleAppApplication.class, args);
	}

}
<code>
# The “main” Method
The final part of our application is the main method. This is just a standard method that follows the Java convention for an application entry point. Our main method delegates to Spring Boot’s SpringApplication class by calling run. SpringApplication bootstraps our application, starting Spring, which, in turn, starts the auto-configured Tomcat web server. We need to pass Example.class as an argument to the run method to tell SpringApplication which is the primary Spring component. The args array is also passed through to expose any command-line arguments.


Hopefully, this section provided some of the Spring Boot basics and got you on your way to writing your own applications.
 
 
