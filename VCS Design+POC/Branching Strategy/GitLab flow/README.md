![image](https://github.com/user-attachments/assets/12357653-d5c2-4520-8943-837f9ff2c74f)

# GitLab Flow

| Created     |    Version   | Author | Comment | Reviewer |
|:------------------:|:-------------:|:-------------:|:-------------:|:------------------:|
| 12-11-2024   | V1   | Pratik | Initial Commit |  |
| 15-11-2024   | V1   | Pratik | L0  | Tapan |
| 20-11-2024   | V1   | Pratik | L1 Feedback | Shashi Kumar |
| 20-11-2024   | V2   | Pratik | L1  | Shashi Kumar |
| 05-12-2024   | V2   | Pratik | L2 Feedback  | Rohit Kumar |
| 05-12-2024   | V3   | Pratik | L2  | anjali kaushal |



## Table of Contents
- [Introduction](#introduction)
- [Why GitLab](#why-gitlab)
- [GitLab Flow](#gitlab-flow)
   - [Production Branch](#production-branch)
   - [Feature Branches](#feature-branches)
   - [Environment-based Branches](#environment-based-branches)
   - [Merge Requests (MR)](#merge-requests-mr)
- [Advantages / Disadvantages](#advantages--disadvantages)
- [Conclusion](#conclusion)
- [Contact Information](#contact-information)
- [References](#references)

## Introduction

GitLab Flow is a Git branching model optimized specifically for working with the GitLab platform. It helps manage various branches and environments efficiently, such as feature branches, main branches, and production branches.

## Why GitLab

The reason for using GitLab Flow is that it simplifies and optimizes CI/CD pipelines, enabling teams to deploy production-ready code and bug fixes smoothly. It focuses on allowing developers to safely and quickly release code directly into the live environment.


## GitLab Flow

| Core Component     | Description                                                                   |
|--------------------|-------------------------------------------------------------------------------|
| Production Branch        | A primary branch that always represents production-ready code.          |
| Feature Branches   |  Separate branches created for new features or changes, which are tested and then merged into the main branch. |
| Environment-based Branches   |Separate branches for development and production environments, making the release and testing process clear and organized.   |
| Merge Requests (MR)   | Used to review and approve changes before merging them, ensuring quality control and collaboration.     |



###  GitLab flow 
#### Production Branch
The production branch is the primary branch in GitLab Flow, containing only production-ready code. This branch is stable and reflects the live environment. Any code that has been thoroughly tested and approved gets merged into the production branch, ensuring that the latest, stable version of the software is ready for deployment. This branch is crucial for maintaining a reliable production environment and helps prevent unstable code from reaching end users.

![image](https://github.com/user-attachments/assets/72b3d713-6003-46d2-9689-b7720d18a933)


#### Feature Branches
Feature branches are temporary branches created to develop new features, enhancements, or specific changes. These branches allow developers to work on new functionality without disrupting the main branch. Once the new code is developed and tested within the feature branch, it undergoes review and is merged into the main branch. This approach supports parallel development, where multiple team members can work on different features simultaneously without conflict.

![image](https://github.com/user-attachments/assets/0398bb63-4106-48ba-91d1-6318c661980b)


#### Environment-based Branches
Environment-based branches, such as development, staging, and production, help manage code deployment in multiple environments. Code moves progressively through these branches as it passes testing and review stages, ensuring a controlled and step-by-step release process. For example, the development branch can hold the latest code for internal testing, while the staging branch mirrors a near-production environment for more thorough testing before final deployment. This structure improves testing, minimizes risk, and ensures that each environment serves a clear purpose.

![image](https://github.com/user-attachments/assets/b2b14dae-af4e-4293-8795-7e01427a12f3)




#### Merge Requests (MR)

Merge Requests (MR) are essential in GitLab Flow for reviewing and approving changes before they’re integrated into a branch, such as the main or production branch. MRs allow team members to examine code changes, suggest improvements, and ensure the quality of the code before it is merged. This collaborative review process helps maintain code quality and encourages feedback, reducing the chances of bugs and improving the overall reliability of the software.

![image](https://github.com/user-attachments/assets/7d6f402c-f1ba-433a-a872-0230c7d8d48c)


## Advantages / Disadvantages
| **Advantages**                                      | **Disadvantages**                                    |
|-----------------------------------------------------|------------------------------------------------------|
| **Easy Collaboration**: Improves coordination between developers and testers. | **Setup Complexity**: The setup and branching structure can be complex for small teams. |
| **Continuous Delivery**: Code can be safely and easily deployed. | **Learning Curve**: Beginners may take time to understand the complexity of GitLab Flow. |
| **Customizable**: Teams can customize the flow according to their use case. | **Environment Constraints**: Setting up and maintaining multiple environments requires extra effort. |
| **Clear Workflow**: Each branch and environment has a clear purpose, reducing confusion. | |


## Conclusion

GitLab Flow is an efficient branching model designed to work with GitLab CI/CD. It provides a structured and organized workflow, making it possible to deploy production code safely and quickly. However, it can be somewhat complex for small teams.
## Contact Information

| Name          | Email Address                          | 
| ------------- |:--------------------------------------:|
| Pratik      | pratik.gondkar.snaatak@mygurukulam.co |

## Refrences 

| Links          | Description                          | 
| ------------- |:--------------------------------------:|
|    https://docs.gitlab.co.jp/ee/topics/gitlab_flow.html  | For Information pupose|
|  https://www.perforce.com/manuals/gitswarm-ee/workflow/gitlab_flow.html  | For Pros and Cons information pupose|
|   https://www.perforce.com/manuals/gitswarm-ee/workflow/gitlab_flow.html  | Diagram & strategy|
|   https://www.gitkraken.com/learn/git/best-practices/git-branch-strategy  | Diagram and strategy|
