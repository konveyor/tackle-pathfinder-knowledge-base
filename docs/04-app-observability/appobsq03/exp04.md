# Basic application health requires semi-complex scripting

<div class="risk-rounded-box medium">Medium</div>

topic for the question **How easy is it to determine the application's health and readiness to handle traffic?**.

Using health scripts represents a basic practice for the operation or
administration team to identify when the application is not ready or healthy
to attend new requests or to run successfully. However this kind of processes
could now be delegated to the container orchestration platform, such as Kubernetes,
as this capability is provided out of the box. 

In a container orchestration platform containers will be started and stopped
based on a number of events, such as evacuating a worker node for maintenance,
rollout of a new configuration, etc.

To avoid service interruptions for the service consumer, Kubernetes will
continuously verify that a container is ready to receive traffic (readiness probe)
and is healthy (i.e. not in a deadlocked state, etc).

How Kubernetes reacts on probe failure can be configured individually, however
as a prerequisite, these probes need to be implemented by the application. A good
example for a readiness probe is for example a http “/health” endpoint that will
only return a valid status after all server components have been started
and initialized.

There are various options to implement this[1] and good practices around it[2].

The current health scripts could not fit the liveness and readiness probe
requirements, and it will be needed to adapt them accordingly.
Therefore, this finding has been marked as “Medium” in the assessment report.

References:
[1. Monitoring application health by using health checks](https://docs.openshift.com/container-platform/4.8/applications/application-health.html)
[2. Liveness and Readiness Probes](https://cloud.redhat.com/blog/liveness-and-readiness-probes)
