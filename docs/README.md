# Tackle Pathfinder Knowledge Base

Tackle Pathfinder is one of the open-source tools of the [Konveyor Commnunity](https://www.konveyor.io)
to assess your app portfolio to getting containerization recommendations, to automated
testing for your modernized app into Kubernetes platforms.

[Tackle Pathfinder](https://github.com/konveyor/tackle-pathfinder) is a questionnaire
based tool that assesses the suitability of applications for modernization in order
to be deployed in Containers on an enterprise Kubernetes platform. Through
interaction with the questionnaire, and review process, the system is enriched
with application knowledge which is exposed via a collection of reports.
The reports provide information about applications’ suitability for Kubernetes
highlight associated risks, and generate an adoption plan informed by the
applications’ prioritization, business criticality and dependencies.

This site includes a set of recommendations to be used as standard knowledge base
for each of the questions in a Pathfinder report when some of the topics are
identified as `High` or `Medium`.

These recommendations are based on field experience, standard patterns and
best practices in Kubernetes space and Cloud Native applications.

The knowledge base is splitted into the different spaces analyzed by Tackle Pathfinder:

* [Application Details](./01-app-details/README.md)
* [Application Dependencies](./02-app-dependencies/README.md)
* [Application Architecture](./03-app-architecture/README.md)
* [Application Observability](./04-app-observability/README.md)
* [Application Cross Cutting Concerns](./05-app-cross-cutting-concerns/README.md)

# Understanding Knowledge Base

Each question of Pathfinder questionnaire includes a set of different answers to
identify the current status of the application. Basically the current status of the
application for each question identifies the gap associated with migrating the
application to a Kubernetes platform. This gap could be marked with one of the
following levels:

* Unknown<div class="risk-box unknown"></div>
* High<div class="risk-box high"></div>
* Medium<div class="risk-box medium"></div>
* Low<div class="risk-box low"></div>

This level has not a direct relationship with efforts or times, and it should be
read as the prioritization to resolve it in a good migration and modernization
of our application.

## Unknown

A topic identified as `Unknown` identifies that the current knowledge or experience
does not allow us to measure correctly. It is recommended to measure it identifying
the teams, team leads or stakeholders with the knowledge or experience to answer
the question.

## High

A topic identified as `High` does not mean that it is impossible to containerize
the application. It means that this topic will most probably block the migration or
modernization of the application unless it is mitigated.

## Medium

A topic identified as `Medium` identifies an improvement area in the migration or modernization of the application. Normally it is an area that could work with a
moderate level of success in a Kubernetes platform, but it should be improved to
a smooth and better transition to the final platform.

## Low

A topic identified as `Low` identifies an area aligned with the best practices in
Kubernetes platform or a topic with a low impact in the migration and modernization of the application.
