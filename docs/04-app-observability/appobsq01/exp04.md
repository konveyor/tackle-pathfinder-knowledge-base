# Logs are exposed using syslog

<div class="risk-rounded-box medium">Medium</div>

topic for the question **How does the application use logging and how are the logs accessed?**.

Using syslog for messaging logging on Linux systems represents a good starting point
on the observability space. This tool offers mechanisms for the developer or
operator to debug and investigate the application. These mechanisms could include
log aggregation, formatters, analyzers, ...

Kubernetes does not provide a native storage solution for log data[1], however
by default, OpenShift Logging sends container and infrastructure logs to the
default aggregation log store based in Kibana, ElasticSearch and Fluentd[2].
This feature is usually enough to debug and investigate the applications and
infrastructure on the daily basics, but also include the capability to send
these logs to other log aggregators[3], as syslog[4].

This question is marked as “Medium” to be reviewed in detail to choose the
best approach to integrate the current syslog mechanisms with the
logging capabilities provided by the container orchestration platform.

References:
1. [Principles of container-based application design - High Observability Principle](https://www.redhat.com/en/resources/cloud-native-container-design-whitepaper)
2. [Logging Architecture](https://kubernetes.io/docs/concepts/cluster-administration/logging/)
3. [Introduction to the OpenShift 4 Logging Stack](https://cloud.redhat.com/blog/introduction-to-the-openshift-4-logging-stack)
4. [Understanding Red Hat OpenShift Logging](https://docs.openshift.com/container-platform/4.8/logging/cluster-logging.html)
