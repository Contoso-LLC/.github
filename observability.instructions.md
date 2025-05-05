---
contact:
  name: Contoso Platform Engineering Team
  email: plateng@contoso.com
  url: https://www.contoso.com/team/markweitzel
version: 1.0.0
description: >-
  Organizational observability policies for Contoso LLC's evergreen platform engineering.
last_updated: 2025-04-18
tags:
  - organizational-policy
  - observability
  - evergreen-platform
---

# Observability Policies

## Instrumentation Rules

- Applications and infrastructure **MUST** emit logs, metrics, and traces to a centralized observability platform (e.g., Azure Monitor, Application Insights).
- All production workloads **MUST** include health checks and expose endpoints for monitoring system status.
- Logs **MUST** include sufficient context (correlation IDs, timestamps, environment, and workload identifiers) to support troubleshooting and root cause analysis.
- Metrics **MUST** be collected for key performance indicators (KPIs) such as latency, error rates, and resource utilization.
- Distributed tracing **SHOULD** be implemented for all services that participate in request flows across system boundaries.
- Applications **SHOULD** use structured logging formats (e.g., JSON) to facilitate automated analysis.
- Infrastructure as Code (IaC) deployments **SHOULD** include configuration for monitoring and alerting resources.
- Non-production environments **MAY** have reduced observability requirements, but should still provide enough data for debugging and performance testing.
- Custom business metrics **MAY** be instrumented to provide additional insights into application behavior and user experience.

## Alerting

A default set of alerts should be configured for all production workloads to ensure timely detection and response to issues. The following alerts are recommended:

| Alert Name                | Description                                                      | Severity   | Threshold/Condition                                  |
|---------------------------|------------------------------------------------------------------|------------|------------------------------------------------------|
| High Error Rate           | Triggered when error rate exceeds acceptable limits               | Critical   | Error rate > 5% over 5 minutes                       |
| High Latency              | Triggered when request/response latency exceeds target            | Warning    | 95th percentile latency > 1s over 5 minutes          |
| Resource Utilization      | Triggered when CPU, memory, or disk usage is abnormally high      | Warning    | CPU/Memory > 80% for 10 minutes                      |
| Service/Endpoint Down     | Triggered when a health check endpoint is unreachable             | Critical   | Health check fails for 3 consecutive attempts         |
| Missing Telemetry         | Triggered when no logs/metrics/traces are received from a service | Warning    | No telemetry for 10 minutes                          |
| Security Event Detected   | Triggered on detection of security-related log events             | Critical   | Security event pattern match in logs                 |

- Alerts **MUST** be routed to the appropriate on-call team or incident management system.
- Alert thresholds **SHOULD** be reviewed and tuned regularly to minimize false positives and ensure relevance.
- Non-production environments **MAY** have relaxed alerting thresholds or reduced alert coverage.

## On-Call Policies

- An on-call rotation **MUST** be established for all production systems to ensure 24/7 coverage.
- On-call personnel **MUST** have access to all relevant observability and alerting platforms.
- Escalation procedures **MUST** be documented and accessible to the on-call team.
- Contact information for the current on-call engineer or team **MUST** be up to date and easily accessible.
- On-call engineers **SHOULD** acknowledge critical alerts within 15 minutes and begin triage immediately.
- Post-incident reviews **SHOULD** be conducted for all major incidents to identify root causes and improve response processes.
- Backup on-call personnel **MAY** be designated to provide additional support during high-severity incidents or holidays.
