# Requires an application or cluster restart to discover new service instances

<div class="risk-rounded-box high">High</div>

topic for the question **How does the application handle service discovery?**.

The application is currently deployed in VMs or bare metal, using a traditional,
properties-file based configuration paradigm, including the locations/addresses
of other internal or external services. Any change requires an application
restart (manually or automatically).

In a container orchestration platform, such as Kubernetes, this is not feasible,
since containers will change their IPs when being rescheduled to other nodes,
being restarted because of Kubernetes events or deployment requirements
(automatically spawning new instances if needed), etc.

To accomplish this, Kubernetes uses DNS-based name resolution of Services that
are being backed by one or more Pods (groups of containers)[1],[2].

This enables DNS-based service discovery, load balancing and can even provide
advanced features such as Canary Deployments, A/B Testing and more. Furthermore,
OpenShift provides built-in Service Mesh (consisting of Istio, Kiali, Jaeger,
Multus and more)[3],[4],[5].

Services are accessible from inside the Kubernetes and are assigned internal IPs.
If a service (backed by 1 to n Pods) needs to be exposed to the outside world
(outside of the OpenShift Cluster), a Route is assigned to a service[2].:

Using this paradigm (as noted above) A/B testing, Canary Deployments and
Blue/Green Deployments are possible.

References:

[1. Kubernetes - Pod](https://kubernetes.io/docs/concepts/workloads/pods/)
[2. Kubernetes - Service](https://kubernetes.io/docs/concepts/services-networking/service/)
[3. Using route-based deployment strategies](https://docs.openshift.com/container-platform/4.8/applications/deployments/route-based-deployment-strategies.html)
[4. Configuring ingress cluster traffic using an Ingress Controller](https://docs.openshift.com/container-platform/4.8/networking/configuring_ingress_cluster_traffic/configuring-ingress-cluster-traffic-ingress-controller.html)
[5. Understanding Red Hat OpenShift Service Mesh](https://docs.openshift.com/container-platform/4.8/service_mesh/v1x/ossm-architecture.html)
