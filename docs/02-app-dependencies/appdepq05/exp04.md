# Application not ready until dependencies are verified available

<div class="risk-rounded-box medium">Medium</div>

topic for the question **Outgoing/southbound dependencies**.

In a container orchestration environment, such as Kubernetes, containers must include
all the dependencies needed to start up and run successfully (aligned with the 
Self-Containment Principle of container-based application design[1]). However many times the
application inside the container requires external dependencies, that they could
not be available.

An application on a container platform needs to accommodate for this and should be
able to automatically recover and act from any event with an impact on its
functionality. When an application’s dependencies are not available, it needs to be
able to recover - otherwise it could introduce cascading failures in a Microservices
architecture where it is itself serving as a dependency to other services.

Generally speaking, applications should implement cloud-native patterns to manage
the availability of the dependencies. Samples of these patterns:

* Circuit Breaker pattern[2] to break cascading failures
* Retries policies 
* Readiness Probe[3] to signal a not-ready state, causing the container platform block any
incoming traffic to the container.
* Liveness Probe[3] to signal a failed state, causing the container platform to restart it.

References:
1. [Principles of container-based application design](https://www.redhat.com/en/resources/cloud-native-container-design-whitepaper)
2. [Circuit Breaker](https://martinfowler.com/bliki/CircuitBreaker.html)
3. [Configure Liveness, Readiness and Startup Probes](https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/)
