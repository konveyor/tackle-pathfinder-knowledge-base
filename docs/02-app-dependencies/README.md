# Application Dependencies

This questionnaire includes a set of questions to check and identify the current
status of the application in areas such as:

- Hardware
- Operating System
- Dependencies

## Questionnaire

* [Does the application require specific hardware?](./02-app-dependencies/appdepq01/README.md)
  * [Unknown](./02-app-dependencies/appdepq01/exp01.md)<div class="risk-box unknown"></div>
  * [Requires CPU that is not supported by Red Hat](./02-app-dependencies/appdepq01/exp02.md)<div class="risk-box high"></div>
  * [Requires custom or legacy hardware](./02-app-dependencies/appdepq01/exp03.md)<div class="risk-box high"></div>
  * [Requires specific computer hardware](./02-app-dependencies/appdepq01/exp04.md)<div class="risk-box medium"></div>
  * Requires CPU that is supported by Red Hat<div class="risk-box low"></div>
 
* [What operating system does the application require?](./02-app-dependencies/appdepq02/README.md)
  * [Unknown](./02-app-dependencies/appdepq02/exp01.md)<div class="risk-box unknown"></div>
  * [Operating system that is not compatible with OpenShift Container Platform](./02-app-dependencies/appdepq02/exp02.md)<div class="risk-box high"></div>
  * [Linux with custom kernel drivers or a specific kernel version](./02-app-dependencies/appdepq02/exp03.md)<div class="risk-box high"></div>
  * [Linux with custom capabilities](./02-app-dependencies/appdepq02/exp01.md)<div class="risk-box medium"></div>
  * [Microsoft Windows](./02-app-dependencies/appdepq02/exp05.md)<div class="risk-box medium"></div>
  * Standard Linux distribution<div class="risk-box low"></div>
 
* [Does the vendor provide support for a third-party component running in a container?](./02-app-dependencies/appdepq03/README.md)
  * [Unknown](./02-app-dependencies/appdepq03/exp01.md)<div class="risk-box unknown"></div>
  * [Not recommended to run the component in a container](./02-app-dependencies/appdepq03/exp02.md)<div class="risk-box high"></div>
  * [No vendor support for containers](./02-app-dependencies/appdepq03/exp03.md)<div class="risk-box high"></div>
  * [Vendor supports containers but with limitations](./02-app-dependencies/appdepq03/exp04.md)<div class="risk-box medium"></div>
  * [Vendor supports their application running in containers but you must build your own images](./02-app-dependencies/appdepq03/exp05.md)<div class="risk-box medium"></div>
  * Vendor fully supports containers, provides certified images<div class="risk-box low"></div>
  * No third-party components required<div class="risk-box low"></div>
 
* [Incoming/northbound dependencies](./02-app-dependencies/appdepq04/README.md)
  * [Unknown](./02-app-dependencies/appdepq04/exp01.md)<div class="risk-box unknown"></div>
  * [Dependencies are difficult or expensive to change because they are legacy or third-party](./02-app-dependencies/appdepq04/exp02.md)<div class="risk-box high"></div>
  * [Many dependencies exist, can be changed but the process is expensive and time-consuming](./02-app-dependencies/appdepq04/exp03.md)<div class="risk-box medium"></div>
  * Many dependencies exist, can be changed because the systems are internally managed<div class="risk-box low"></div>
  * Internal dependencies only<div class="risk-box low"></div>
  * No incoming/northbound dependencies<div class="risk-box low"></div>
 
* [Outgoing/southbound dependencies](./02-app-dependencies/appdepq05/README.md)
  * [Unknown](./02-app-dependencies/appdepq05/exp01.md)<div class="risk-box unknown"></div>
  * [Dependency availability only verified when application is processing traffic](./02-app-dependencies/appdepq05/exp02.md)<div class="risk-box high"></div>
  * [Dependencies require a complex and strict startup order](./02-app-dependencies/appdepq05/exp03.md)<div class="risk-box medium"></div>
  * [Application not ready until dependencies are verified available](./02-app-dependencies/appdepq05/exp04.md)<div class="risk-box medium"></div>
  * Limited processing available if dependencies are unavailable<div class="risk-box low"></div>
  * No outgoing/southbound dependencies<div class="risk-box low"></div>
