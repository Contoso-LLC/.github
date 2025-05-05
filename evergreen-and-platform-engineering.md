> [!note]
> 
> This document is a collection of ideas on how an organizations best practices and standards for platform engineering can serve as input to the evergreen/scaffolding agent. It is intended to be a living document that evolves over time as new information and insights are gained. Any & all feedback/suggestions that you have would be aweseome and greatly appreciated.


# Background on Platform Engineering
Platform engineering is a discipline that focuses on designing and building platforms that enable developers to deliver software more efficiently and effectively. It involves creating a set of tools, processes, and best practices that help teams build, deploy, and manage applications in a consistent and reliable manner.
Platform engineering is often seen as a response to the challenges of traditional software development, where teams struggle with complex infrastructure, inconsistent tooling, a lack of standardization, and increased operational overhead, e.g. lengthy approval processes. By providing a unified platform that abstracts away the underlying complexity, reduces developer toil, and enables self-service, dev teams are able to focus on building applications and delivering value to their organization.

## Everything as Code
The concept of "everything as code" is a key principle in platform engineering. It emphasizes the need to treat all aspects of the platform, including infrastructure, configuration, policies, and processes, as code. This approach allows teams to leverage version control, automation, and collaboration tools to manage their platforms more effectively. The approach for the evergreen agent will be to pull the organizational standards and policies from a Git repository following this pattern.

### Well known location
There are two "special" repositories in every GitHub organization: .github and .github-private. These repositories are used to store organization-wide settings, policies, and templates. As a convention, we'll use these for a consistent and predictable location for the evergreen agent to find the organizational standards and policies. 

In addition, each repository can also have a .github folder that can be used for project-specific settings, policies, and templates. This allows for a clear separation of organization-wide and project-specific configurations/overrides.

## Separation of Concerns
Organizations often have different teams responsible for different aspects of the platform, such as infrastructure, security, observability, and deployment. Therefore, each "concern" should be able to have its own set of policies and standards that can be managed independently. This allows for greater flexibility and agility in managing the platform, as well as reducing the risk of conflicts between different teams.

## Specifying Policies and Standards
In this sample organization we'll use markdown with front matter to specify the policies and standards. This allows for a clear and human-readable format that can be easily understood by all stakeholders. The front matter can be used to specify metadata about the policy, such as the version, contact information, and tags. The body of the document can be used to specify the actual policy or standard, including any examples or explanations.

### Examples

Below are examples of markdown-based organizational standards and policies used in this repository. The rules themselves are written in a "specification" format, e.g. "MUST", "SHOULD", "MAY", etc. This allows for a clear and unambiguous definition of the policy, which can be easily understood and enforced by the evergreen agent (or another agent/tool that it orchestrates).

- [Naming and Tagging Policy](evergreen-platform-engineering/organizational-standards/naming-tagging.md)
- [Deployment Environment Policy](evergreen-platform-engineering/organizational-standards/deployment-environment.md)
- [Observability Policy](evergreen-platform-engineering/organizational-standards/observability.md)
- [Security Policy](evergreen-platform-engineering/organizational-standards/security.md)
