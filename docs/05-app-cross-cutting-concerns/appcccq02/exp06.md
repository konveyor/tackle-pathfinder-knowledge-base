# Configuration retrieved from an external server

<div class="risk-rounded-box medium">Medium</div>

topic for the question **How is the application configured?**.

Examples: Spring Cloud Config Server, HashiCorp Consul

Using an external config server is possible and not an anti-pattern[1], however
has the disadvantage of having an external component that is required for
your application to run[2].

An alternative to this external dependency is the usage of Kubernetes ConfigMaps[3],
that (being YAML-files) can also be versioned in e.g. git, enforcing an
“everything as code” approach, meaning version-controlling all components that
an application and its supporting infrastructure is composed of.

When moving to Kubernetes, it is recommended to evaluate the value of ConfigMaps
and if using these can satisfy all the requirements that the application may have,
reducing operational and maintenance complexity.

References:
[1. Spring Boot Microservices on Red Hat OpenShift Container Platform](https://access.redhat.com/documentation/en-us/reference_architectures/2017/html-single/spring_boot_microservices_on_red_hat_openshift_container_platform_3/index)
[2. Spring on Kubernetes](https://cloud.redhat.com/learn/topics/spring)
[3. Configure a Pod to Use a ConfigMap](https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-configmap/)
