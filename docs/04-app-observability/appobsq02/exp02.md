# No metrics available

<div class="risk-rounded-box medium">Medium</div>

topic for the question **Does the application provide metrics?**.

As a good practice, an application should provide endpoints to expose
application-specific metrics, beyond simple data such as memory usage[1].
A good example could be “processed data sets / time”, concurrent sessions,
transactions per second, failed lookups per second, etc.

What is meaningful in the context of a specific application needs to be
determined by the application team, which in turn should expose these metrics.
These metrics are a way to determine the overall application health, possible
performance degradation and notify the application or support team in case
certain thresholds are exceeded via an alert manager[2]. Also, these metrics
can be used to feed into the Horizontal Pod Autoscaler (HPA), which will
spin up new application pods (component pods) if necessary[3].

The built-in application metrics management is built on Prometheus[4],
therefore exposing metrics in a Prometheus-compliant format is recommended.
Since Prometheus is used widely for collection of metrics (regardless if
you decide to use the OpenShift Prometheus or a separate, independent instance)
implementation in Prometheus-format is a good investment. Also, since a
huge number of so-called Prometheus “Exporters” and client libraries[5]
are available, making your application metrics consumable by Prometheus
and visualizing on a Grafana Dashboard [6] is straightforward.

References:
1. [Principles of container-based application design - section “HOP” - High Observability Principle](https://www.redhat.com/en/resources/cloud-native-container-design-whitepaper)
2. [Understanding Red Hat OpenShift's Application Monitoring Operator](https://developers.redhat.com/blog/2019/09/10/understanding-red-hat-openshifts-application-monitoring-operator)
3. [Kubernetes - Horizontal Pod Autoscaler](https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale/)
4. [Prometheus - Monitoring system & time series database](https://prometheus.io/docs/instrumenting/exporters/)
5. [Prometheus - Exporters and Integrations](https://prometheus.io/docs/instrumenting/exporters/)
6. [Custom Grafana dashboards for Red Hat OpenShift Container Platform 4](https://www.redhat.com/en/blog/custom-grafana-dashboards-red-hat-openshift-container-platform-4)
