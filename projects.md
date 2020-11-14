---
layout: page
title: Projects
permalink: /projects/
---

# JHipster

[JHipster](https://jhipster.tech) is an open source code generation platform. I have been involved with the project since 2016. I also serve as secretary for the JHipster Developers Association, a non-profit association dedicated to promoting the project.

# JHipster Control Center

The [JHipster Control Center](https://github.com/jhipster/jhipster-control-center) is a "sidecar application" to manage multiple JHipster applications.
The Control Center automatically detects existing JHipster applications by connecting to a discovery service (Eureka, Consul, Kubernetes) and provide interactive dashboards to interact with each service's management API to realize various operations: view metrics, change log levels, view OpenAPI docs, etc. It can also be integrated with Observability tools (logs, metrics and traces aggregation services). As such it can be used to manage applications during their entire development lifecycle from the developer machine up to production environments.

![Metrics Page 1](/images/jhipster-control-center/jhipster-control-center-metrics1.png)

I was the initiator of this project of which I wrote the [initial specifications in an RFC](https://github.com/jhipster/generator-jhipster/blob/master/rfcs/2-jhipster-rfc-jhipster-control-center.md) and coded the proof of concept to demonstrate the ability to provide dynamic proxying of requests based on different service discovery technologies. We then received a lot of contributions from the community which make the project production ready and recommend its use within the parent JHipster project.

![API docs Page](/images/jhipster-control-center/jhipster-control-center-api-docs.png)


# JHipster Console

The [JHipster Console](https://github.com/jhipster/jhipster-console) is a now deprecated monitoring and alerting solution that helped JHipster users easily set up ELK (Elasticsearch, Logstash, Kibana) and Zipkin using Docker for exploiting logs, metrics and traces from their applications.