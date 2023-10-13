> data.gov.uk Publish Elasticsearch Metrics Exporter is retired

# data.gov.uk Publish Elasticsearch Metrics Exporter

The repository contains the deployment manifests to expose Elasticsearch queue metrics for data.gov.uk Publish.

It relies on the deployment of [Elasticsearch Exporter](https://github.com/justwatchcom/elasticsearch_exporter) (a Go application) to deal create an endpoint that can be accessed by Prometheus.

## Getting Started

This app is deployed on the PaaS.

```
## make sure that you clone the elasticsearch_exporter within the datagovuk_publish_elasticsearch_monitor folder
git clone https://github.com/justwatchcom/elasticsearch_exporter

# staging
cf push -p elasticsearch_exporter -f manifest-staging.yml

# production
cf push -p elasticsearch_exporter -f manifest-production.yml
```

The metrics are accessible online at https://publish-data-staging-elasticsearch-monitor.cloudapps.digital/metrics and https://publish-data-production-elasticsearch-monitor.cloudapps.digital/metrics.
