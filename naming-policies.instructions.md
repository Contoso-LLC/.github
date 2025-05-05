---
contact:
  name: Contoso Platform Engineering Team
  email: plateng@contoso.com
  url: https://www.contoso.com/team/markweitzel
version: 1.0.0
description: >-
  Organizational naming policies for Contoso LLC's evergreen platform engineering.
last_updated: 2025-04-29
tags:
  - organizational-policy
  - naming
  - evergreen-platform
---

# Naming Policies

## Naming Conventions

### Azure Resource Naming

All Azure resources **MUST** follow these naming conventions:

| Resource Type      | Naming Convention                        |
|--------------------|------------------------------------------|
| Resource Group     | rg-environment-workload-location         |
| Storage Account    | stenvironmentworkloadunique              |
| Virtual Network    | vnet-environment-workload-location        |
| Subnet             | snet-environment-workload-location        |
| App Service        | app-environment-workload-location         |
| Key Vault          | kv-environment-workload-location          |
| SQL Database       | sql-environment-workload-location         |

Where:

- environment: dev, test, prod, etc.
- workload: short name for the application or service
- location: Azure region abbreviation (e.g., eus for East US)
- unique: a unique string to ensure global uniqueness where required
