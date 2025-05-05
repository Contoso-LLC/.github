---
contact:
  name: Contoso Platform Engineering Team
  email: plateng@contoso.com
  url: https://www.contoso.com/team/markweitzel
version: 1.0.0
description: >-
  Organizational deployment policies for Contoso LLC's evergreen platform engineering.
last_updated: 2025-04-18
tags:
  - organizational-policy
  - deployment
  - evergreen-platform
---

# Deployment Policies

## Deployment Rules

- All infrastructure and application deployments **MUST** be defined using approved Infrastructure as Code (IaC) tools, specifically Bicep or Terraform.
- All infrastructure **SHOULD** use one of the [approved IaC templates](./standard-environment-definitions) provided by the platform engineering team.
- Deployment definitions **MUST** be stored in version-controlled repositories.
- All changes to deployment definitions **MUST** go through code review and approval processes before being applied.
- Deployments **SHOULD** be automated using CI/CD pipelines to ensure consistency and repeatability.
- Manual changes to deployed resources in production environments are **NOT PERMITTED** except in emergency situations, and must be documented and remediated via IaC as soon as possible.
- IaC templates **MUST** include configuration for monitoring, alerting, and security controls in production environments. For non-production environments, IaC templates **SHOULD** include these configurations.
- All deployments **MUST** be idempotent, allowing safe re-application without unintended side effects.
- Teams **SHOULD** use one of the pre-approved and defined deployment definitions provided by the platform engineering team, unless a valid exception is documented and approved.

## Environment Categories

The following environment categories are recognized and must be clearly identified in deployment definitions:

- **Sandbox**: Used for experimentation and learning. Minimal controls and monitoring. Not for production data.
- **Development (dev)**: Used for active development and integration. May have relaxed controls but should mimic production as closely as practical.
- **Test**: Used for testing, quality assurance, and validation. Should closely mirror production in configuration and scale.
- **Production (prod)**: Used for live workloads and customer-facing services. Highest level of controls, monitoring, and restrictions.
