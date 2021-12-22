# Logs are in a custom binary format, exposed with non-standard protocols

<div class="risk-rounded-box high">High</div>

topic for the question **How does the application use logging and how are the logs accessed?**.

Using custom binary log format or exposing with non-standard protocols could
require adding complex integrations between the container orchestration platform,
such as Kubernetes, and external log systems, implementing those binary formats or
protocols. These integrations could have an impact in the way the target systems
manage the logs coming from the containers, which are ephemeral processes deployed
in the container orchestration platform, or how to set up everything accordingly.
It will be required to review these processes and align with the best practices in
the container-based application designs.

The High Observability principle[1] of container-based application design, the
application should log important events into the standard error and standard
output for log aggregation. As a better practice, the logs should be collected
and stored in a logging system to facilitate the access, search and consumption
for the different teams. Kubernetes does not provide a native storage solution
for log data[2], instead OpenShift uses the logging stack (Kibana, Elasticsearch,
Fluentd)[3] to collect logs from the pods and events to be visualized in Kibana
dashboards. This platform feature [4] allows the application to delegate the log
management to the platform, instead of them.

References:
[1. Principles of container-based application design - High Observability Principle](https://www.redhat.com/en/resources/cloud-native-container-design-whitepaper)
[2. Logging Architecture](https://kubernetes.io/docs/concepts/cluster-administration/logging/)
[3. Introduction to the OpenShift 4 Logging Stack](https://cloud.redhat.com/blog/introduction-to-the-openshift-4-logging-stack)
[4. Understanding Red Hat OpenShift Logging](https://docs.openshift.com/container-platform/4.8/logging/cluster-logging.html)
