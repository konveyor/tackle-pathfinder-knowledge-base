# Uses technologies that are compatible with Kubernetes but require specific libraries or services 

<div class="risk-rounded-box medium">Medium</div>

topic for the question **How does the application handle service discovery?**.

These technologies, and others similar, are compatible with a container orchestration
platform, such as Kubernetes, however they add additional complexity and match with
underlying services provided by the container orchestration platform. So, they need
to be adapted to the Kubernetes paradigm to avoid conflicts and to reduce overlapping
between them.

Given the current situation, if you don’t have much experience with the “Service”
paradigms[1] in Kubernetes that provide DNS-based service discovery, load balancing
and can even provide advanced features such as Canary Deployments, A/B Testing and
more. Furthermore, OpenShift provides built-in Service Mesh (consisting of Istio,
Kiali, Jaeger, Multus and more)[2],[3],[4].

Services are accessible from inside the Kubernetes Cluster and are assigned
internal IPs. If a service (backed by 1 to n Pods) needs to be exposed to the
outside world (outside of the OpenShift Cluster), a Route is assigned to a service.

Using this paradigm (as noted above) A/B testing, Canary Deployments and
Blue/Green Deployments are possible

References:
[1. Kubernetes - Service](https://kubernetes.io/docs/concepts/services-networking/service/)
[2. Using route-based deployment strategies](https://docs.openshift.com/container-platform/4.8/applications/deployments/route-based-deployment-strategies.html)
[3. Configuring ingress cluster traffic using an Ingress Controller](https://docs.openshift.com/container-platform/4.8/networking/configuring_ingress_cluster_traffic/configuring-ingress-cluster-traffic-ingress-controller.html)
[4. Understanding Red Hat OpenShift Service Mesh](https://docs.openshift.com/container-platform/4.8/service_mesh/v1x/ossm-architecture.html)
