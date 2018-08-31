# data.gov.uk Publish Elasticsearch Metrics Exporter

The repository contains the deployment manifests to expose Elasticsearch queue metrics for data.gov.uk Publish.

It relies on the deployment of [Elasticseach Exporter](https://github.com/alphagov/datagovuk_publish_elasticsearch_monitor) (a Go application) to deal create an endpoint that can be accessed by Prometheus.

## Getting Started

This app is deployed on the PaaS.

```
git clone https://github.com/justwatchcom/elasticsearch_exporter
cf push -p elasticsearch_exporter -f manifest-staging.yml
cf push -p elasticsearch_exporter -f manifest-production.yml
```

The metrics are accessible online at https://publish-data-staging-elasticsearch-monitor.cloudapps.digital/metrics and https://publish-data-production-elasticsearch-monitor.cloudapps.digital/metrics.

