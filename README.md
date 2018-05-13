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

Level 0 : 

Callable<T>
Google Protocol Buffers

### Error Handling

- [VND.error](https://github.com/blongden/vnd.error)
- [Spring HATEOAS](https://projects.spring.io/spring-hateoas/)
- [Hypermedia As The Engine Of Application State (HATEOAS) ](https://en.wikipedia.org/wiki/HATEOAS)

### Hypermedia

- [HAL](http://stateless.co/hal_specification.html)

### Media Type and Schema

### API Versioning

### Documenting REST APIs

### The Client Side

### Summary

## Chap 7. Routing

### Cloud Foundry Route Services

/Users/Naoki/src/github.com/cloud-native-java/routing/route-service

```


$ cf login -a https://api.run.pivotal.io

$ cd ~/src/github.com/cloud-native-java/routing/route-service
$ mvn -f pom.xml clean install 
$ cf push route-service
$ cf create-user-provided-service route-service -r https://my-route-service.cfapps.io


$ cd ~/src/github.com/cloud-native-java/routing/downstream-service

$ cf push downstream-service
$ cf bind-route-service cfapps.io route-service --hostname cnj-downstream-service

cf bind-route-service cfapps.io route-service --hostname cnj-route-service
Binding route cnj-route-service.cfapps.io to service instance route-service in org nsegaster-org / space development as nsegaster+pivotal@gmail.com...
OK

➜  downstream-service git:(master) ✗ cf bind-route-service cfapps.io route-service --hostname my-downstream-service
Binding route my-downstream-service.cfapps.io to service instance route-service in org nsegaster-org / space development as nsegaster+pivotal@gmail.com...
OK

```
https://docs.cloudfoundry.org/services/route-services.html
https://docs.pivotal.io/pivotalcf/2-1/services/route-services.html

### Netflix Eureka(https://github.com/Netflix/eureka)

AWS Service registry for resilient mid-tier load balancing and failover.

### [Netflix Ribbon](https://github.com/Netflix/ribbon)

a client-side load balancing library.
Ribbon is a Inter Process Communication (remote procedure calls) library with built in software load balancers. The primary usage model involves REST calls with various serialization scheme support.

### [blog-series-building-microservices](http://callistaenterprise.se/blogg/teknik/2015/05/20/blog-series-building-microservices/)

### [Spring Cloud Netflix](https://cloud.spring.io/spring-cloud-netflix/)

- [Samples/Eureka Server](https://github.com/spring-cloud-samples/eureka)
- [Samples/Eureka Client](https://github.com/spring-cloud-samples/customers-stores)
- [Samples/Minimal Client](https://github.com/spring-cloud-samples/scripts/blob/master/demo/client.groovy)

## Chap 8. Edge Services

## III. Data Integration

## Chap 9. Managing Data

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