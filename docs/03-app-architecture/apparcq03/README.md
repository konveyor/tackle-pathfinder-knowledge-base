# How does the application manage its internal state?

Answers, Risk and Explanations:

* [Unknown](./03-app-architecture/apparcq03/exp01.md)<div class="risk-box unknown"></div>
* [Application components use shared memory within a pod](./03-app-architecture/apparcq03/exp02.md)<div class="risk-box medium"></div>
* [State is managed externally by another product](./03-app-architecture/apparcq03/exp03.md)<div class="risk-box medium"></div>
* [State maintained in non-shared, non-ephemeral storage](./03-app-architecture/apparcq03/exp04.md)<div class="risk-box medium"></div>
* Disk shared between application instances<div class="risk-box low"></div>
* Stateless or ephemeral container storage<div class="risk-box low"></div>
