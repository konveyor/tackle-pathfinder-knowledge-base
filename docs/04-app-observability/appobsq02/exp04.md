# Metrics exposed using binary protocols

<div class="risk-rounded-box medium">Medium</div>

topic for the question **Does the application provide metrics?**.

Examples: SNTP, JMX

As a good practice[1], the application provides endpoints to expose
application-specific metrics, however these endpoints use binary protocols
not aligned with standards available to be used in a container orchestration
platform, such as Prometheus[2].

These metrics are a way to determine the overall application health, possible
performance degradation and notify the application or support team in case
certain thresholds are exceeded via an alert manager[3]. Also, these metrics
can be used to feed into the Horizontal Pod Autoscaler (HPA), which will
spin up new application pods (component pods) if necessary[4].

It is recommended to review these metrics endpoints to expose them
using other protocols aligned with the container orchestration platform,
such as Kubernetes. For example, JMX could be exposed using REST API
endpoints using Jolokia[5], a JMX-HTTP bridge. 

The built-in application metrics management is built on Prometheus, therefore
exposing metrics in a Prometheus-compliant format is recommended. Since
Prometheus is used widely for collection of metrics (regardless if you
decide to use the OpenShift Prometheus or a separate, independent instance)
implementation in Prometheus-format is a good investment. Also, since a
huge number of so-called Prometheus “Exporters” and client libraries[6] are
available, making your application metrics consumable by Prometheus
and visualizing on a Grafana Dashboard[7] is straightforward.

References:
1. [Principles of container-based application design - section “HOP” - High Observability Principle](https://www.redhat.com/en/resources/cloud-native-container-design-whitepaper)
2. [Prometheus - Monitoring system & time series database](https://prometheus.io/)
3. [Understanding Red Hat OpenShift's Application Monitoring Operator](https://developers.redhat.com/blog/2019/09/10/understanding-red-hat-openshifts-application-monitoring-operator)
4. [Kubernetes - Horizontal Pod Autoscaler](https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale/)
5. [Jolokia - JMX-HTTP Bridge](https://jolokia.org/)
6. [Prometheus - Exporters and Integrations](https://prometheus.io/docs/instrumenting/exporters/)
7. [Custom Grafana dashboards for Red Hat OpenShift Container Platform 4](https://www.redhat.com/en/blog/custom-grafana-dashboards-red-hat-openshift-container-platform-4)
