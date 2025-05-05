---
contact:
  name: Contoso Platform Engineering Team
  email: plateng@contoso.com
  url: https://www.contoso.com/team/markweitzel
version: 1.0.0
description: >-
  Organizational tagging policies for Contoso LLC's evergreen platform engineering.
last_updated: 2025-04-29
tags:
  - organizational-policy
  - tagging
  - evergreen-platform
---

# Tagging Policies

## Tagging Specification

All Azure resources **MUST** include the following tags:

| Tag Name    | Description                                                                                 |
|-------------|---------------------------------------------------------------------------------------------|
| Creator     | MUST indicate who created the resource (e.g., "Bicep", "Automatically added by NRMS Azure Policy"). |
| CreatedDate | MUST specify the date when the resource was created.                                        |
| contact     | MUST provide the point of contact for the resource.                                         |
| purpose     | MUST describe the purpose of the resource (e.g., "MySQL Database").                        |
