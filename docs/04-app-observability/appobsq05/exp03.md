# 2-5 minutes

<div class="risk-rounded-box medium">Medium</div>

topic for the question **How long does it take the application to be ready to handle traffic?**.

The time the application takes to be ready from the moment of starting the
deployment may affect the availability of the applications during any new
deployment and in the recovery of any failure. It would be better if we can
work on the application to make it start in less than 1 minute to be able to
have less downtime if it occurred.

While not being a strict technical dependency (or even problem), it is considered
a good practice to build small containers that start up in a very short time.
This will help Kubernetes spin application or service instances up and down
quickly, depending on demand, using the deployment strategy[1] defined.

A service that takes very long to start needs to have more parallel instances
continuously running to mitigate possible breaks or service degradation, since
Kubernetes cannot start up new instances fast enough, should a problem occur.

An ideal container-based application should follow the 12-Factor App principles[2],
using smaller, decoupled components. While not all of these are achievable
under all circumstances, these principles should guide refactoring efforts
and strategies.

References:
1. [Kubernetes Deployment Strategies](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/#strategy)
2. [The Twelve-Factor App](https://12factor.net/)
