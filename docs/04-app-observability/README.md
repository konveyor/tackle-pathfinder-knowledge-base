# Application Observability

This document includes a set of recommendations to be used as standard comments to add in Pathfinder reports when some of
the topics are identified as `High` or `Medium` risks. These recommendations are based on field experience, standard patterns
and best practices in Kubernetes space and Cloud Native applications.

This part is focused in Application Observability space.

## Questionnaire

Set of the current questions of Tackle inventory in this space:

* [How does the application use logging and how are the logs accessed?](./04-app-observability/appobsq01/README.md)
  * [Unknown](./04-app-observability/appobsq01/exp01.md)
  * [Logs are unavailable or are internal with no way to export them (High)](./04-app-observability/appobsq01/exp02.md)
  * [Logs are in a custom binary format, exposed with non-standard protocols (High)](./04-app-observability/appobsq01/exp02.md)
  * [Logs are exposed using syslog (Medium)](./04-app-observability/appobsq01/exp04.md)
  * [Logs are written to a file system, sometimes as multiple files (Medium)](./04-app-observability/appobsq01/exp05.md)
  * Logs are forwarded to an external logging system (example: Splunk) (Low)
  * Logs are configurable (example: can be sent to stdout) (Low)
 
* [Does the application provide metrics?](./04-app-observability/appobsq02/README.md)
  * [Unknown](./04-app-observability/appobsq02/exp01.md)
  * [No metrics available (Medium)](./04-app-observability/appobsq02/exp02.md)
  * [Metrics collected but not exposed externally (Medium)](./04-app-observability/appobsq02/exp03.md)
  * [Metrics exposed using binary protocols (examples: SNMP, JMX) (Medium)](./04-app-observability/appobsq02/exp04.md)
  * Metrics exposed using a third-party solution (examples: Dynatrace, AppDynamics) (Low)
  * Metrics collected and exposed with built-in Prometheus endpoint support (Low)
 
* [How easy is it to determine the application's health and readiness to handle traffic?](./04-app-observability/appobsq03/README.md)
  * [Unknown](./04-app-observability/appobsq03/exp01.md)
  * [No health or readiness query functionality available (High)](./04-app-observability/appobsq03/exp02.md)
  * [Monitored and managed by a custom watchdog process (High)](./04-app-observability/appobsq03/exp03.md)
  * [Basic application health requires semi-complex scripting (Medium)](./04-app-observability/appobsq03/exp04.md)
  * Dedicated, independent liveness and readiness endpoints (Low)
  * Health is verified by probes running synthetic transactions (Low)
 
* [What best describes the application's runtime characteristics?](./04-app-observability/appobsq04/README.md)
  * [Unknown](./04-app-observability/appobsq04/exp01.md)
  * [Deterministic and predictable real-time execution or control requirements (High)](./04-app-observability/appobsq04/exp02.md)
  * [Sensitive to latency (examples: voice applications, high frequency trading applications) (Medium)](./04-app-observability/appobsq04/exp02.md)
  * [Constant traffic with a broad range of CPU and memory usage (Medium)](./04-app-observability/appobsq04/exp02.md)
  * Intermittent traffic with predictable CPU and memory usage (Low)
  * Constant traffic with predictable CPU and memory usage (Low)
 
* [How long does it take the application to be ready to handle traffic?](./04-app-observability/appobsq05/README.md)
  * [Unknown](./04-app-observability/appobsq05/exp01.md)
  * [More than 5 minutes (High)](./04-app-observability/appobsq05/exp02.md)
  * [2-5 minutes (Medium)](./04-app-observability/appobsq05/exp03.md)
  * [1-2 minutes (Medium)](./04-app-observability/appobsq05/exp04.md)
  * 10-60 seconds (Low)
  * Less than 10 seconds (Low)
