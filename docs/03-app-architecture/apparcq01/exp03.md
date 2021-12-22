# Application fails when a southbound dependency is unavailable and does not recover automatically

<div class="risk-rounded-box high">High</div>

topic for the question **How resilient is the application? How well does it recover from outages and restarts?**.

In a container orchestration platform, such as Kubernetes, containers are started
and stopped based on external events, while Kubernetes makes sure that deployment
configurations (e.g. minimum of 3 pods (groups of containers) running at any time)
are upheld.

An application on a container platform needs to accommodate for this and should
be able to automatically recover from a restart. Also, when an application’s
dependencies are not available, it needs to be able to recover - otherwise it
could introduce cascading failures in a Microservices environment where it is
itself serving as a dependency to other services (which can be avoided by applying
the Circuit Breaker pattern[1]).

Generally speaking, required manual intervention in a running application is
an antipattern in the container world.

The application can either recover by itself, using retries or similar mechanisms, or its Liveness Probe [2],[3] can signal a failed state, causing the container
platform to restart it.

Either way, an application that does not recover by itself or with help of the
container orchestration will sooner or later end in severely deteriorating
services, since the application is still running (not crashed) but not serving
meaningful responses. The container platform would not notice and decide that
deployment requirements (e.g. “always have a minimum of 2 pod running”) are
still satisfied.

This risk needs to be addressed before deploying any production-grade
services with this gap.

References:
[1. Circuit Breaker](https://martinfowler.com/bliki/CircuitBreaker.html)
[2. Configure Liveness, Readiness and Startup Probes](https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/)
[3. Liveness and Readiness Probes](https://cloud.redhat.com/blog/liveness-and-readiness-probes)
