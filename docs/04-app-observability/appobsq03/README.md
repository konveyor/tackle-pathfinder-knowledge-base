# How easy is it to determine the application's health and readiness to handle traffic?

Answers, Risk and Explanations:

* [Unknown](./04-app-observability/appobsq03/exp01.md)
* [No health or readiness query functionality available (High)](./04-app-observability/appobsq03/exp02.md)
* [Monitored and managed by a custom watchdog process (High)](./04-app-observability/appobsq03/exp03.md)
* [Basic application health requires semi-complex scripting (Medium)](./04-app-observability/appobsq03/exp04.md)
* Dedicated, independent liveness and readiness endpoints (Low)
* Health is verified by probes running synthetic transactions (Low)
