# Application Details

This questionnaire includes a set of questions to check and identify the current
status of the application in areas such as:

- Development Life cycle
- Support life cycle
- Deployment strategies

## Questionnaire

* [Does the application development team understand and actively develop the application?](./01-app-details/appdetq01/README.md)
  * [Unknown](./01-app-details/appdetq01/exp01.md)<div class="risk-box unknown"></div>
  * [Little knowledge, no development](./01-app-details/appdetq01/exp02.md)<div class="risk-box high"></div>
  * [Maintenance mode, no SME knowledge or adequate documentation available](./01-app-details/appdetq01/exp03.md)<div class="risk-box high"></div>
  * [Maintenance mode, SME knowledge is available](./01-app-details/appdetq01/exp04.md)<div class="risk-box medium"></div>
  * Actively developed, SME knowledge is available<div class="risk-box low"></div>
  * Greenfield application<div class="risk-box low"></div>
 
* [How is the application supported in production?](./01-app-details/appdetq02/README.md)
  * [Unknown](./01-app-details/appdetq02/exp01.md)<div class="risk-box unknown"></div>
  * [External support provider with a ticket-driven escalation process; no inhouse support resources](./01-app-details/appdetq02/exp02.md)<div class="risk-box high"></div>
  * [Separate internal support team, separate from the development team, with little interaction between the teams](./01-app-details/appdetq02/exp03.md)<div class="risk-box high"></div>
  * [Multiple teams provide support using an established escalation model](./01-app-details/appdetq02/exp04.md)<div class="risk-box medium"></div>
  * SRE approach with a knowledgeable and experienced operations team<div class="risk-box low"></div>
  * DevOps approach with the same team building the application and supporting it in production<div class="risk-box low"></div>
 
* [How much time passes from when code is committed until the application is deployed to production?](./01-app-details/appdetq03/README.md)
  * [Unknown](./01-app-details/appdetq03/exp01.md)<div class="risk-box unknown"></div>
  * [Not tracked](./01-app-details/appdetq03/exp02.md)<div class="risk-box high"></div>
  * [More than 6 months](./01-app-details/appdetq03/exp03.md)<div class="risk-box high"></div>
  * [2-6 months](./01-app-details/appdetq03/exp04.md)<div class="risk-box medium"></div>
  * 8-30 days<div class="risk-box low"></div>
  * 1-7 days<div class="risk-box low"></div>
  * Less than 1 day<div class="risk-box low"></div>
 
* [How often is the application deployed to production?](./01-app-details/appdetq04/README.md)
  * [Unknown](./01-app-details/appdetq04/exp01.md)<div class="risk-box unknown"></div>
  * [Not tracked](./01-app-details/appdetq04/exp02.md)<div class="risk-box high"></div>
  * [Less than once every 6 months](./01-app-details/appdetq04/exp03.md)<div class="risk-box high"></div>
  * [Between once a month and once every 6 months](./01-app-details/appdetq04/exp04.md)<div class="risk-box medium"></div>
  * Weekly<div class="risk-box low"></div>
  * Daily<div class="risk-box low"></div>
  * Several times a day<div class="risk-box low"></div>
 
* [What is the application's mean time to recover (MTTR) from failure in a production environment?](./01-app-details/appdetq05/README.md)
  * [Unknown](./01-app-details/appdetq05/exp01.md)<div class="risk-box unknown"></div>
  * [Not tracked](./01-app-details/appdetq05/exp02.md)<div class="risk-box high"></div>
  * [1 month or more](./01-app-details/appdetq05/exp03.md)<div class="risk-box high"></div>
  * [1-7 days](./01-app-details/appdetq05/exp04.md)<div class="risk-box medium"></div>
  * 1-24 hours<div class="risk-box low"></div>
  * Less than 1 hour<div class="risk-box low"></div>
 
* [Does the application have legal and/or licensing requirements?](./01-app-details/appdetq06/README.md)
  * [Unknown](./01-app-details/appdetq06/exp01.md)<div class="risk-box unknown"></div>
  * [Multiple legal and licensing requirements](./01-app-details/appdetq06/exp02.md)<div class="risk-box high"></div>
  * [Licensing requirements](./01-app-details/appdetq06/exp03.md)<div class="risk-box medium"></div>
  * [Legal requirements](./01-app-details/appdetq06/exp04.md)<div class="risk-box medium"></div>
  * None<div class="risk-box low"></div>
 
* [Which model best describes the application architecture?](./01-app-details/appdetq07/README.md)
  * [Unknown](./01-app-details/appdetq07/exp01.md)<div class="risk-box unknown"></div>
  * [Massive monolith, singleton deployment, vertical scale only](./01-app-details/appdetq07/exp02.md)<div class="risk-box medium"></div>
  * [Massive monolith, non-singleton deployment, complex to scale horizontally](./01-app-details/appdetq07/exp03.md)<div class="risk-box medium"></div>
  * [Complex monolith, strict runtime dependency startup order, non-resilient architecture](./01-app-details/appdetq07/exp04.md)<div class="risk-box medium"></div>
  * Resilient monolith<div class="risk-box low"></div>
  * Independently deployable components<div class="risk-box low"></div>
