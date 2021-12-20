# Massive monolith (high memory and CPU usage), singleton deployment, vertical scale only

**Risk Level**: Medium

The application has been designed in a traditional, monolithic architecture
with a restriction about the number of instances running. The application
is only available to run with a single instance.

While it is possible to deploy monolithic applications as containers, several
of the benefits of using a container orchestration platform remain unused [1]:

* Setting the deployment with a single replica will not allow to scale the
application and it could affect the deployment process with some downtime periods.
* Smaller components can be scaled independently, providing effective resource
usage, elasticity and leveraging autoscaling functionality brought by the platform.
* Smaller components can be updated independently, if done right - allowing
for faster turnaround times and higher degrees of deployment and test automation
* Smaller components typically have a faster startup time, making rescheduling,
autoscaling and other Kubernetes events more effective.

An ideal container-based application should follow the 12-Factor App principles [2],
using smaller, decoupled components. While not all of these are achievable under
all circumstances, these principles should guide refactoring efforts and strategies.

References:
[1] What is Kubernetes?
[2] The Twelve-Factor App
