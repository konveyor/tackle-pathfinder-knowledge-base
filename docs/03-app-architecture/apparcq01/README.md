# How resilient is the application? How well does it recover from outages and restarts?

Answers, Risk and Explanations:

* [Unknown](./03-app-architecture/apparcq01/exp01.md)<div class="risk-box unknown"></div>
* [Application cannot be restarted cleanly after failure, requires manual intervention](./03-app-architecture/apparcq01/exp02.md)<div class="risk-box high"></div>
* [Application fails when a southbound dependency is unavailable and does not recover automatically](./03-app-architecture/apparcq01/exp03.md)<div class="risk-box high"></div>
* [Application functionality is limited when a dependency is unavailable but recovers when the dependency is available](./03-app-architecture/apparcq01/exp04.md)<div class="risk-box medium"></div>
* Application employs resilient architecture patterns<div class="risk-box low"></div>
* Application containers are randomly terminated to test resiliency; chaos engineering principles are followed<div class="risk-box low"></div>
