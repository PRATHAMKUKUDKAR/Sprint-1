#  Mono vs. Micro Repositories

| Created/Modified | Version | Author              | Comment          | Reviewer       |
|-------------------|---------|---------------------|------------------|----------------|
| 11-11-2024        | V1      | Pratham Kukudkar    | Initial Commit   |                |
| 15-11-2024        | V2      | Pratham Kukudkar    | L0             |     Tapan            |
| 20-11-2024        | V3      | Pratham Kukudkar    | L1            |       Sashi     |

<p align="center">
  <img src="https://github.com/user-attachments/assets/d8291bcc-bbf7-423f-91da-aefa5fda9632" alt="Mono vs Multi Repository" width="500"/>
</p>

## Table of Contents
- [Introduction](#introduction)
  - [Monorepository](#monorepository)
  - [Microservices Repository](#microservices-repository)
- [Mono Repository vs Micro Repository](#mono-repository-vs-micro-repository)
- [Choosing the Right Approach](#choosing-the-right-approach)
- [Conclusion](#conclusion)
- [Contact Information](#contact-information)
- [References](#references)

## Introduction

Choosing between Mono and Micro Repositories is a critical decision in software development, as it shapes the project's architecture, collaboration model, and scalability.

## Monorepository
A monorepository, or monolith repository, is a single repository that houses the code for multiple projects, services, or modules. This approach to version control offers centralized management of multiple interconnected components within a unified codebase.

### Monorepository Examples
- **Google**: Manages various projects like search, Gmail, and Maps in a single unified code repository.
- **Facebook**: Utilizes a monolithic repository for its core platform components like news feed and messaging.

## Microservices Repository

In a microservices repository pattern, each microservice has its own repository, enabling independent version control, testing, and deployment. This decentralized approach aligns with the modularity and autonomy principles of microservices architecture.

### Microservices Repository Examples
- **Netflix**: Adopts a microservices architecture with independent repositories for services like streaming and recommendations.
- **Amazon**: Implements microservices-based architecture with separate repositories for services, enabling scalable development and deployment.

## Mono Repository vs Micro Repository

| Mono Repository                                       | Micro Repository                                      |
|------------------------------------------------------|-------------------------------------------------------|
| Single repository containing code for all projects   | Multiple repositories, each dedicated to a project or component |
| May lead to increased complexity as codebase grows   | Provides modularity and reduces complexity            |
| Limited parallel development across projects         | Enables concurrent development on separate repositories |
| Unified governance                                   | Requires governance for managing multiple repositories |
| Testing the entire codebase may be complex           | Testing can be more focused on individual projects     |
| Centralized version history for all projects         | Distributed version control with project-specific histories |

## Choosing the Right Approach

When deciding between Mono and Micro Repositories, consider the following factors:

- **Project Size and Complexity**: For smaller projects with fewer dependencies, a Mono Repository may suffice. Larger, more complex projects often benefit from the isolation provided by Micro Repositories.
- **Team Structure and Collaboration Model**: Evaluate how teams are organized and how they collaborate. Mono Repositories promote cross-project collaboration, while Micro Repositories offer greater independence for individual teams.
- **Scalability Requirements**: Consider the project's growth trajectory. Micro Repositories offer better scalability and agility for rapidly evolving projects.

## Conclusion

Both Mono and Micro Repository architectures have their strengths and weaknesses. The choice depends on various factors such as project size, team dynamics, and scalability requirements. In our case, we've opted for a Micro Repository approach to better align with our project's modularity, scalability, and parallel development needs.

## Contact Information

| Name             | Email Address                          |
|------------------|---------------------------------------|
| Pratham Kukudkar | pratham.kukudkar.snaatak@mygurukulam.co |

## References

| Links                                                                                                  | Descriptions                                                                                       |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [LinkedIn - Navigating Codebase Management](https://www.linkedin.com/pulse/navigating-codebase-management-monorepo-vs-microrepo-rajeev-barnwal-u318f/) | The author discusses the differences and usability of mono and micro repositories. |
| [Medium - Understanding Micro vs. Mono Repo](https://apoorv-tomar.medium.com/a-better-understanding-of-micro-rep-vs-mono-repo-a9f31f1e20fe) | This link provides an understanding of the repositories. |
| [Redswitches - Monolith vs Microservices](https://www.redswitches.com/blog/monolith-vs-microservices/) | Explains the differences between monolithic and microservices approaches. |
| [GitHub - Mono Repo Features](https://github.com/MyGurukulam-p11/Documentation-P11/blob/Pratham-Scrum-26/VCS%20Design%20+%20POC/Mono-Micro%20Repo/Mono%20repo%20features/README.md) | Detailed mono repository features. |
| [GitHub - Micro Repo Features](https://github.com/MyGurukulam-p11/Documentation-P11/tree/Pratham-Scrum-27/VCS%20Design%20+%20POC/Micro%20Repo/Micro%20repo%20features) | Detailed micro repository features. |
