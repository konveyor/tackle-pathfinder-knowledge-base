# More than 5 minutes

<div class="risk-rounded-box high">High</div>

topic for the question **How long does it take the application to be ready to handle traffic?**.

The time the application takes to be ready from the moment of starting the
deployment may affect the availability of the applications during any new
deployment and in the recovery of any failure. It would be better if we can
work on the application to make it start in less than 1 minute to be able to
have less downtime if it occurred.

Applications with long starting time will have an impact on the user
experience (waiting more time), and it will require more resources (parallel
instances) running to mitigate possible breaks or service degradation. Both
aspects could negatively affect the application life cycle, the general
performance and behaviour of the application.

It is considered a good practice to build small containers that start up
in a very short time. This will help Kubernetes spin application or service
instances up and down quickly, depending on demand, using the
deployment strategy[1] defined.

An ideal container-based application should follow the 12-Factor App principles[2],
using smaller, decoupled components. While not all of these are achievable
under all circumstances, these principles should guide refactoring efforts
and strategies.

References:
1. [Using deployment strategies](https://docs.openshift.com/container-platform/4.8/applications/deployments/deployment-strategies.html)
2. [The Twelve-Factor App](https://12factor.net/)
