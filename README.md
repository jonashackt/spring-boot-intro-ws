# Ueberblicks-Workshop zu Spring Boot, Cloud, Docker, Admin, Infra-as-Code, usw.

> "Das große Ganze verstehen"

...dynamisch, Praxiserfahrungen, teils hands-on

Meine Zusatzempfehlungen: Architekturansatz Microservices, TDD!, CI/CD, Infrastructure-as-Code, Log-Korrelation, Containerisierung...



## Kurzvorstellung

Maintainer Spring Boot Starter for Apache CXF SOAP Webservices: [google](https://www.google.de/) __spring boot cxf__

Guter Gesamtüberblick über sehr viele Aspekte der Entwicklung mit Spring Boot: https://blog.codecentric.de/2016/02/spring-boot-apache-cxf/

Aktuell "Infrastructure-as-Code" / Continuous Delivery / Docker(isierung) / Orchestrierung / Gesamtarchitektur

[cc Team-Seite](https://www.codecentric.de/team/jonas-hecht/) | [jonashackt.github.io/](https://jonashackt.github.io/) | [@jonashackt](https://twitter.com/jonashackt)



## Architekturübersicht - was ist Spring Boot? Was sind Spring Boot Starter?

http://slides.com/jonashackt/dos-spring-01#/

Tipp: https://spring.io/guides


#### Hands-On Beispiel 1: Das erste eigene Spring Boot Projekt

http://slides.com/jonashackt/dos-spring-01-3#/

__part2:__ https://github.com/jonashackt/spring-and-rest-basics


## Praxiserfahrungen

Nochmal :) https://blog.codecentric.de/2016/02/spring-boot-apache-cxf/


#### 1. Umgebungsabhängige Konfiguration

`java -jar foo.jar --server.port=8079` ---> Umgebungsvariablen! ---> git! ---> Ansible!

Beispiel: https://blog.codecentric.de/en/2017/01/ansible-windows-spring-boot/


#### 2. Testen / TDD

`src/main/java` & `src/test/java` --> IntelliJ example

https://blog.codecentric.de/2016/06/spring-boot-apache-cxf-soap-webservices-testen/


#### Hands-On Beispiel 2: Spring Boot & RESTful Webservices

> Da fährt einfach ein Web- & Applicationserver hoch??!

--> Spring Boot vs. Applicationserver

http://slides.com/jonashackt/dos-spring-01-3#/

__part3 & part4:__ https://github.com/jonashackt/spring-and-rest-basics


Tipps: [REST-assured](https://github.com/rest-assured/rest-assured); [Springfox REST API visualizer](https://github.com/springfox/springfox)


#### 3. Logging / Logkorrelation

[sl4j Logging Facade](https://www.slf4j.org/) + [logback](https://logback.qos.ch/)
 
__+__

[Open Source Elastic Stack](https://www.elastic.co/de/products)

https://blog.codecentric.de/2016/07/spring-boot-apache-cxf-logging-monitoring-logback-elasticsearch-logstash-kibana/

https://github.com/jonashackt/docker-elk


#### 4. Microservices mit Spring Cloud

http://projects.spring.io/spring-cloud/ & https://cloud.spring.io/spring-cloud-netflix/

[google](https://www.google.de/) __scale spring boot__

https://blog.codecentric.de/en/2017/05/ansible-docker-windows-containers-scaling-spring-cloud-netflix-docker-compose/

Complete example project: https://github.com/jonashackt/cxf-spring-cloud-netflix-docker


#### 5. Spring Boot Admin

Basically an Frontend for [Spring Boot Actuator Endpoints](https://docs.spring.io/spring-boot/docs/current/reference/html/production-ready-endpoints.html)

http://codecentric.github.io/spring-boot-admin/1.5.4/

example project (again): https://github.com/jonashackt/cxf-spring-cloud-netflix-docker


#### 6. Spring Boot & Container / Docker

http://slides.com/jonashackt/dos-spring-01-4#/

Beispielprojekt --> https://github.com/jonashackt/cxf-spring-cloud-netflix-docker

`docker-compose up -d`

#### Hands-On Beispiel 3: Spring Boot & Docker

Spring Boot App Dockerisieren: __part7__: https://github.com/jonashackt/spring-and-rest-basics


#### 7. Build-Prozess & CI/CD

__Maven__ (Gradle)

good CI-Server: [Gitlab CI](https://about.gitlab.com/features/gitlab-ci-cd/), [Concourse](https://concourse.ci/), (Jenkins)

Docker für parallele Feature- oder sogar Release-Entwicklung

__Infrastructure as Code__: [google](https://www.google.de/) __spring boot docker ansible__

https://blog.codecentric.de/en/2017/04/ansible-docker-windows-containers-spring-boot/


#### 8. Wohin mit wiederverwendbarer (technischer) Frameworklogik? --> der eigene Spring Boot Starter

https://blog.codecentric.de/2016/10/spring-boot-apache-cxf-spring-boot-starter/


#### 9. Spring Boot & a modern Webfrontend (Vue.js)

Angular or React.js or Vue.js...

* Build-Process, Maven to handle it all (NPM, Node, Bower, Grunt, Gulp, Webpack...)

* Development-Process (npm run dev + Spring Boot Devtools), Single-Origin Policy

https://github.com/jonashackt/spring-boot-vuejs


#### 10. Spring Boot & Databases

Spring Data to rule them all! (relational, non-relational, whatever-DB)

http://projects.spring.io/spring-data/

Example-Project: https://github.com/jonashackt/spring-boot-vuejs

https://github.com/jonashackt/spring-boot-vuejs/blob/master/backend/pom.xml

[UserRepositoryTest.java](https://github.com/jonashackt/spring-boot-vuejs/blob/master/backend/src/test/java/de/jonashackt/springbootvuejs/repository/UserRepositoryTest.java)

[UserRepository.java](https://github.com/jonashackt/spring-boot-vuejs/blob/master/backend/src/main/java/de/jonashackt/springbootvuejs/repository/UserRepository.java)

REST-Services on top...

[BackendControllerTest.java](https://github.com/jonashackt/spring-boot-vuejs/blob/master/backend/src/test/java/de/jonashackt/springbootvuejs/controller/BackendControllerTest.java)

[BackendController.java](https://github.com/jonashackt/spring-boot-vuejs/blob/master/backend/src/main/java/de/jonashackt/springbootvuejs/controller/BackendController.java)

