# Deterministic and predictable real-time execution or control requirements

**Risk Level**: High

Containers rely on operating system features and do not require a virtualization
layer (hypervisor) that introduces a performance degradation. This capability
allows to co-locate multiple isolated containers on a single node, as well as
to decompose an application into multiple containers distributed across several
nodes. However some applications often require real-time behaviour (i.e: capability
to meet predefined deadlines), but these capabilities are not fully supported by
a container orchestration platform, such as Kubernetes.

Kubernetes allows multiple deployments of topologies[1], based in bare metal hosts,
virtualized or in cloud environments (private, public or hybrid). At the same time
a set of different capabilities such as scheduler[2], taints and tolerations[3],
limits and quotas that could help to set up the best approach to start and execute
containers. However it is important to dig deep into the application requirements
to apply the solution to provide them for the application. This could be somewhat
complex and this is the reason this topic is marked as “High” to be resolved before
going to production.

References:
[1. Kubernetes - Cluster Architecture](https://kubernetes.io/docs/concepts/architecture/)
[2. Kubernetes Scheduler](https://kubernetes.io/docs/concepts/scheduling-eviction/kube-scheduler/)
[3. Kubernetes - Taints and Tolerations](https://kubernetes.io/docs/concepts/scheduling-eviction/taint-and-toleration/)
[4. Kubernetes - Resource Quotas](https://kubernetes.io/docs/concepts/policy/resource-quotas/)
