# Application Architecture

This questionnaire includes a set of questions to check and identify the current
status of the application in areas such as:

- Resilience
- Clustering
- Communications

## Questionnaire

* [How resilient is the application? How well does it recover from outages and restarts?](./03-app-architecture/apparcq01/README.md)
  * [Unknown](./03-app-architecture/apparcq01/exp01.md)<div class="risk-box unknown"></div>
  * [Application cannot be restarted cleanly after failure, requires manual intervention](./03-app-architecture/apparcq01/exp02.md)<div class="risk-box high"></div>
  * [Application fails when a southbound dependency is unavailable and does not recover automatically](./03-app-architecture/apparcq01/exp03.md)<div class="risk-box high"></div>
  * [Application functionality is limited when a dependency is unavailable but recovers when the dependency is available](./03-app-architecture/apparcq01/exp04.md)<div class="risk-box medium"></div>
  * Application employs resilient architecture patterns<div class="risk-box low"></div>
  * Application containers are randomly terminated to test resiliency; chaos engineering principles are followed<div class="risk-box low"></div>
 
* [How does the external world communicate with the application?](./03-app-architecture/apparcq02/README.md)
  * [Unknown](./03-app-architecture/apparcq02/exp01.md)<div class="risk-box unknown"></div>
  * [Non-TCP/IP protocols](./03-app-architecture/apparcq02/exp02.md)<div class="risk-box high"></div>
  * [TCP/IP, with host name or IP address encapsulated in the payload](./03-app-architecture/apparcq02/exp03.md)<div class="risk-box high"></div>
  * [TCP/UDP without host addressing](./03-app-architecture/apparcq02/exp04.md)<div class="risk-box medium"></div>
  * TCP/UDP encapsulated, using TLS with SNI header<div class="risk-box low"></div>
  * HTTP/HTTPS<div class="risk-box low"></div>
 
* [How does the application manage its internal state?](./03-app-architecture/apparcq03/README.md)
  * [Unknown](./03-app-architecture/apparcq03/exp01.md)<div class="risk-box unknown"></div>
  * [Application components use shared memory within a pod](./03-app-architecture/apparcq03/exp02.md)<div class="risk-box medium"></div>
  * [State is managed externally by another product](./03-app-architecture/apparcq03/exp03.md)<div class="risk-box medium"></div>
  * [State maintained in non-shared, non-ephemeral storage](./03-app-architecture/apparcq03/exp04.md)<div class="risk-box medium"></div>
  * Disk shared between application instances<div class="risk-box low"></div>
  * Stateless or ephemeral container storage<div class="risk-box low"></div>
 
* [How does the application handle service discovery?](./03-app-architecture/apparcq04/README.md)
  * [Unknown](./03-app-architecture/apparcq04/exp01.md)<div class="risk-box unknown"></div>
  * [Uses technologies that are not compatible with Kubernetes](./03-app-architecture/apparcq04/exp02.md)<div class="risk-box high"></div>
  * [Requires an application or cluster restart to discover new service instances](./03-app-architecture/apparcq04/exp03.md)<div class="risk-box high"></div>
  * [Uses technologies that are compatible with Kubernetes but require specific libraries or services](./03-app-architecture/apparcq04/exp04.md)<div class="risk-box medium"></div>
  * Uses Kubernetes DNS name resolution<div class="risk-box low"></div>
  * Does not require service discovery<div class="risk-box low"></div>
 
* [How is the application clustering managed?](./03-app-architecture/apparcq05/README.md)
  * [Unknown](./03-app-architecture/apparcq05/exp01.md)<div class="risk-box unknown"></div>
  * [Manually configured clustering](./03-app-architecture/apparcq05/exp02.md)<div class="risk-box high"></div>
  * [Managed by an external off-PaaS cluster manager](./03-app-architecture/apparcq05/exp03.md)<div class="risk-box high"></div>
  * Managed by an application runtime that is compatible with Kubernetes<div class="risk-box low"></div>
  * No cluster management required<div class="risk-box low"></div>
