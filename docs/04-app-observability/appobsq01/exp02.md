# Logs are unavailable or are internal with no way to export them

**Risk Level**: High

Logging is a very important way for the developer or operator to debug and
investigate the application. Without logs there is a big gap in the observability
space of the application, with a huge impact for debugging and operating operations
on a daily basis. If the application does not provide logs or are not able to be
exported, the application is not following the High Observability principle[1]
of container-based application design. The implications of not having these in
place are numerous, none of which are desirable. Therefore, this finding has been
marked as “High” in the assessment report.

Containers are like black boxes, but to become a cloud-native citizen must
provide APIs for a container orchestration platform, such as Kubernetes, to
observe the container’s health and act accordingly. This is a fundamental
prerequisite for automating container life cycles, improving the system’s resilience
and user experience. 

The application should log important events into the standard error and
standard output for log aggregation.

As a better practice, the logs should be collected and stored in a logging system
to facilitate the access, search and consumption for the different teams.
Kubernetes does not provide a native storage solution for log data[2], instead
OpenShift uses the logging stack (Kibana, Elasticsearch, Fluentd)[3] to collect
logs from the pods and events to be visualized in Kibana dashboards. This platform
feature [4] allows the application to delegate the log management to the platform,
instead of them.

References:

[1. Principles of container-based application design - High Observability Principle](https://www.redhat.com/en/resources/cloud-native-container-design-whitepaper)
[2. Logging Architecture](https://kubernetes.io/docs/concepts/cluster-administration/logging/)
[3. Introduction to the OpenShift 4 Logging Stack](https://cloud.redhat.com/blog/introduction-to-the-openshift-4-logging-stack)
[4. Understanding Red Hat OpenShift Logging](https://docs.openshift.com/container-platform/4.8/logging/cluster-logging.html)
