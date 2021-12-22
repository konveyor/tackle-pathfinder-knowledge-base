# Manual deployment using a user interface

<div class="risk-rounded-box high">High</div>

topic for the question **How is the application deployed?**.

Deploying an application on Kubernetes requires a higher degree of automation
than is currently available. Technically, an application can be deployed manually,
configuration can be adapted manually, but that is an antipattern in a container
orchestration environment.

One of the key advantages of running an application in a container orchestration
platform is the ability to roll out new versions without service interruption,
roll back deployments to previous versions in case of errors, scale up and down
application components (even automatically) based on load or other metrics.
It is even possible to initiate a new deployment in a test environment,
including automated tests with every code commit, using pipelines[1].
This leads to much higher velocity than in traditional environments.

Additionally, describing deployment characteristics and the desired state of
an application as YAML-files[2] is the prerequisite for higher deployment
quality with less errors and the capability to version deployment attributes
in a version control system, leading to a GitOps approach[3].

This is not possible in case of required manual intervention in an
application deployment.

Therefore, we highlight this as a high risk item that should be amended
during a migration.

References:
[1. Understanding OpenShift pipelines](https://docs.openshift.com/container-platform/4.8/cicd/pipelines/understanding-openshift-pipelines.html)
[2. Kubernetes Deployments](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/)
[3. Introduction to GitOps with OpenShift](https://cloud.redhat.com/blog/introduction-to-gitops-with-openshift)
