# Linux with custom capabilities

<div class="risk-rounded-box medium">Medium</div>

topic for the question **What operating system does the application require?**.

Examples: seccomp, root access

For security reasons, container orchestration platforms, such as Kubernetes,
prohibit the use of containers running as root (or any other privileged user,
for that matter). While this can be enabled, it is strongly discouraged as it
is considered an anti-pattern[1].

If the requirement stems from using privileged ports (<1024), container images
can be built that use non-privileged ports and map those ports in the service
definition.

In Kubernetes, a pod (container) exposes ports only on an internal network.
These are load-balanced by Kubernetes services[2], providing endpoints for
consumption of provided ports, regardless of how many instances of a pod
are running in this deployment.

For Kubernetes Cluster internal communication, these internal service addresses
should be used. If these services need to be consumed / addressable from outside
the cluster, a Route can be assigned to a service, making it accessible from the
outside world.

These paradigms should be considered when moving an application on Kubernetes.

For ease of consumption, there are e.g. NGINX container images [3] and more
readily available from the Red Hat Container Catalog.

These will also expose ports above 1024 (on the container level) that can be
mapped to e.g. 80/443 on the service/route level.

Generally, it is recommended to use Red Hat supported images (as Red Hat will
also watch CVE exposures, bugfix updates, etc) or base custom images on RHEL
or UBI (Universal Base Images[4]) and use an ImageStream [5] to be notified
if an updated version of the base image (e.g. due to a fixed CVE) is
available - or even trigger a build process and automated deployment.

References:
[1. Just say no to root (in containers)](https://opensource.com/article/18/3/just-say-no-root-containers)
[2. Kubernetes Services](https://kubernetes.io/docs/concepts/services-networking/service/)
[3. NGINX Image](https://catalog.redhat.com/software/containers/ubi8/nginx-118/5f521a6f9dd2d5ca7158e5dc)
[4. Universal Base Images](https://catalog.redhat.com/software/containers/ubi8/nginx-118/5f521a6f9dd2d5ca7158e5dc)
[5. Managing image streams](https://docs.openshift.com/container-platform/4.8/openshift_images/image-streams-manage.html)
