# Massive monolith (high memory and CPU usage), non-singleton deployment, complex to scale horizontally

**Risk Level**: Medium

The application has been designed in a traditional, monolithic architecture -
however, it is not complex to scale horizontally, as a Load Balancer in front of
it would be the only requirement of more than one instance. (No exact answer
match, the closest one was chosen).

While it is possible to deploy monolithic applications as containers, several of the
benefits of using a container orchestration platform remain unused[1]:

* Smaller components can be scaled independently, providing effective resource
usage, elasticity and leveraging autoscaling functionality brought by the platform.
* Smaller components can be updated independently, if done right - allowing for
faster turnaround times and higher degrees of deployment and test automation
* Smaller components typically have a faster startup time, making rescheduling,
autoscaling and other Kubernetes events more effective.

An ideal container-based application should follow the 12-Factor App principles[2],
using smaller, decoupled components. While not all of these are achievable under
all circumstances, these principles should guide refactoring efforts and strategies.

References:
[1. What is Kubernetes?](https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/)
[2. The Twelve-Factor App](https://12factor.net/)
