# How resilient is the application? How well does it recover from outages and restarts?

Answers, Risk and Explanations:

* [Unknown](./03-app-architecture/apparcq01/exp01.md)
* [Application cannot be restarted cleanly after failure, requires manual intervention (High)](./03-app-architecture/apparcq01/exp02.md)
* [Application fails when a southbound dependency is unavailable and does not recover automatically (High)](./03-app-architecture/apparcq01/exp03.md)
* [Application functionality is limited when a dependency is unavailable but recovers when the dependency is available (Medium)](./03-app-architecture/apparcq01/exp04.md)
* Application employs resilient architecture patterns (examples: circuit breakers, retry mechanisms) (Low)
* Application containers are randomly terminated to test resiliency; chaos engineering principles are followed (Low)
