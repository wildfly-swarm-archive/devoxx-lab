# Decomposing a Java EE monolith into WildFly Swarm microservices

This lab will introduce the developer to WildFly Swarm through the migration of a Java EE monolith appplication to microservices for parts of the stack. The services will be discoverable, provide failover with Netflix Ribbon, and utilize Netflix Hystrix for circuit breaking amongst other things.

See also http://cfp.devoxx.co.uk/2016/talk/OAL-7049/Decomposing_a_Java_EE_monolith_into_WildFly_Swarm_microservices

## Preparing your laptop

If you plan to attend the lab, there is a couple of things you can do before the actual workshop to ensure a pleasant experience.

### Minimum System Requirements

At a bare minimum you'll need the following things on your laptop:

- [JDK 8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
- [Maven 3.3.x](https://maven.apache.org/download.cgi)
- IDE ([Eclipse](http://www.eclipse.org/downloads/packages/eclipse-ide-java-developers/keplersr1), Intellij)
- [Git](https://git-scm.com/downloads)

## Additional Software

During the lab we are going to require some components that the lecturer will provide. Among these things are components for service registration and discovery and other parts that are typically provided by the deployment environment.

These components will be made available as shared services throughout the room. However if you plan to use some of it on your laptop, then we recommend the following additional components:

- [Docker](https://www.docker.com/)
- [Consul](https://hub.docker.com/r/progrium/consul/)

## Warm up your maven repo

We are running on a shared WIFI at the lab location, so preparing your local maven repo upfront can save you valuable time at the workshop.

The most simple way to prepare your local repository, is to build one of the WildFly Swarm examples:

1) Checkout the WildFly Swarm examples

The following commands will checkout the examples tagged '1.0.0.CR1'.

```
git clone https://github.com/wildfly-swarm/wildfly-swarm-examples.git

git checkout tags/1.0.0.CR1 -b swarm-examples-1.0.0.CR1
```

2) Build the JPA/JAX-RS examples

This may take some time to complete. Make sure you run it on a decent broadband connection.

```
cd swarm-examples-1.0.0.CR1
cd base
mvn clean install
cd ../jpa-jaxrs-cdi/
mvn clean install
```

## The lab sources

The source code for the lab will be provided on Friday. If you have any questions upfront, don't hesitate to contact us here:

https://groups.google.com/forum/?nomobile=true#!forum/wildfly-swarm

## Reading on microservices concepts

We will cover general microservice concepts during the lab to some extend, but cannot fully cover the wide range of concepts and ideas that relate to it without sacrificing time for practical activities.

It's therefore recommended that you read up about microservices concepts to some degree and relate this information to a situation that concerns you, like a recent software project or upcoming architectural discussions with your peers.

Your feedback and questions during the workshop will help to drive the direction of the activities and and make it valuable experience for everybody attending.

The following is a list of resources that we can recommend to get you started.

*Online articles*
- Eberhard Wolff, "Microservices Primer": https://leanpub.com/microservices-primer
- Martin Fowler, "Microservices in a Nutshell":  https://www.thoughtworks.com/de/insights/blog/microservices-nutshell

*Microservice Books*
- Sam Newman. "Building Microservices": http://shop.oreilly.com/product/0636920033158.do
- Eric Evans, "Domain Driven Design": http://www.amazon.com/Domain-Driven-Design-Tackling-Complexity-Software/dp/0321125215

*WildFly Swarm*
- Homepage: http://wildfly-swarm.io/
- User Guide:  https://wildfly-swarm.gitbooks.io/wildfly-swarm-users-guide/content/v/7d7ea3560e6b65f673bc76ff7fd65499e28ffca2/

*OpenShift*
- OpenShift Origin: https://www.openshift.org/


# Questions?

If you have any questions before the lab, contact us here:

https://groups.google.com/forum/?nomobile=true#!forum/wildfly-swarm
