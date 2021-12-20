# How does the application use logging and how are the logs accessed?

Answers, Risk and Explanations:

* [Unknown](./04-app-observability/appobsq01/exp01.md)
* [Logs are unavailable or are internal with no way to export them (High)](./04-app-observability/appobsq01/exp02.md)
* [Logs are in a custom binary format, exposed with non-standard protocols (High)](./04-app-observability/appobsq01/exp02.md)
* [Logs are exposed using syslog (Medium)](./04-app-observability/appobsq01/exp04.md)
* [Logs are written to a file system, sometimes as multiple files (Medium)](./04-app-observability/appobsq01/exp05.md)
* Logs are forwarded to an external logging system (example: Splunk) (Low)
* Logs are configurable (example: can be sent to stdout) (Low)
