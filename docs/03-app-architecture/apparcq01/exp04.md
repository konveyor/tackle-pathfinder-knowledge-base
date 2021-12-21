# Application functionality is limited when a dependency is unavailable but recovers when the dependency is available

**Risk Level**: Medium

In a container orchestration environment, such as Kubernetes, containers are started
and stopped based on external events, while Kubernetes makes sure that deployment
configurations (e.g. minimum of 3 pods (groups of containers) running at any time)
are upheld.

An application on a container platform needs to accommodate for this and should
be able to automatically recover from a restart. Also, when an application’s
dependencies are not available, it needs to be able to recover - otherwise
it could introduce cascading failures in a Microservices environment where it is
itself serving as a dependency to other services (which can be avoided by applying the Circuit Breaker pattern[1]).

Generally speaking, required manual intervention in a running application
is an antipattern in the container world.

The application can either recover by itself, using retries or similar mechanisms,
or its Liveness Probe [2],[3] can signal a failed state, causing the container
platform to restart it.

References:
[1. Circuit Breaker](https://martinfowler.com/bliki/CircuitBreaker.html)
[2. Configure Liveness, Readiness and Startup Probes](https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/)
[3. Liveness and Readiness Probes](https://cloud.redhat.com/blog/liveness-and-readiness-probes)
