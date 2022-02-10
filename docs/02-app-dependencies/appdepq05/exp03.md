# Dependencies require a complex and strict startup order

<div class="risk-rounded-box medium">Medium</div>

topic for the question **Outgoing/southbound dependencies**.

In a container orchestration environment, such as Kubernetes, containers must include
all the dependencies needed to start up and run successfully (aligned with the 
Self-Containment Principle of container-based application design[1]). However many times the
application inside the container requires external dependencies, that they could
not be available.

An application on a container platform needs to accommodate for this and should be
able to automatically check, act and recover from any event with an impact on its
functionality. Manage manage complex and strict dependency startup order could have an
impact in its availability, so it is important to include the right checkpoints to 
verify everything before to manage real traffic.

Generally speaking, applications should implement cloud-native patterns to manage
the availability of the dependencies. Samples of these patterns:

* Circuit Breaker pattern[2] to break cascading failures
* Init containers[3] that run before application containers in a Pod, containing
utilities or setup scripts not present in an application image.
* Checking container startup with startup probes[4].
* Readiness Probe[5] to signal a not-ready state, causing the container platform block any
incoming traffic to the container.
* Liveness Probe[5] to signal a failed state, causing the container platform to restart it.

References:
1. [Principles of container-based application design](https://www.redhat.com/en/resources/cloud-native-container-design-whitepaper)
2. [Circuit Breaker](https://martinfowler.com/bliki/CircuitBreaker.html)
3. [Init Containers](https://kubernetes.io/docs/concepts/workloads/pods/init-containers/)
4. [Startup Probes](https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/#define-startup-probes)
5. [Configure Liveness, Readiness and Startup Probes](https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/)
