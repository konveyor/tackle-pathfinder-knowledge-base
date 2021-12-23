# Sensitive to latency

<div class="risk-rounded-box medium">Medium</div>

topic for the question **What best describes the application's runtime characteristics?**.

Kubernetes uses a Scheduler[1] to determine placement of Pods onto Nodes based
on availability of compute resources and even distribution of load across the
cluster (based on node capabilities). To allow for some headroom without reserving
worker nodes exclusively for some applications, usage of affinity-rules or
anti-affinity rules[2] for certain (high burstable) pods within the application
might be advisable. 

References:
1. [Kubernetes Scheduler](https://kubernetes.io/docs/concepts/scheduling-eviction/kube-scheduler/)
2. [Assigning Pods to Nodes](https://kubernetes.io/docs/concepts/scheduling-eviction/kube-scheduler/)
