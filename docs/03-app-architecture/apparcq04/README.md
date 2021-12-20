# How does the application handle service discovery?

Answers, Risk and Explanations:

* [Unknown](./03-app-architecture/apparcq04/exp01.md)
* [Uses technologies that are not compatible with Kubernetes (examples: hardcoded IP addresses, custom cluster manager) (High)](./03-app-architecture/apparcq04/exp02.md)
* [Requires an application or cluster restart to discover new service instances (High)](./03-app-architecture/apparcq04/exp03.md)
* [Uses technologies that are compatible with Kubernetes but require specific libraries or services (examples: HashiCorp Consul, Netflix Eureka) (Medium)](./03-app-architecture/apparcq04/exp04.md)
* Uses Kubernetes DNS name resolution (Low)
* Does not require service discovery (Low)
