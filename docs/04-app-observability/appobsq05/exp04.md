# 1-2 minutes

<div class="risk-rounded-box medium">Medium</div>

topic for the question **How long does it take the application to be ready to handle traffic?**.

This range of startup time has been marked as “Medium” (so, a possible risk or,
at least area for improvement) because in a container environment, application
startup time is usually aimed to be much less.

While not being a strict technical dependency (or even problem), it is considered
a good practice to build small containers that start up in a very short time.
This will help Kubernetes spin application or service instances up and
down quickly, depending on demand, using the deployment strategy[1] defined.

When Kubernetes reschedules pods to other nodes or restarts pods, the aim is
to have quickly responding pods. However, this can be worked around by
increasing the number of concurrent pods in the deployment configuration[2]
that describes the intended application behaviour and minimum (or exact, maximum)
number of pods of a given type that always need to run.

An ideal container-based application should follow the 12-Factor App principles[3],
using smaller, decoupled components. While not all of these are achievable
under all circumstances, these principles should guide refactoring efforts
and strategies.

References:
[1. Using deployment strategies](https://docs.openshift.com/container-platform/4.8/applications/deployments/deployment-strategies.html)
[2. Deployments Configuration](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/#scaling-a-deployment)
[3. The Twelve-Factor App](https://12factor.net/)
