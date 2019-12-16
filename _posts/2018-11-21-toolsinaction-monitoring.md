---
layout: post
title: "Tools in action - Monitoring a JHipster microservice architecture in practice"
date: 2018-11-21 14:09:24 +0100
categories: talks
---

I gave this 25 minutes talk 3 times in 2018 at 3 different conferences (VoxxedDays microservice, JHipster Conf and Devoxx France).
It has been enriching to do it several times to different audiences and being able to get more and more confident each time.
It was also a good challenge to constrain the talk time to 25 min as I was initially planning for 45 min.
It is much easier to get a a spot at conferences for a tools in action,
so I think I will stick to this format in the future but maybe try to reduce the scope of what I want to present.

# Video

<iframe width="560" height="315" src="https://www.youtube.com/embed/NpLef-jmX2Y" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# Summary of the talk

After a brief overview of the problems encountered when monitoring microservices, I demonstrate how the [JHipster Console](https://github.com/jhipster/jhipster-console) can help you monitor a JHipster microservice architecture and how it provides an integrated solution for the the 3 ways of observability:

1. **Logs :** Kibana and Elasticsearch are leveraged to view, aggregate and search logs.
2. **Metrics :** Internal application metrics can be graphed and studied using newer features of Kibana and Elasticsearch.
3. **Traces :** By integrating the Zipkin UI and Kibana through dynamic links between the 2 UIs, one can easily jump between the distributed trace latency graph and the logs associated with a given Trace ID.

# Links

### Github repo

The code was published to [pierrebesson/microservice-monitoring-tools-in-action-demo](https://github.com/PierreBesson/microservice-monitoring-tools-in-action-demo), it will allow you to run the demo locally with docker compose and everything working out of the box.

### VoxxedDays Microservices (October 29th 2018)

- [Session details on the VoxxedDays Microservices website](https://vxdms2018.confinabox.com/talk/VNM-6703/Monitoring_a_JHipster_microservice_architecture_in_practice)
- [Youtube video](https://www.youtube.com/watch?v=NpLef-jmX2Y)
- [Slides](https://pierrebesson.github.io/microservice-monitoring-tools-in-action-slides/)

#### Screenshots

![Kibana Logs dashboard](image::/images/2018-monitoring-tools-in-action/logs-dashboard.png)

![Graphing a custom metric with Kibana](/images/2018-monitoring-tools-in-action/graphing-a-custom-metric.png)

![Trace Error in Zipkin](/images/2018-monitoring-tools-in-action/trace-error.png)

![Trace logs in Kibana](/images/2018-monitoring-tools-in-action/trace-logs.png)

### JHipster Conf (June 21th 2018)

- [Agenda on the JHipster Conf website (archive.org link)](https://web.archive.org/web/20180627154623/https://jhipster-conf.github.io/)
- No video

### Devoxx France (April 19th 2018), in French

- [Session details on the DevoxxFr website](https://cfp.devoxx.fr/2018/talk/ZZR-7431/Monitoring_en_pratique_d'une_architecture_microservice_JHipster)
- [Youtube video (in French)](https://www.youtube.com/watch?v=yG7zu0Nqa5Y)
- [Slides](https://pierrebesson.github.io/devoxxfr-2018-monitoring-slides/)
