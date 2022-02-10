# Dependency availability only verified when application is processing traffic

<div class="risk-rounded-box high">High</div>

topic for the question **Outgoing/southbound dependencies**.

In a container orchestration environment, such as Kubernetes, containers must include
all the dependencies needed to start up and run successfully (aligned with the 
Self-Containment Principle of container-based application design[1]). However many times the
application inside the container requires external dependencies, that they could
not be available.

An application on a container platform needs to accommodate for this and should be
able to automatically check, act and recover from any event with an impact on its
functionality. That processes should be done along the runtime life cycle of the application
and not only when is processing real traffic. Otherwise the application is delegating
to have traffic, and adding an overhead, to check the availability of any dependency. This
risk should be mitigated including the right checkpoints to verify everything before and
during the application runtime life cycle. Kubernetes could check these results and takes
the best actions to recover the application's status.

Generally speaking, applications must implement cloud-native patterns to manage
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
