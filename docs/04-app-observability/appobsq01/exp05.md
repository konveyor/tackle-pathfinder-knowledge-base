# Logs are written to a file system, sometimes as multiple files

<div class="risk-rounded-box medium">Medium</div>

topic for the question **How does the application use logging and how are the logs accessed?**.

Logging is a very important way for the developer or operator to debug and
investigate the application. Using a file system, or multiple files is a
common practice in many applications, however it is not aligned with the
High Observability principle[1] of container-based application design. The
applications deployed as containers in a container orchestration platform, such
as Kubernetes, should log important events into the standard error and standard
output for log aggregation, because they could be aggregated by the log system
of the container orchestration platform.

Kubernetes does not provide a native storage solution for log data[2], instead
OpenShift uses the logging stack (Kibana, Elasticsearch, Fluentd)[3] to collect
logs from the pods and events to be visualized in Kibana dashboards. This
platform feature[4] allows the application to delegate the log management
to the platform, instead of them.

This question is marked as “Medium” to be reviewed in detail to choose
the best approach to adapt the current log implementation to the best
practices for container-based application designs.

References:
[1. Principles of container-based application design - High Observability Principle](https://www.redhat.com/en/resources/cloud-native-container-design-whitepaper)
[2. Logging Architecture](https://kubernetes.io/docs/concepts/cluster-administration/logging/)
[3. Introduction to the OpenShift 4 Logging Stack](https://cloud.redhat.com/blog/introduction-to-the-openshift-4-logging-stack)
[4. Understanding Red Hat OpenShift Logging](https://docs.openshift.com/container-platform/4.8/logging/cluster-logging.html)
