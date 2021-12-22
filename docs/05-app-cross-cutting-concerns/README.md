# Application Cross Cutting Concerns

This questionnaire includes a set of questions to check and identify the current
status of the application in areas such as:

- Testing
- Configuration
- Deployment Model

## Questionnaire

* [How is the application tested?](./05-app-cross-cutting-concerns/appcccq01/README.md)
  * [Unknown](./05-app-cross-cutting-concerns/appcccq01/exp01.md)<div class="risk-box unknown"></div>
  * [No testing or minimal manual testing only](./05-app-cross-cutting-concerns/appcccq01/exp02.md)<div class="risk-box high"></div>
  * [Minimal automated testing, focused on the user interface](./05-app-cross-cutting-concerns/appcccq01/exp03.md)<div class="risk-box medium"></div>
  * [Some automated unit and regression testing, basic CI/CD pipeline testing; modern test practices are not followed](./05-app-cross-cutting-concerns/appcccq01/exp04.md)<div class="risk-box medium"></div>
  * Highly repeatable automated testing (examples: unit, integration, smoke tests) before deploying to production; modern test practices are followed<div class="risk-box low"></div>
  * Chaos engineering approach, constant testing in production<div class="risk-box low"></div>
 
* [How is the application configured?](./05-app-cross-cutting-concerns/appcccq02/README.md)
  * [Unknown](./05-app-cross-cutting-concerns/appcccq02/exp01.md)<div class="risk-box unknown"></div>
  * [Configuration files compiled during installation and configured using a user interface](./05-app-cross-cutting-concerns/appcccq02/exp02.md)<div class="risk-box high"></div>
  * [Configuration files are stored externally (example: in a database) and accessed using specific environment keys](./05-app-cross-cutting-concerns/appcccq02/exp03.md)<div class="risk-box high"></div>
  * [Multiple configuration files in multiple file system locations](./05-app-cross-cutting-concerns/appcccq02/exp04.md)<div class="risk-box medium"></div>
  * [Configuration files built into the application and enabled using system properties at runtime](./05-app-cross-cutting-concerns/appcccq02/exp05.md)<div class="risk-box medium"></div>
  * [Configuration retrieved from an external server](./05-app-cross-cutting-concerns/appcccq02/exp06.md)<div class="risk-box medium"></div>
  * Configuration loaded from files in a single configurable location; environment variables used<div class="risk-box low"></div>
 
* [How does the application acquire security keys or certificates?](./05-app-cross-cutting-concerns/appcccq03/README.md)
  * [Unknown](./05-app-cross-cutting-concerns/appcccq03/exp01.md)<div class="risk-box unknown"></div>
  * [Hardware security modules or encryption devices](./05-app-cross-cutting-concerns/appcccq03/exp02.md)<div class="risk-box high"></div>
  * [Keys/certificates bound to IP addresses and generated at runtime for each application instance](./05-app-cross-cutting-concerns/appcccq03/exp03.md)<div class="risk-box high"></div>
  * [Keys/certificates compiled into the application](./05-app-cross-cutting-concerns/appcccq03/exp04.md)<div class="risk-box medium"></div>
  * [Loaded from a shared disk](./05-app-cross-cutting-concerns/appcccq03/exp05.md)<div class="risk-box medium"></div>
  * [Retrieved from an external server](./05-app-cross-cutting-concerns/appcccq03/exp06.md)<div class="risk-box medium"></div>
  * Loaded from files<div class="risk-box low"></div>
  * Not required<div class="risk-box low"></div>
 
* [How is the application deployed?](./05-app-cross-cutting-concerns/appcccq04/README.md)
  * [Unknown](./05-app-cross-cutting-concerns/appcccq04/exp01.md)<div class="risk-box unknown"></div>
  * [Manual deployment using a user interface](./05-app-cross-cutting-concerns/appcccq04/exp02.md)<div class="risk-box high"></div>
  * [Manual deployment with some automation](./05-app-cross-cutting-concerns/appcccq04/exp03.md)<div class="risk-box high"></div>
  * [Simple automated deployment scripts](./05-app-cross-cutting-concerns/appcccq04/exp04.md)<div class="risk-box medium"></div>
  * [Automated deployment with manual intervention or complex promotion through pipeline stages](./05-app-cross-cutting-concerns/appcccq04/exp05.md)<div class="risk-box medium"></div>
  * Automated deployment with a full CI/CD pipeline, minimal intervention for promotion through pipeline stages<div class="risk-box low"></div>
  * Fully automated (GitOps), blue-green, or canary deployment<div class="risk-box low"></div>
 
* [Where is the application deployed?](./05-app-cross-cutting-concerns/appcccq05/README.md)
  * [Unknown](./05-app-cross-cutting-concerns/appcccq05/exp01.md)<div class="risk-box unknown"></div>
  * [Bare metal server](./05-app-cross-cutting-concerns/appcccq05/exp02.md)<div class="risk-box low"></div>
  * Virtual machine<div class="risk-box low"></div>
  * Private cloud<div class="risk-box low"></div>
  * Public cloud provider<div class="risk-box low"></div>
  * [Platform as a Service](./05-app-cross-cutting-concerns/appcccq05/exp06.md)<div class="risk-box medium"></div>
  * Hybrid cloud<div class="risk-box low"></div>
  * [Others](./05-app-cross-cutting-concerns/appcccq05/exp08.md)<div class="risk-box medium"></div>
 
* [How mature is the containerization process, if any?](./05-app-cross-cutting-concerns/appcccq06/README.md)
  * [Unknown](./05-app-cross-cutting-concerns/appcccq06/exp01.md)<div class="risk-box unknown"></div>
  * [Application runs in a container on a laptop or desktop](./05-app-cross-cutting-concerns/appcccq06/exp02.md)<div class="risk-box high"></div>
  * [Some experience with containers but not yet fully defined](./05-app-cross-cutting-concerns/appcccq06/exp03.md)<div class="risk-box high"></div>
  * Proficient with containers and container platforms<div class="risk-box low"></div>
  * Application containerization has not yet been attempted<div class="risk-box low"></div>
