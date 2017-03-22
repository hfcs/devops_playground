# DevOps Playground

A collection of examples deploying logging/monitor/visualization/utilities for
microservice apps.

## `vagrant_vm`

A [Vagrant](https://www.vagrantup.com/) example deploying virtualbox VM images,
with following infrastructures.

* [Consul](https://www.consul.io/) for service discovery, service health,
shared key/value storage.  
* [Prometheus](https://prometheus.io/) for monitoring, alert, and time series
statistics.
  * [Statsd](https://github.com/etsy/statsd) for monitor agnostic metrics, apps
  from different languages just call statsd library and send their metrics.
  * [statsd_exporter](https://github.com/prometheus/statsd_exporter) exposes
  metrics from app nodes to be collected by monitor node.
* [ELK Stack](https://www.elastic.co/webinars/introduction-elk-stack) for
centralized logging, a collection of [Logstash](https://www.elastic.co/products/logstash),
[Elasticsearch](https://www.elastic.co/products/elasticsearch), and
[Kibana](https://www.elastic.co/products/kibana).
  * [Filebeat](https://www.elastic.co/products/beats/filebeat) ships logs from
  app nodes to logging node.
* [Grafana](grafana.org) for visualization, analytic, and alert of monitor
and logging (notice Grafana may replace Kibana).
* [Redis](https://redis.io/) for in-memory data store, message broker.  
* [MEAN](https://en.wikipedia.org/wiki/MEAN_(software_bundle) for Javascript
based full stack and use [ExpressJS](expressjs.com) for backend services.
