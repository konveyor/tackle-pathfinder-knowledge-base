# Not tracked

<div class="risk-rounded-box high">High</div>

topic for the question **How much time passes from when code is committed until the application is deployed to production?**.

Not tracking this time represents a lack of improvement in the application life
cycle in general, but could have an impact on the benefits for this application
in a container orchestration platform, such as Kubernetes.

Software Delivery Performance[1] defines the Lead Time metric as the total time
it takes for work to move through the value stream, from the moment the work is
requested to the time it’s delivered. Optimizing this value the value stream of
the application could impact successfully in the general overview of the application.

Kubernetes does not include specific features or capabilities focused to optimize
that metric, however the platform itself allows to create new value streams based
on CICD pipelines, optimization resources, automating processes and so on that could
have a huge impact on that metric.

Missing this metric at all means a “High” risk because we could not identify how
this application could be improved in the container orchestration platform. It
should check or review the main benefits for this application on the new platform.

Using tools like Pelorus [2] will help to get that metrics, among others, to
optimize the value stream of the application.

References:
1. [Exploring a Metrics-Driven approach to transformation](https://cloud.redhat.com/blog/exploring-a-metrics-driven-approach-to-transformation)
2. [Pelorus](https://pelorus.readthedocs.io/en/latest/#software-delivery-performance-as-an-outcome)
