# Manually configured clustering

<div class="risk-rounded-box high">High</div>

topic for the question **How is the application clustering managed?**.

Examples: static clusters

In a container orchestration platform, such as Kubernetes, containers are considered
ephemeral and will come and go dynamically, either triggered by human interaction by
administrators or as part of Kubernetes internal automatisms. Therefore, any static
configuration pointing to other cluster members will not work and needs to be changed.

Kubernetes (as a container orchestration platform) provides numerous ways to
maintain a specific target state of an application (for example, a specific number
of instances must be running at any time) and communication between those (via
cluster internal services and service discovery).

To accomplish the latter, Kubernetes uses DNS-based name resolution of Services
that are being backed by one or more Pods (groups of containers)[1].

This enables DNS-based service discovery, load balancing and can even provide
advanced features such as Canary Deployments, A/B Testing and more.
Furthermore, OpenShift provides built-in Service Mesh (consisting of Istio,
Kiali, Jaeger, Multus and more)[2],[3],[4].

Services are accessible from inside the OpenShift Cluster and are assigned
internal IPs. If a service (backed by 1 to n Pods) needs to be exposed to
the outside world (outside of the OpenShift Cluster), a Route is assigned
to a service[3].

Using this paradigm (as noted above) A/B testing, Canary Deployments and
Blue/Green Deployments are possible.

References:
[1. Kubernetes - Service](https://kubernetes.io/docs/concepts/services-networking/service/)
[2. Using route-based deployment strategies](https://docs.openshift.com/container-platform/4.8/applications/deployments/route-based-deployment-strategies.html)
[3. Configuring ingress cluster traffic using an Ingress Controller](https://docs.openshift.com/container-platform/4.8/networking/configuring_ingress_cluster_traffic/configuring-ingress-cluster-traffic-ingress-controller.html)
[4. Understanding Red Hat OpenShift Service Mesh](https://docs.openshift.com/container-platform/4.8/service_mesh/v1x/ossm-architecture.html)
