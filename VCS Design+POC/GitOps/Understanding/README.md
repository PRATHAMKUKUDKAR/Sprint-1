# GitOps Understanding
![image](https://github.com/user-attachments/assets/6ea53c76-ed56-4d99-98a3-c0001528c47e)

| Author   |Created on |Version| Last updated by | Last edited on | Reviewed By L0 | Reviewed By L1 | Reviewed By L2 |
|-------------|------------|-----------|-----------------|----------------|----------------|----------------|-------|
| Priyanshu Yadav|14-11-24 | Version 1 | Priyanshu Yadav   | 20-11-24       |  Tapan Kumar Sahu           |                |   |

## Table of Content
- [Introduction](#Introduction)
- [What is Gitops](#What-is-Gitops)
- [Why do we use Gitops ?](#Why-do-we-use-Gitops)
- [Gitops principles](#Gitops-principles)
- [Different GitOps Tools](#Different-GitOps-Tools)
- [GitOps Workflows and Procedures](#GitOps-Workflows-and-Procedures)
- [Benefit of Gitops](#Benefit-of-Gitops)
- [Drawbacks of GitOps](#Drawbacks-of-GitOps)
- [GitOps Best Practices](#GitOps-Best-Practices)
- [FAQ'S](#FAQ'S)
- [References](#References)

## Introduction
   GitOps is a methodology that leverages Git as a single source of truth for infrastructure and application deployments. GitOps tools automate the deployment, management, and monitoring of infrastructure and applications using Git repositories as the central control plane. In this document, we will evaluate various GitOps tools, discussing their features, advantages, and limitations, and provide a comparison in tabular form.


## What is Gitops

Gitops is the basically a devops practice but with git repositories , it means taking git repositories as the single source of truth , now as the name suggest it has two things in it , git for version control and ops for operation that we are going to perform using that .

So gitops is a devops practice where we first have IAC ( infrastructure as code ) , it can be in terraform , ansible or Kubernetes , and then using gitops tools we manage , configure  and deploy the infra . 


## Why do we use Gitops 

- Without GitOps, deploying Terraform code from a local system creates integration issues among team members.
- Risks of pushing untested code directly to the main branch increase, potentially causing infrastructure problems.
- Lack of automated testing means higher chances of errors.
- GitOps automates infrastructure tasks like testing and deployment, and enforces branching strategies.
- Improves collaboration, reduces errors, and enhances deployment reliability.

## Gitops principles

| Principle                                      | Description                                                                                                                                                                                                                  |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Declarative Descriptions                       | Use declarative descriptions to define the desired state of the system. This means the entire system state is described using code. Tools like Kubernetes manifests, Terraform scripts, or Ansible playbooks specify what the infrastructure should look like, not how to achieve that state. |
| Version Control as the Single Source of Truth  | Use Git as the single source of truth for the desired state. This ensures that the entire system state is versioned, auditable, and easily revertible.                                                                         |
| Automated Workflows                            | Automate the application of the desired state to the infrastructure. Tools continuously monitor the Git repository for changes and apply them to the infrastructure.                                                           |
| Rollbacks                                      | Easily rollback to previous states if issues arise. This ensures that any deployment or configuration change can be reversed quickly and safely.                                                                               |


## Different GitOps Tools

| **Tool**       | **Description**                                                                 | **Features**                                                                                  |
|----------------|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| **Argo CD**    | A declarative, GitOps continuous delivery tool for Kubernetes.                   | Automatic syncing, rollback capabilities, rich UI, RBAC, multi-cluster support, monitoring, and alerting. |
| **Flux**       | A GitOps operator for Kubernetes that synchronizes the state in the Git repository with the cluster. | Automated syncing, image automation, multi-tenancy, and notifications.                        |
| **Jenkins X**  | A CI/CD platform for Kubernetes with built-in GitOps support.                    | Git-based pipelines, preview environments, automatic versioning, and promotion.               |
| **GitLab**     | An integrated DevOps platform with GitOps capabilities.                          | Git-based CI/CD, version control, monitoring, security features.                              |
| **BuildPiper** |BuildPiper is a platform that automates Kubernetes and microservices deployments with secure CI/CD pipelines and advanced observability​| GitOps-based CI/CD,Observability,Multi-cloud Support:,Automated Rollbacks|

## References
   To get more detailed information Different GitOps Tools.
   https://mygurukulam25.atlassian.net/jira/software/projects/SCRUM/boards/1?label=%23Priyanshu&selectedIssue=SCRUM-45

To get more detailed information about the tool.
## GitOps Workflows and Procedures

| **Stage**         | **Description**                                                                                          |
|-------------------|----------------------------------------------------------------------------------------------------------|
| **IAC (Infrastructure as Code)** | First, define the code that you want to deploy, whether it is Terraform, Ansible, or Kubernetes. |
| **Git Commit**    | Commit the code to the Git repository.                                                                   |
| **CI/CD**         | Deploy the code continuously using CI tools for GitOps like Argo CD.                                  |
| **Keeps Track of Code** | If the code in the Git repository changes (e.g., updating a Docker image in Kubernetes), Argo CD will automatically pull the changes and redeploy the updated code. |

 <img width="639" alt="image" src="https://github.com/user-attachments/assets/1bbab5ff-3f9a-41c0-a6d8-a6388d00f709">




## Benefit of Gitops

| Feature       | Description                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------|
| Automation    | With GitOps, complete deployment of infrastructure is automated, minimizing manual intervention and reducing the risk of errors.                                   |
| Version Control | Git serves as the foundation in GitOps, providing complete control over versioning of code, enabling easy tracking of changes, and facilitating rollbacks in case of issues. |
| Consistency   | GitOps ensures consistency across different environments (e.g., staging, production, development) by defining configuration settings in Git repositories, thereby avoiding manual configuration issues. |
| Security      | Access to Git repositories is controlled, allowing only authorized users to make changes, enhancing security.                                                  |
| Testing       | GitOps integrates with CI/CD pipelines, enabling the integration of testing tools to prevent errors.                                                            |


## Drawbacks of GitOps

| Concern                                     | Description                                                                                                                            |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Learning Curve                              | The learning curve for GitOps tools is steep. Users need to understand the functionalities of each tool, integrate them into their workflow, and then learn how to use them effectively. |
| Complexity                                  | Setting up a GitOps workflow involves configuring Git repositories, CI/CD pipelines, and Infrastructure as Code (IaC) tools. Managing these components can be complex and requires a deep understanding of various technologies. |
| Latency                                     | GitOps workflows rely on Git commits to trigger deployments, which can introduce latency. The time it takes to commit changes, run CI/CD pipelines, and apply changes to the infrastructure can slow down the deployment process. |
| Limited Support for Non-Git Configurations | GitOps heavily relies on Git for configuration management. Environments or systems that do not use Git may find it challenging to integrate GitOps practices. |
| Dependency on CI/CD Pipeline Stability     | GitOps heavily depends on the stability of CI/CD pipelines to automate deployments. Any instability or issues within these pipelines can directly impact the deployment process. |



## GitOps Best Practices

### Infrastructure as Code (IaC)
**Practice:** Define infrastructure and application configurations declaratively using code.
**Benefits:** Enables versioning, repeatability, and automation of infrastructure deployment.
**Tools:** Terraform, Kubernetes YAML files, Helm charts.

### Git Repository as the Single Source of Truth
**Practice:** Use Git repositories to store all configuration and code.
**Benefits:** Facilitates collaboration, version control, and auditability.
**Branching Strategy:** Use branching strategies such as GitFlow for managing changes.

### Automated CI/CD Pipelines
**Practice:** Implement automated pipelines for continuous integration (CI) and continuous delivery (CD).
**Benefits:** Ensures rapid feedback, consistent deployments, and reduces manual errors.
**Tools:** Jenkins, GitLab CI, Tekton, GitHub Actions.

### GitOps Tools Integration
**Practice:** Utilize dedicated GitOps tools for managing deployments and infrastructure.
**Benefits:** Simplifies deployment workflows, automates synchronization, and ensures desired state enforcement.
**Tools:** Argo CD, Flux, Jenkins X, Weave GitOps.

### Documentation and Knowledge Sharing
**Practice:** Document configurations, workflows, and best practices.
**Benefits:** Facilitates onboarding, fosters collaboration, and ensures knowledge retention.
**Platforms:** Use wikis, README files, and collaborative documentation tools.

## FAQ'S

### How does GitOps differ from traditional DevOps?

DevOps provides a holistic approach to software development and operations, emphasizing collaboration and automation across the entire lifecycle. On the other hand, GitOps narrows its focus to continuous delivery and deployment, leveraging Git as the single source of truth for configuration management

## Contact Information 

| Name | Email address | 
|--------|------------|
|  Priyanshu Yadav  | priyanshu.yadav.snaatak@mygurukulam.co  | 

## References
| Links | Description |
|-------|-------------|
| [Gitops with Argocd](https://www.youtube.com/watch?v=1hF-HRq5Mww) | why do we use gitops , what is it , how to use it ( pracitcal ) |
| [Gitops tools](https://github.com/weaveworks/awesome-gitops) | What are different gitops tools we can use |
