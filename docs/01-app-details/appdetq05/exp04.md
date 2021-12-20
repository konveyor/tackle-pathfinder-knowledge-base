# 1-7 days

**Risk Level**: Medium

A Container orchestration platform, such as Kubernetes, provides tools and capabilities to identify the health and status of an application, in order to recover the application quickly. The application must be ready to recover in a short period of time (a few minutes). Longer periods of recovery are not aligned with the best practices in container environments, because they will have huge impacts on the general performance of the application, and the platform. This 
The current recovery time represents a “Medium” risk because it is not feasible to manage days as periods of recovery in a container orchestration platform. The process to recover the application should be reviewed before moving to the new container orchestration platform.
Software Delivery Performance [1] defines the Mean Time to Recover metric as the average time that an application will take to revolver from any failure. Measuring this metric we could define new processes to check the health or status of the application in production. In the end, this could help the organization to be more reactive to issues and errors in a short period of time.
Kubernetes includes features to check and verify the health and status of the application [2], aligned with new value streams based on CICD pipelines, optimization resources, automating processes and so on that could have a huge impact on that metric.
Using tools like Pelorus [3] will help to get that metrics, among others, to optimize the value stream of the application.

References:
[1] Exploring a Metrics-Driven approach to transformation
[2] Kubernetes - Configure Liveness, Readiness and Startup Probes
[3] Pelorus