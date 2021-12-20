# Application Details

This document includes a set of recommendations to be used as standard comments to add in Pathfinder reports when some of
the topics are identified as `High` or `Medium` risks. These recommendations are based on field experience, standard patterns
and best practices in Kubernetes space and Cloud Native applications.

This part is focused in Application Details space.

## Questionnaire

Set of the current questions of Tackle inventory in this space:

* [Does the application development team understand and actively develop the application?](./01-app-details/appdetq01/README.md)
  * [Unknown](./01-app-details/appdetq01/exp01.md)
  * [Little knowledge, no development (example: third-party or commercial off-the-shelf application) (High)](./01-app-details/appdetq01/exp02.md)
  * [Maintenance mode, no SME knowledge or adequate documentation available (High)](./01-app-details/appdetq01/exp03.md)
  * [Maintenance mode, SME knowledge is available (Medium)](./01-app-details/appdetq01/exp04.md)
  * Actively developed, SME knowledge is available (Low)
  * Greenfield application (Low)
 
* [How is the application supported in production?](./01-app-details/appdetq02/README.md)
  * [Unknown](./01-app-details/appdetq02/exp01.md)
  * [External support provider with a ticket-driven escalation process; no inhouse support resources (High)](./01-app-details/appdetq02/exp02.md)
  * [Separate internal support team, separate from the development team, with little interaction between the teams (High)](./01-app-details/appdetq02/exp03.md)
  * [Multiple teams provide support using an established escalation model (Medium)](./01-app-details/appdetq02/exp04.md)
  * SRE (Site Reliability Engineering) approach with a knowledgeable and experienced operations team (Low)
  * DevOps approach with the same team building the application and supporting it in production (Low)
 
* [How much time passes from when code is committed until the application is deployed to production?](./01-app-details/appdetq03/README.md)
  * [Unknown](./01-app-details/appdetq03/exp01.md)
  * [Not tracked (High)](./01-app-details/appdetq03/exp02.md)
  * [More than 6 months (High)](./01-app-details/appdetq03/exp03.md)
  * [2-6 months (Medium)](./01-app-details/appdetq03/exp04.md)
  * 8-30 days (Low)
  * 1-7 days (Low)
  * Less than 1 day (Low)
 
* [How often is the application deployed to production?](./01-app-details/appdetq04/README.md)
  * [Unknown](./01-app-details/appdetq04/exp01.md)
  * [Not tracked (High)](./01-app-details/appdetq04/exp02.md)
  * [Less than once every 6 months (High)](./01-app-details/appdetq04/exp03.md)
  * [Between once a month and once every 6 months (Medium)](./01-app-details/appdetq04/exp04.md)
  * Weekly (Low)
  * Daily (Low)
  * Several times a day (Low)
 
* [What is the application's mean time to recover (MTTR) from failure in a production environment?](./01-app-details/appdetq05/README.md)
  * [Unknown](./01-app-details/appdetq05/exp01.md)
  * [Not tracked (High)](./01-app-details/appdetq05/exp02.md)
  * [1 month or more (High)](./01-app-details/appdetq05/exp03.md)
  * [1-7 days (Medium)](./01-app-details/appdetq05/exp04.md)
  * 1-24 hours (Low)
  * Less than 1 hour (Low)
 
* [Does the application have legal and/or licensing requirements?](./01-app-details/appdetq06/README.md)
  * [Unknown](./01-app-details/appdetq06/exp01.md)
  * [Multiple legal and licensing requirements (High)](./01-app-details/appdetq06/exp02.md)
  * [Licensing requirements (examples: per server, per CPU) (Medium)](./01-app-details/appdetq06/exp03.md)
  * [Legal requirements (examples: cluster isolation, hardware, PCI or HIPAA compliance) (Medium)](./01-app-details/appdetq06/exp04.md)
  * None (Low)
 
* [Which model best describes the application architecture?](./01-app-details/appdetq07/README.md)
  * [Unknown](./01-app-details/appdetq07/exp01.md)
  * [Massive monolith (high memory and CPU usage), singleton deployment, vertical scale only (Medium)](./01-app-details/appdetq07/exp02.md)
  * [Massive monolith (high memory and CPU usage), non-singleton deployment, complex to scale horizontally (Medium)](./01-app-details/appdetq07/exp03.md)
  * [Complex monolith, strict runtime dependency startup order, non-resilient architecture (Medium)](./01-app-details/appdetq07/exp04.md)
  * Resilient monolith (examples: retries, circuit breakers) (Low)
  * Independently deployable components (Low)
