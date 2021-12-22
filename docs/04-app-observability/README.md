# Application Observability

This questionnaire includes a set of questions to check and identify the current
status of the application in areas such as:

- Logging
- Metrics
- Health & Readiness

## Questionnaire

* [How does the application use logging and how are the logs accessed?](./04-app-observability/appobsq01/README.md)
  * [Unknown](./04-app-observability/appobsq01/exp01.md)<div class="risk-box unknown"></div>
  * [Logs are unavailable or are internal with no way to export them](./04-app-observability/appobsq01/exp02.md)<div class="risk-box high"></div>
  * [Logs are in a custom binary format, exposed with non-standard protocols](./04-app-observability/appobsq01/exp02.md)<div class="risk-box high"></div>
  * [Logs are exposed using syslog](./04-app-observability/appobsq01/exp04.md)<div class="risk-box medium"></div>
  * [Logs are written to a file system, sometimes as multiple files](./04-app-observability/appobsq01/exp05.md)<div class="risk-box medium"></div>
  * Logs are forwarded to an external logging system<div class="risk-box low"></div>
  * Logs are configurable<div class="risk-box low"></div>
 
* [Does the application provide metrics?](./04-app-observability/appobsq02/README.md)
  * [Unknown](./04-app-observability/appobsq02/exp01.md)<div class="risk-box unknown"></div>
  * [No metrics available](./04-app-observability/appobsq02/exp02.md)<div class="risk-box medium"></div>
  * [Metrics collected but not exposed externally](./04-app-observability/appobsq02/exp03.md)<div class="risk-box medium"></div>
  * [Metrics exposed using binary protocols](./04-app-observability/appobsq02/exp04.md)<div class="risk-box medium"></div>
  * Metrics exposed using a third-party solution<div class="risk-box low"></div>
  * Metrics collected and exposed with built-in Prometheus endpoint support<div class="risk-box low"></div>
 
* [How easy is it to determine the application's health and readiness to handle traffic?](./04-app-observability/appobsq03/README.md)
  * [Unknown](./04-app-observability/appobsq03/exp01.md)<div class="risk-box unknown"></div>
  * [No health or readiness query functionality available](./04-app-observability/appobsq03/exp02.md)<div class="risk-box high"></div>
  * [Monitored and managed by a custom watchdog process](./04-app-observability/appobsq03/exp03.md)<div class="risk-box high"></div>
  * [Basic application health requires semi-complex scripting](./04-app-observability/appobsq03/exp04.md)<div class="risk-box medium"></div>
  * Dedicated, independent liveness and readiness endpoints<div class="risk-box low"></div>
  * Health is verified by probes running synthetic transactions<div class="risk-box low"></div>
 
* [What best describes the application's runtime characteristics?](./04-app-observability/appobsq04/README.md)
  * [Unknown](./04-app-observability/appobsq04/exp01.md)<div class="risk-box unknown"></div>
  * [Deterministic and predictable real-time execution or control requirements](./04-app-observability/appobsq04/exp02.md)<div class="risk-box high"></div>
  * [Sensitive to latency](./04-app-observability/appobsq04/exp03.md)<div class="risk-box medium"></div>
  * [Constant traffic with a broad range of CPU and memory usage](./04-app-observability/appobsq04/exp04.md)<div class="risk-box medium"></div>
  * Intermittent traffic with predictable CPU and memory usage<div class="risk-box low"></div>
  * Constant traffic with predictable CPU and memory usage<div class="risk-box low"></div>
 
* [How long does it take the application to be ready to handle traffic?](./04-app-observability/appobsq05/README.md)
  * [Unknown](./04-app-observability/appobsq05/exp01.md)<div class="risk-box unknown"></div>
  * [More than 5 minutes](./04-app-observability/appobsq05/exp02.md)<div class="risk-box high"></div>
  * [2-5 minutes](./04-app-observability/appobsq05/exp03.md)<div class="risk-box medium"></div>
  * [1-2 minutes](./04-app-observability/appobsq05/exp04.md)<div class="risk-box medium"></div>
  * 10-60 seconds<div class="risk-box low"></div>
  * Less than 10 seconds<div class="risk-box low"></div>
