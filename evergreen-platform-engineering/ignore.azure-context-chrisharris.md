# Azure Context Document

## Tenant Information
- **Tenant Name**: Microsoft
- **Tenant ID**: 72f988bf-86f1-41af-91ab-2d7cd011db47
- **Subscriptions**:
  - charris-demosub (ID: 4feebfc0-ddbe-4bc2-802c-0ae0c40517d0)
  - GithubCopilotForAzure-Testing (ID: cda6aeab-6dec-4567-a4d8-3770583a13f0)

## Resource Information
### Common Resource Types
Based on analysis of your current Azure subscriptions, the following resource types are most commonly used:

1. Operational Insights Workspaces (12)
2. Storage Accounts (11)
3. Network Watchers (11)
4. Container Registries (9)
5. Cognitive Services Accounts (8)
6. User Assigned Managed Identities (8)
7. App Managed Environments (7)
8. Application Insights Components (7)
9. Container Apps (6)
10. Web Sites (5)

This indicates a preference for containerized applications and a focus on monitoring and observability.

### Virtual Network Details
- Found virtual network "mysql-vnet" with subnet "mysql-subnet" in the "tomescht-mysql-rg" resource group

### Azure Region Geography
Resources are primarily deployed in the following regions (in order of frequency):
1. **westus2** (34 resources)
2. **eastus** (32 resources)
3. **eastus2** (20 resources)
4. **westus** (17 resources)
5. **global** (9 resources)
6. **canadacentral** (7 resources)
7. **westus3** (5 resources)
8. southcentralus, japaneast, uksouth (1 each)

This indicates a strong preference for US regions, particularly West US 2 and East US.

## Infrastructure Details
### Infrastructure as Code (IaC)
- **Evidence of Bicep usage**: Resources found with "createdBy: Bicep" tag

### Azure SDKs Used
- No specific SDK information found in the available data

## Organizational Policies
### Tagging Policies
Common tags found across resources include:
- **Creator**: Used to indicate who created the resource (e.g., "Bicep", "Automatically added by NRMS Azure Policy")
- **CreatedDate**: Used to track when resources were created
- **contact**: Used to indicate the point of contact for a resource
- **purpose**: Used to describe the purpose of a resource (e.g., "MySQL Database")
- Several system-generated tags related to Azure OpenAI and AI services

### Naming Conventions
Based on resource names observed:
- AI resources often use a prefix like "ai-" followed by a descriptive name
- Virtual networks may use a naming pattern that indicates their purpose (e.g., "mysql-vnet")

## Preferences
### Service Preferences
- **Compute**: Strong preference for containerization with Container Apps and Container Registries
- **Databases**: Evidence of MySQL database usage
- **AI/ML**: Significant usage of Cognitive Services and Azure OpenAI

### Monitoring and Observability
- Heavy use of Operational Insights Workspaces and Application Insights suggests a commitment to comprehensive monitoring

### Deployment Preferences
- Evidence of Bicep usage for Infrastructure as Code

### Security Preferences
- Usage of User Assigned Managed Identities indicates a focus on secure authentication methods

This document represents a summary of the organizational context, policies, and preferences detected in the current Azure environment based on available information. Individual resource names are excluded, but patterns and preferences are highlighted where detected.
