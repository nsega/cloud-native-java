# cloud-native-java

[Cloud Native Java](http://shop.oreilly.com/product/0636920038252.do)

## Part I. Basics

## Chap 1. The Cloud Native Application

### The Tweleve Factors

## Chap 2. Bootcamp : Introducing Spring Boot and Cloud Foundry

- [Spring Initilizr](http://start.spring.io/)

- [Building an Application with Spring Boot](https://spring.io/guides/gs/spring-boot/)

## Chap 3. Twelve-Factor Application Style Configuration

- [Twelve-Factor application manifesto](https://12factor.net/config)

## Chap 4. Testing

## Chap 5. The Forklifted Application

The goal of this chapter was to address common concerns typical of efforts to move existing legacy applications to the cloud.

- [JavaBuildpack](https://github.com/cloudfoundry/java-buildpack)
- [okta](https://developer.okta.com/)

## Part II. Web Services

## Chap 6. REST APIs

### Error Handling

- [VND.error](https://github.com/blongden/vnd.error)
- [Spring HATEOAS](https://projects.spring.io/spring-hateoas/)
- [Hypermedia As The Engine Of Application State (HATEOAS)](https://en.wikipedia.org/wiki/HATEOAS)

### Hypermedia

- [HAL](http://stateless.co/hal_specification.html)

### Media Type and Schema

### API Versioning

### Documenting REST APIs

### The Client Side

### Summary

## Chap 7. Routing

### Cloud Foundry Route Services

```
$ cf login -a https://api.run.pivotal.io

$ cd ~/src/github.com/cloud-native-java/routing/route-service
$ mvn -f pom.xml clean install 
$ cf push route-service
$ cf create-user-provided-service route-service -r https://my-route-service.cfapps.io

$ cd ~/src/github.com/cloud-native-java/routing/downstream-service

$ cf push downstream-service
$ cf bind-route-service cfapps.io route-service --hostname cnj-downstream-service
```

### Cloud Foundry Route Services

[Cloud Foundry Route Services](https://docs.cloudfoundry.org/services/route-services.html)

### [Netflix Eureka](https://github.com/Netflix/eureka)

- AWS Service registry for resilient mid-tier load balancing and failover.

### [Netflix Ribbon](https://github.com/Netflix/ribbon)

a client-side load balancing library.
Ribbon is a Inter Process Communication (remote procedure calls) library with built in software load balancers. The primary usage model involves REST calls with various serialization scheme support.

### [Netflix Feign](https://cloud.spring.io/spring-cloud-netflix/)

a library from Netflix that makes deriving service clients as simple as an interface definition and some conventions.

### [Netflix Zuul](https://github.com/Netflix/zuul)

a gateway service that provides dynamic routing, monitoring, resiliency, security, and more.

### [Netflix Prana](https://github.com/Netflix/Prana)

### [blog-series-building-microservices](http://callistaenterprise.se/blogg/teknik/2015/05/20/blog-series-building-microservices/)

### [Spring Cloud Netflix](https://cloud.spring.io/spring-cloud-netflix/)

- [Samples/Eureka Server](https://github.com/spring-cloud-samples/eureka)
- [Samples/Eureka Client](https://github.com/spring-cloud-samples/customers-stores)
- [Samples/Minimal Client](https://github.com/spring-cloud-samples/scripts/blob/master/demo/client.groovy)

## Chap 8. Edge Services

### Security on the Edge

- [Zuul's architecture](https://www.slideshare.net/MikeyCohen1/zuul-netflix-springone-platform)

### OAuth

- Client, Resource owner, Resource server, Authorization server

### Spring Security

### Spring Cloud Security

#### Securing the Greetings Resource Server

### Build an OAuth-Secured Single-Page Application

## III. Data Integration

## Chap 9. Managing Data

Spring Data’s mission is to provide a familiar and consistent, Spring-based programming model for data access while still retaining the special traits of the underlying data store. 

- [Spring Data](http://projects.spring.io/spring-data/)
- [Spring Data JPA](https://projects.spring.io/spring-data-jpa/)
- [Spring Data JDBC](https://github.com/nurkiewicz/spring-data-jdbc-repository)
- [Spring Data MongoDB](https://projects.spring.io/spring-data-mongodb/)
- [Spring Data Neo4j](https://projects.spring.io/spring-data-neo4j/)
- [Spring Data Redis](https://projects.spring.io/spring-data-redis/)

## Chap 10. Messaging

## Chap 11. Batch Process and Tasks

## Chap 12. Data Integration

## IV. Production

## Chap 13. The Observable System

## Chap 14. Service Brokers

## Chap 15. Continious Delivery

### ref URL

- [What is username and password when starting Spring Boot with Tomcat?](https://stackoverflow.com/questions/37285016/what-is-username-and-password-when-starting-spring-boot-with-tomcat)
- [Spring Boot boot-features-security](https://docs.spring.io/spring-boot/docs/1.5.9.RELEASE/reference/htmlsingle/#boot-features-security)
- [Spring Cloud Case Study](https://www.infoq.com/presentations/spring-boot-cloud-case-study)