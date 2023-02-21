# Portfolio-charts repository is a repo created with CrossyRoad application and all it's Helm charts..

### The repository contains the following Helm charts:
* application
Application: Has the application yaml files themself, the mysql database that the app depends on,
and the nginx ingress controller that accepts trific from the enviroment.
Application helm chart also depends on resources in other charts - security charts and kibana.

* appfiles
Appfiles: Is not acctualy helm chart, but has manifests of ArgoCD application files, and build them in
form of 'app of apps' structure. Every application file builds a chart in the repo.

* logging/fluentd
Fluentd: In charge to build the fluentd DaemonSet to the logging procces.

* logging/elasticsearch
Elasticsearch: In charge to build the Elasticsearch database and the Kibana UI to the logging procces.

* monitoring/prometheus
Prometheus: Collect metrics in the cluster and serve them as data.

* monitoring/grafana
Grafana: Friendly UI to prometheus with cool dashboards and alerting option.
