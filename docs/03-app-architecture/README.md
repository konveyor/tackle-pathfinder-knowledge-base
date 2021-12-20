# Application Architecture

This document includes a set of recommendations to be used as standard comments to add in Pathfinder reports when some of
the topics are identified as `High` or `Medium` risks. These recommendations are based on field experience, standard patterns
and best practices in Kubernetes space and Cloud Native applications.

This part is focused in Application Details space.

## Questionnaire

Set of the current questions of Tackle inventory in this space:

* [How resilient is the application? How well does it recover from outages and restarts?](./03-app-architecture/apparcq01/README.md)
  * [Unknown](./03-app-architecture/apparcq01/exp01.md)
  * [Application cannot be restarted cleanly after failure, requires manual intervention (High)](./03-app-architecture/apparcq01/exp02.md)
  * [Application fails when a southbound dependency is unavailable and does not recover automatically (High)](./03-app-architecture/apparcq01/exp03.md)
  * [Application functionality is limited when a dependency is unavailable but recovers when the dependency is available (Medium)](./03-app-architecture/apparcq01/exp04.md)
  * Application employs resilient architecture patterns (examples: circuit breakers, retry mechanisms) (Low)
  * Application containers are randomly terminated to test resiliency; chaos engineering principles are followed (Low)
 
* [How does the external world communicate with the application?](./03-app-architecture/apparcq02/README.md)
  * [Unknown](./03-app-architecture/apparcq02/exp01.md)
  * [Non-TCP/IP protocols (examples: serial, IPX, AppleTalk) (High)](./03-app-architecture/apparcq02/exp02.md)
  * [TCP/IP, with host name or IP address encapsulated in the payload (High)](./03-app-architecture/apparcq02/exp03.md)
  * [TCP/UDP without host addressing (example: SSH) (Medium)](./03-app-architecture/apparcq02/exp04.md)
  * TCP/UDP encapsulated, using TLS with SNI header (Low)
  * HTTP/HTTPS (Low)
 
* [How does the application manage its internal state?](./03-app-architecture/apparcq03/README.md)
  * [Unknown](./03-app-architecture/apparcq03/exp01.md)
  * [Application components use shared memory within a pod (Medium)](./03-app-architecture/apparcq03/exp02.md)
  * [State is managed externally by another product (examples: Zookeeper or Red Hat Data Grid) (Medium)](./03-app-architecture/apparcq03/exp03.md)
  * [State maintained in non-shared, non-ephemeral storage (Medium)](./03-app-architecture/apparcq03/exp04.md)
  * Disk shared between application instances (Low)
  * Stateless or ephemeral container storage (Low)
 
* [How does the application handle service discovery?](./03-app-architecture/apparcq04/README.md)
  * [Unknown](./03-app-architecture/apparcq04/exp01.md)
  * [Uses technologies that are not compatible with Kubernetes (examples: hardcoded IP addresses, custom cluster manager) (High)](./03-app-architecture/apparcq04/exp02.md)
  * [Requires an application or cluster restart to discover new service instances (High)](./03-app-architecture/apparcq04/exp03.md)
  * [Uses technologies that are compatible with Kubernetes but require specific libraries or services (examples: HashiCorp Consul, Netflix Eureka) (Medium)](./03-app-architecture/apparcq04/exp04.md)
  * Uses Kubernetes DNS name resolution (Low)
  * Does not require service discovery (Low)
 
* [How is the application clustering managed?](./03-app-architecture/apparcq05/README.md)
  * [Unknown](./03-app-architecture/apparcq05/exp01.md)
  * [Manually configured clustering (example: static clusters) (High)](./03-app-architecture/apparcq05/exp02.md)
  * [Managed by an external off-PaaS cluster manager (High)](./03-app-architecture/apparcq05/exp03.md)
  * Managed by an application runtime that is compatible with Kubernetes (Low)
  * No cluster management required (Low)
