# Between once a month and once every 6 months

<div class="risk-rounded-box medium">Medium</div>

topic for the question **How often is the application deployed to production?**.

If a low deployment frequency is caused by lack of build automation, testing
complexity or complex processes that need to be followed, it is considered a
risk that should be looked into, focussing on improvement. Sometimes it is simply
the result of releases being tied to business requirements or change requests.

Software Delivery Performance[1] defines the Deployment Frequency metric as the
number of times the code is deployed into production, and Mean Time to Recover[2]
metric as how long it takes the application to recover from failures in production.
Measuring both metrics we could define a new deployment process to have the latest
changes in production faster and a reduced time to recover from failures. In the end,
this could help the organization to test and verify new features in production
without waiting a long period of time.

Kubernetes does not include specific features or capabilities focused to optimize
that metric, however the platform itself allows to create new value streams based
on CICD pipelines, optimization resources, automating processes and so on that
could have a huge impact on that metric.

Using tools like Pelorus[3] will help to get that metrics, among others, to
optimize the value stream of the application.

References:
[1. Exploring a Metrics-Driven approach to transformation](https://cloud.redhat.com/blog/exploring-a-metrics-driven-approach-to-transformation)
[2. Mean time to recovery](https://en.wikipedia.org/wiki/Mean_time_to_recovery)
[3. Pelorus](https://pelorus.readthedocs.io/en/latest/#software-delivery-performance-as-an-outcome)
