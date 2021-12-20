# How does the application manage its internal state?

Answers, Risk and Explanations:

* [Unknown](./03-app-architecture/apparcq03/exp01.md)
* [Application components use shared memory within a pod (Medium)](./03-app-architecture/apparcq03/exp02.md)
* [State is managed externally by another product (examples: Zookeeper or Red Hat Data Grid) (Medium)](./03-app-architecture/apparcq03/exp03.md)
* [State maintained in non-shared, non-ephemeral storage (Medium)](./03-app-architecture/apparcq03/exp04.md)
* Disk shared between application instances (Low)
* Stateless or ephemeral container storage (Low)
