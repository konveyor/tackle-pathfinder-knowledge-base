# Configuration files compiled during installation and configured using a user interface

<div class="risk-rounded-box high">High</div>

topic for the question **How is the application configured?**.

One of the principles of a container-based application design is the image
immutability principle[1]. This principle means that a containerized
application is immutable, and once built are not expected to change between
different environments. In fact the container will require an external configuration
mechanism to adapt it across environments, rather than creating or modifying per
environment.

Compiling the container image including configuration files, or configuring
using user interfaces with manual process, are far away from the best practices
in a container orchestration platform, such as Kubernetes. Kubernetes provides
different mechanisms out-of-the-box[2] to achieve this principle.

This risk needs to be addressed before deploying any production-grade
services with this gap.

References:
1. [Principles of container-based application design - Image Immutability Principle](https://www.redhat.com/en/resources/cloud-native-container-design-whitepaper)
2. [Configure a Pod to Use a ConfigMap](https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-configmap/)
