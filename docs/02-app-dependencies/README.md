# Application Dependencies

This document includes a set of recommendations to be used as standard comments to add in Pathfinder reports when some of
the topics are identified as `High` or `Medium` risks. These recommendations are based on field experience, standard patterns
and best practices in Kubernetes space and Cloud Native applications.

This part is focused in Application Dependencies space.

## Questionnaire

Set of the current questions of Tackle inventory in this space:

* [Does the application require specific hardware?](./02-app-dependencies/appdepq01/README.md)
  * [Unknown](./02-app-dependencies/appdepq01/exp01.md)
  * [Requires CPU that is not supported by Red Hat (High)](./02-app-dependencies/appdepq01/exp02.md)
  * [Requires custom or legacy hardware (example: USB device) (High)](./02-app-dependencies/appdepq01/exp03.md)
  * [Requires specific computer hardware (examples: GPUs, RAM, HDDs) (Medium)](./02-app-dependencies/appdepq01/exp04.md)
  * Requires CPU that is supported by Red Hat (Low)
 
* [What operating system does the application require?](./02-app-dependencies/appdepq02/README.md)
  * [Unknown](./02-app-dependencies/appdepq02/exp01.md)
  * [Operating system that is not compatible with OpenShift Container Platform (examples: OS X, AIX, Unix, Solaris) (High)](./02-app-dependencies/appdepq02/exp02.md)
  * [Linux with custom kernel drivers or a specific kernel version (High)](./02-app-dependencies/appdepq02/exp03.md)
  * [Linux with custom capabilities (examples: seccomp, root access) (Medium)](./02-app-dependencies/appdepq02/exp01.md)
  * [Microsoft Windows (Medium)](./02-app-dependencies/appdepq02/exp05.md)
  * Standard Linux distribution (Low)
 
* [Does the vendor provide support for a third-party component running in a container?](./02-app-dependencies/appdepq03/README.md)
  * [Unknown](./02-app-dependencies/appdepq03/exp01.md)
  * [Not recommended to run the component in a container (High)](./02-app-dependencies/appdepq03/exp02.md)
  * [No vendor support for containers (High)](./02-app-dependencies/appdepq03/exp03.md)
  * [Vendor supports containers but with limitations (examples: functionality is restricted, component has not been tested) (Medium)](./02-app-dependencies/appdepq03/exp04.md)
  * [Vendor supports their application running in containers but you must build your own images (Medium)](./02-app-dependencies/appdepq03/exp05.md)
  * Vendor fully supports containers, provides certified images (Low)
  * No third-party components required (Low)
 
* [Incoming/northbound dependencies](./02-app-dependencies/appdepq04/README.md)
  * [Unknown](./02-app-dependencies/appdepq04/exp01.md)
  * [Dependencies are difficult or expensive to change because they are legacy or third-party (High)](./02-app-dependencies/appdepq04/exp02.md)
  * [Many dependencies exist, can be changed but the process is expensive and time-consuming (Medium)](./02-app-dependencies/appdepq04/exp03.md)
  * Many dependencies exist, can be changed because the systems are internally managed (Low)
  * Internal dependencies only (Low)
  * No incoming/northbound dependencies (Low)
 
* [Outgoing/southbound dependencies](./02-app-dependencies/appdepq05/README.md)
  * [Unknown](./02-app-dependencies/appdepq05/exp01.md)
  * [Dependency availability only verified when application is processing traffic (High)](./02-app-dependencies/appdepq05/exp02.md)
  * [Dependencies require a complex and strict startup order (Medium)](./02-app-dependencies/appdepq05/exp03.md)
  * [Application not ready until dependencies are verified available (Medium)](./02-app-dependencies/appdepq05/exp04.md)
  * Limited processing available if dependencies are unavailable (Low)
  * No outgoing/southbound dependencies (Low)
