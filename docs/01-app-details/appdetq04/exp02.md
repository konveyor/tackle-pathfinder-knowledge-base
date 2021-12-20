# Not tracked

**Risk Level**: High

Not tracking this time represents a lack of improvement in the application life cycle in general, but could have an impact on the benefits for this application in a container orchestration platform, such as Kubernetes. 
Software Delivery Performance [1] defines the Deployment Frequency metric as the number of times the code is deployed into production, and Mean Time to Recover [2] metric as how long it takes the application to recover from failures in production. Measuring both metrics we could define a new deployment process to have the latest changes in production faster and a reduced time to recover from failures. In the end, this could help the organization to test and verify new features in production without waiting a long period of time.
Kubernetes does not include specific features or capabilities focused to optimize that metric, however the platform itself allows to create new value streams based on CICD pipelines, optimization resources, automating processes and so on that could have a huge impact on that metric.

Missing this metric at all means a “High” risk because we could not identify how this application could be deployed faster in the container orchestration platform. It should check or review the main benefits for this application on the new platform.

Using tools like Pelorus [3] will help to get that metrics, among others, to optimize the value stream of the application.

References:
[1] Exploring a Metrics-Driven approach to transformation
[2] Mean time to recovery
[3] Pelorus
