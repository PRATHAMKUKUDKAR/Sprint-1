# GitOps


| Author | Created on | Version  | Last updated by | Last edited on | Reviewed By L0 | Reviewed By L1 | 
|--------|------------|----------|-----------------|----------------|----------------|----------------|
| Priyanshu Yadav | 15-11-24   | 1 |  Priyanshu Yadav |  20/11/2024 |Tapan Kumar Sahu |                | 

## Table of Contents
- [Introduction](#introduction)
- [What is GitOps?](#what-is-gitops)
- [Why GitOps?](#why-gitops)
- [Types of GitOps Workflows](#types-of-gitops-workflows)
- [Comparison of GitOps Workflows](#comparison-of-gitops-workflows)
- [Gitops strategies](#Gitops-strategies)
- [Conclusion](#conclusion)
- [Contact Information](#contact-information)
- [References](#references)


## Introduction
In the evolving landscape of DevOps, GitOps has emerged as a paradigm that leverages Git as the single source of truth for managing infrastructure and application deployments. GitOps brings reliability, security, and speed to the development and operational workflows by utilizing Git repositories for version control and automation.

## What is GitOps?
GitOps is a set of practices that use Git repositories as the source of truth for declarative infrastructure and applications. It encompasses the use of Git as a version control system to manage changes, ensuring that the desired state of the system is always represented in the Git repository. These changes are automatically applied to the system by reconciling the actual state with the declared state.

## Why GitOps?
GitOps provides numerous benefits, including:
- **Version Control**: Every change is tracked, ensuring a clear history and audit trail.
- **Consistency and Standardization**: By using a single source of truth, environments can be easily replicated and managed.
- **Automation**: Continuous deployment is achieved through automated reconciliation of the desired state, reducing manual intervention.
- **Improved Collaboration**: Changes are made through pull requests and code reviews, enhancing collaboration among teams.
- **Enhanced Security**: Access controls and audit logs in Git enhance the security of deployments.

## Types of GitOps Workflows

| Workflow             | Description                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------|
| **Pull-Based**           | An agent runs inside the cluster, continuously monitoring the Git repository for state reconciliation. |
| **Push-Based**           | Changes are pushed to the Git repository, triggering CI/CD pipelines for deployment to the cluster. |
| **Manual Sync**          | Changes are manually committed to the Git repository, and synchronization with the cluster is triggered manually. |
| **Event-Driven**         | Specific events trigger deployment, automating the process based on events like commits or merges. |
| **Hybrid**               | Combines elements of pull-based, push-based, and manual sync workflows, adapted to fit organizational needs. |
| **Multi-Cluster**        | Manages multiple clusters from a single Git repository, ensuring consistent deployments across environments. |

## Comparison of GitOps Workflows

| Feature             | Push-Based GitOps | Pull-Based GitOps | Manual Sync GitOps | Event-Driven GitOps | Hybrid GitOps | Multi-Cluster GitOps |
|---------------------|-------------------|-------------------|--------------------|---------------------|---------------|----------------------|
| **Security**            | Requires credentials in CI/CD pipeline | Credentials not required in pipeline | Can be tightly controlled | Depends on event sources | Combines security features | Manages credentials across clusters |
| **Consistency**         | Susceptible to drift | Continuously ensures consistency | Manual checks needed | Event-triggered consistency | Mixed consistency based on methods | Ensures consistency across clusters |
| **Deployment Speed**    | Immediate after commit | Dependent on polling interval | Delayed due to manual intervention | Immediate based on events | Varies by method used | Consistent deployment across clusters |
| **Complexity**          | Simpler to implement | More complex setup | Simple but manual | Complex due to event setup | Can be highly complex | High complexity due to coordination |
| **Multi-Environment**   | Limited support | Excellent support | Limited and manual | Good support with event configuration | Flexible multi-environment support | Excellent support for multiple clusters |

## Gitops strategies

GitOps is an operational framework that uses Git as the single source of truth for declarative infrastructure and applications. It leverages Git repositories to manage and track changes, promoting collaboration, transparency, and automation in the deployment and management of cloud-native applications. Here are some key GitOps strategies:

- ### Declarative Configuration
   - **Definition**: Use declarative definitions for infrastructure and applications, meaning you specify the desired state in configuration files stored in Git repositories.
   - **Benefit**: Ensures that the system's state is version-controlled and reproducible.

- ### Single Source of Truth
   - **Definition**: Git repositories serve as the single source of truth for both infrastructure and application code.
   - **Benefit**: Changes are tracked and audited, making it easier to manage configurations and rollback if necessary.

- ### Automated Workflows
   - **Definition**: Utilize Continuous Integration and Continuous Deployment (CI/CD) pipelines to automate the application and infrastructure deployment processes.
   - **Benefit**: Reduces manual intervention, minimizes errors, and accelerates the deployment process.


- ### Infrastructure as Code (IaC)
   - **Definition**: Manage infrastructure using code and configuration files stored in version control.
   - **Benefit**: Promotes consistency, repeatability, and traceability of infrastructure changes.


- ### Observability and Monitoring
   - **Definition**: Implement monitoring and observability tools to track the state and performance of applications and infrastructure.
   - **Benefit**: Provides insights into system health and enables proactive management.

- ### Security and Compliance
   - **Definition**: Embed security and compliance checks within the GitOps pipeline.
   - **Benefit**: Ensures that all changes comply with security policies and regulations, reducing the risk of vulnerabilities.

- ### Rollback and Recovery
   - **Definition**: Use Git's versioning capabilities to quickly rollback to previous states in case of issues.
   - **Benefit**: Simplifies recovery and minimizes downtime during incidents.



## Conclusion
GitOps has revolutionized the way we manage and deploy infrastructure and applications. By leveraging the strengths of Git as a version control system, GitOps enhances consistency, security, and automation. Choosing between push-based and pull-based workflows depends on the specific needs and constraints of our project.
## Contact Information

| Name           | Email address                        | 
|----------------|--------------------------------------|
| Priyanshu Yadav | priyanshu.yadav.snaatak@mygurukulam.co | 

## References

| Links | Descriptions | 
|-------|--------------|
|https://docs.mia-platform.eu/docs/development_suite/deploy/gitops-based/#:~:text=The%20GitOps%20deployment%20strategy%20is,stored%20in%20the%20Git%20repository. | GitOps strategy |
|https://www.gitops.tech/| about using GitOps |
| https://codefresh.io/learn/gitops/gitops-workflow-vs-traditional-workflow-what-is-the-difference/ | GitOps Workflow vs. Traditional Workflow |
