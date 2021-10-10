---
layout: post
title: The JHipster Control Center - the realization of the JHipster DevOps experience
date: '2021-02-26 12:00:00 +0100'
tags: 'jhipster,devops,microservices,eureka,consul'
categories: articles
---
![JHipster Control Center main page screenshot](/images/covers/jhipster-control-center-intro-1.jpg)
Screenshot of the JHipster Control Center initial version.

<!-- toc -->

<!-- tocstop -->

## Introducing the JHipster Control Center

### Project's origin

In december 2019, I submitted an RFC ([JHipster-RFC-2](https://github.com/jhipster/generator-jhipster/blob/master/rfcs/2-jhipster-rfc-jhipster-control-center.md)) to the JHipster project outlining my vision for a new tool that could be used to manage multiple JHipster applications from a single place.

The premises of this idea was that JHipster excels at providing a good application management experience (eg. administrator dashboards integrated into the generated application), however this experience could greatly benefit from being externalized from the application code for a number of reasons:

1. Reduce the generated code that can now optionally remove the admin screens code
2. Remove the need to maintain 3 times the same admin screen codebase for Angular, React, Vue
3. Manage multiple JHipster applications from the same UI
4. Be able to plug into different service discovery mechanisms such as Eureka, Consul, Kubernetes or a simple static list of addresses

### Distinction with the JHipster-Registry

Since JHipster version 4 (released in 2017), we already offer an application that can manage multiple JHipster microservices from a single UI : the JHipster Registry. However, the JHipster Registry is based on an Eureka server and our attempts to extend it to connect it to non Eureka aware applications have failed. In effect the JHipster Registry's internal working are highly coupled to Eureka which makes it hard to adapt the application to connect to applications using a different service discovery technology such as Consul, Kubernetes or standard DNS.

### Development phase

After initiating the proof of concept in February 2020, I left the project to be lead by the Ippon JHipster internship team which did an awesome job. In particular, I would like to thank in particular [Nassim Errahoui](https://github.com/nassimerrahoui) for leading the development and taking over the project as well as [Pascal Grimaud](https://github.com/pascalgrimaud) for his mentorship. In less than 9 months, the project received 265 commits from 10 contributors in total and reached feature parity and even improved on the JHipster Registry.
TODO update

The JHipster Control Center is fully open source and its development is happening publicly on its [Github repo](https://github.com/jhipster/jhipster-control-center). It is a standard JHipster application based on a reactive Spring Boot back-end and a Vue.js front-end. If you find it useful, you are welcome to join us and contribute.

## Using the JHipster Control Center from development to operations

The JHipster Control Center was envisionned as the swiss army knife that will give you insights into your application at all steps of its lifecycle from developing new features, investigating bugs, observing behavior in production as well as analysing real life performance. We strongly believe in the need for developers to be responsible for their applications in production and as such it makes sense to use the same observability tool whether their application is running locally on their laptop or on a production server.

### Using the JHipster Control Center to simplify development

You can easily start the JHipster Control Center and access it at [localhost:7419](http://localhost:7419) (mnemonic: `7419` is `JHIP` in l33tsp33k):

    docker-compose -f src/main/docker/jhipster-control-center.yml up -d

Then it should detect your running application on its default port (ie. 8080). If you are running it on a different port or if you are running multiple applications, change the environment variables in `src/main/docker/jhipster-control.center.yml` to point it to your applications (one line for each service with its correct port) then run the previous command again.

```
jhipster-control-center:
    [...]
    environment:
    [...]
      - SPRING_CLOUD_DISCOVERY_CLIENT_SIMPLE_INSTANCES_SAMPLEAPP1_0_URI=http://host.docker.internal:8081
      - SPRING_CLOUD_DISCOVERY_CLIENT_SIMPLE_INSTANCES_SAMPLEAPP2_0_URI=http://host.docker.internal:8081
    [...]
```

### Using the JHipster Control Center in staging environments

### Using the JHipster Control Center in production environments 

## Conclusion




// insert pic 1


