# Not tracked

<div class="risk-rounded-box high">High</div>

topic for the question **What is the application's mean time to recover (MTTR) from failure in a production environment?**.

Not tracking this time represents a lack of improvement in the application life
cycle in general, but could have an impact on the benefits for this application
in a container orchestration platform, such as Kubernetes.

Software Delivery Performance[1] defines the Mean Time to Recover metric as
the average time that an application will take to revolver from any failure.
Measuring this metric we could define new processes to check the health or status
of the application in production. In the end, this could help the organization to
be more reactive to issues and errors in a short period of time.

Kubernetes includes features to check and verify the health and status of the
application[2], aligned with new value streams based on CICD pipelines, optimization
resources, automating processes and so on that could have a huge impact on that metric.

Missing this metric at all means a “High” risk because we could not identify how
this application could be restored until issues or errors in the container
orchestration platform. It should check or review the main benefits for this
application on the new platform.

Using tools like Pelorus[3] will help to get that metrics, among others, to
optimize the value stream of the application.

References:
[1. Exploring a Metrics-Driven approach to transformation](https://cloud.redhat.com/blog/exploring-a-metrics-driven-approach-to-transformation)
[2. Kubernetes - Configure Liveness, Readiness and Startup Probes](https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/)
[3. Pelorus](https://pelorus.readthedocs.io/en/latest/#software-delivery-performance-as-an-outcome)
