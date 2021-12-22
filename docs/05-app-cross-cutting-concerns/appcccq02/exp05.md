# Configuration files built into the application and enabled using system properties at runtime

<div class="risk-rounded-box medium">Medium</div>

topic for the question **How is the application configured?**.

One of the principles of a container-based application design is the image
immutability principle[1]. This principle means that a containerized application
is immutable, and once built are not expected to change between different
environments. In fact the container will require an external configuration
mechanism to adapt it across environments, rather than creating or modifying
per environment.

Compiling the container image including configuration files and enabling by
system properties at runtime could be done in a container orchestration
platform, such as Kubernetes, however it will add some complexity in
deployment process. It will require defining environment-deployment processes
to enable/disable the system properties accordingly. Adding all the
environment configuration in the container image could add some extra operations
and it could have effects when debugging or operating the application.

Kubernetes provides different mechanisms out-of-the-box[2] to achieve this
principle.

As the application could run on Kubernetes, this risk is marked as “Medium”
in order to address best approaches.

References:
[1. Principles of container-based application design - Image Immutability Principle](https://www.redhat.com/en/resources/cloud-native-container-design-whitepaper)
[2. Configure a Pod to Use a ConfigMap](https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-configmap/)
