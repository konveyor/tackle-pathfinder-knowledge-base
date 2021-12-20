# Application Cross Cutting Concerns

This document includes a set of recommendations to be used as standard comments to add in Pathfinder reports when some of
the topics are identified as `High` or `Medium` risks. These recommendations are based on field experience, standard patterns
and best practices in Kubernetes space and Cloud Native applications.

This part is focused in Application Cross Cutting Concerns space.

## Questionnaire

Set of the current questions of Tackle inventory in this space:

* [How is the application tested?](./05-app-cross-cutting-concerns/appcccq01/README.md)
  * [Unknown](./05-app-cross-cutting-concerns/appcccq01/exp01.md)
  * [No testing or minimal manual testing only (High)](./05-app-cross-cutting-concerns/appcccq01/exp02.md)
  * [Minimal automated testing, focused on the user interface (Medium)](./05-app-cross-cutting-concerns/appcccq01/exp03.md)
  * [Some automated unit and regression testing, basic CI/CD pipeline testing; modern test practices are not followed (Medium)](./05-app-cross-cutting-concerns/appcccq01/exp04.md)
  * Highly repeatable automated testing (examples: unit, integration, smoke tests) before deploying to production; modern test practices are followed (Low)
  * Chaos engineering approach, constant testing in production (example: A/B testing + experimentation) (Low)
 
* [How is the application configured?](./05-app-cross-cutting-concerns/appcccq02/README.md)
  * [Unknown](./05-app-cross-cutting-concerns/appcccq02/exp01.md)
  * [Configuration files compiled during installation and configured using a user interface (High)](./05-app-cross-cutting-concerns/appcccq02/exp02.md)
  * [Configuration files are stored externally (example: in a database) and accessed using specific environment keys (examples: host name, IP address) (High)](./05-app-cross-cutting-concerns/appcccq02/exp03.md)
  * [Multiple configuration files in multiple file system locations (Medium)](./05-app-cross-cutting-concerns/appcccq02/exp04.md)
  * [Configuration files built into the application and enabled using system properties at runtime (Medium)](./05-app-cross-cutting-concerns/appcccq02/exp05.md)
  * [Configuration retrieved from an external server (examples: Spring Cloud Config Server, HashiCorp Consul) (Medium)](./05-app-cross-cutting-concerns/appcccq02/exp06.md)
  * Configuration loaded from files in a single configurable location; environment variables used (Low)
 
* [How does the application acquire security keys or certificates?](./05-app-cross-cutting-concerns/appcccq03/README.md)
  * [Unknown](./05-app-cross-cutting-concerns/appcccq03/exp01.md)
  * [Hardware security modules or encryption devices (High)](./05-app-cross-cutting-concerns/appcccq03/exp02.md)
  * [Keys/certificates bound to IP addresses and generated at runtime for each application instance (High)](./05-app-cross-cutting-concerns/appcccq03/exp03.md)
  * [Keys/certificates compiled into the application (Medium)](./05-app-cross-cutting-concerns/appcccq03/exp04.md)
  * [Loaded from a shared disk (Medium)](./05-app-cross-cutting-concerns/appcccq03/exp04.md)
  * [Retrieved from an external server (examples: HashiCorp Vault, CyberArk Conjur) (Medium)](./05-app-cross-cutting-concerns/appcccq03/exp05.md)
  * Loaded from files (Low)
  * Not required (Low)
 
* [How is the application deployed?](./05-app-cross-cutting-concerns/appcccq04/README.md)
  * [Unknown](./05-app-cross-cutting-concerns/appcccq04/exp01.md)
  * [Manual deployment using a user interface (High)](./05-app-cross-cutting-concerns/appcccq04/exp02.md)
  * [Manual deployment with some automation (High)](./05-app-cross-cutting-concerns/appcccq04/exp03.md)
  * [Simple automated deployment scripts (Medium)](./05-app-cross-cutting-concerns/appcccq04/exp04.md)
  * [Automated deployment with manual intervention or complex promotion through pipeline stages (Medium)](./05-app-cross-cutting-concerns/appcccq04/exp05.md)
  * Automated deployment with a full CI/CD pipeline, minimal intervention for promotion through pipeline stages (Low)
  * Fully automated (GitOps), blue-green, or canary deployment (Low)
 
* [Where is the application deployed?](./05-app-cross-cutting-concerns/appcccq05/README.md)
  * [Unknown](./05-app-cross-cutting-concerns/appcccq05/exp01.md)
  * [Bare metal server (Low)](./05-app-cross-cutting-concerns/appcccq05/exp02.md)
  * Virtual machine (examples: Red Hat Virtualization, VMware) (Low)
  * Private cloud (example: Red Hat OpenStack Platform) (Low)
  * Public cloud provider (examples: Amazon Web Services, Microsoft Azure, Google Cloud Platform) (Low)
  * [Platform as a service (examples: Heroku, Force.com, Google App Engine) (Medium)](./05-app-cross-cutting-concerns/appcccq05/exp06.md)
  * Hybrid cloud (public and private cloud providers) (Low)
  * [Other. Specify in the comments field (Medium)](./05-app-cross-cutting-concerns/appcccq05/exp08.md)
 
* [How mature is the containerization process, if any?](./05-app-cross-cutting-concerns/appcccq06/README.md)
  * [Unknown](./05-app-cross-cutting-concerns/appcccq06/exp01.md)
  * [Application runs in a container on a laptop or desktop (High)](./05-app-cross-cutting-concerns/appcccq06/exp02.md)
  * [Some experience with containers but not yet fully defined (High)](./05-app-cross-cutting-concerns/appcccq06/exp03.md)
  * Proficient with containers and container platforms (examples: Swarm, Kubernetes) (Low)
  * Application containerization has not yet been attempted (Low)
