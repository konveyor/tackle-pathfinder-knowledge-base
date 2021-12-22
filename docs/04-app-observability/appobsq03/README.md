# How easy is it to determine the application's health and readiness to handle traffic?

Answers, Risk and Explanations:

* [Unknown](./04-app-observability/appobsq03/exp01.md)<div class="risk-box unknown"></div>
* [No health or readiness query functionality available](./04-app-observability/appobsq03/exp02.md)<div class="risk-box high"></div>
* [Monitored and managed by a custom watchdog process](./04-app-observability/appobsq03/exp03.md)<div class="risk-box high"></div>
* [Basic application health requires semi-complex scripting](./04-app-observability/appobsq03/exp04.md)<div class="risk-box medium"></div>
* Dedicated, independent liveness and readiness endpoints<div class="risk-box low"></div>
* Health is verified by probes running synthetic transactions<div class="risk-box low"></div>
