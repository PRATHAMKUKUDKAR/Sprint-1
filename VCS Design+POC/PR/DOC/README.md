![image](https://github.com/user-attachments/assets/ee1156b3-5a6c-43f8-9f6b-6e27504dd8aa)

# PR Documentation

## Author

| Created     |    Version   | Author | Comment | Reviewer |
|:------------------:|:-------------:|:-------------:|:-------------:|:------------------:|
| 17-11-2024   | V1   | Radha | Initial Commit |  |
| 19-11-2024   | V2   | Radha | L0 | Aakash Tripathi |  
| 21-11-2024   | V2   | Radha | L1 | Deepak Nishad | 
| 05-11-2024   | V2   | Radha | L2 | Anjali | 

## Table of Contents
- [Introduction](#introduction)
- [Why Use Pull Requests?](#why-use-pull-requests)
- [What is a Pull Request?](#what-is-a-pull-request)
- [Types of Pull Requests](#types-of-pull-requests)
- [Advantages](#advantages)
- [Disadvantages](#disadvantages)
- [Conclusion](#conclusion)
- [Contact Information](#contact-information)
- [References](#references)

## Introduction
A Pull Request (PR) is a method used in Git-based version control systems (like GitHub or GitLab) to propose changes to a codebase. It is a key part of the collaboration process, allowing developers to submit their changes for review before merging them into the main branch.

## Why Use Pull Requests?

| Feature          | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| **Code Review**   | Facilitates peer reviews to improve code quality.                          |
| **Collaboration** | Encourages teamwork by involving multiple developers in the process.       |
| **Accountability**| Tracks who wrote and reviewed the code.                                    |
| **Version Control**| Prevents conflicts by allowing structured integration.                    |
| **Documentation** | Maintains a history of changes with detailed descriptions.                 |

## What is a Pull Request?
A Pull Request is a request to merge changes from one branch (feature branch) into another branch (main or development). It includes:
- **Code Changes**: New features, bug fixes, or updates.

- **Comments**: Descriptions or discussions around the code changes.

- **Reviews**: Feedback from team members before merging.

## Workflow of a Pull Request
![image](https://github.com/user-attachments/assets/23449d86-22e7-4ba4-8819-3a709c28ed29)

- **Create a Feature Branch:** Developers create a new branch from the base branch to work on a specific task or feature.

- **Make Changes:** Code changes are made on the feature branch.

- **Push to Remote:** Once the changes are committed locally, the branch is pushed to the remote repository.

- **Open a PR:** A PR is opened from the feature branch to the base branch (usually main).

- **Review Process:** Other team members review the changes, request modifications, and discuss improvements.

- **Resolve Conflicts:** If there are conflicts between the feature and base branches, they are resolved.

- **Merge:** Once approved, the PR is merged into the base branch.


## Types of Pull Requests

| Type              | Description                                                                  |
|-------------------|------------------------------------------------------------------------------|
| **Feature PR**    | Introduces new functionality to the codebase.                               |
| **Bug Fix PR**    | Addresses issues or defects in the existing code.                           |
| **Hotfix PR**     | Provides an immediate solution for critical issues in production.           |
| **Refactor PR**   | Improves code structure or performance without altering functionality.       |
| **Chore PR**      | Updates non-functional aspects, e.g., dependencies, configuration.          |

## Advantages of Pull Requests

| Advantage                  | Description                                                                  |
|----------------------------|------------------------------------------------------------------------------|
| **Improved Code Quality**  | Peer reviews catch potential issues.                                        |
| **Team Collaboration**     | Encourages discussions and knowledge sharing.                               |
| **Reduced Conflicts**       | Merges are done systematically.                                            |
| **Audit Trail**            | Provides a clear history of changes and decisions.                          |
| **Early Issue Detection**  | Identifies bugs or design flaws before they escalate.                       |

## Disadvantages of Pull Requests

| Disadvantage               | Description                                                                  |
|----------------------------|------------------------------------------------------------------------------|
| **Time-Consuming**         | Reviews and discussions can delay merges.                                   |
| **Overhead**               | Managing PRs may become complex in large projects.                          |
| **Dependency on Reviewers**| Progress can stall if reviewers are unavailable.                            |
| **Risk of Conflict**       | Long-lived branches may lead to more merge conflicts.                       |

## Conclusion
Pull Requests are an essential part of modern software development, especially in collaborative environments. While they have their challenges, such as review time and potential conflicts, their benefits in ensuring code quality, facilitating collaboration, and maintaining a clean version control system far outweigh the drawbacks. With the proper workflow and integration with tools like CI/CD, PRs enhance the development process and make projects scalable and maintainable.

## Contact information
| Name | Email address | 
|--------|------------|
| Radha  | radha.gondchor.snaatak@mygurukulam.co | 

## References

| Links |
|--------|
| https://www.atlassian.com/git/tutorials/making-a-pull-request|
| https://git-scm.com/docs/git-request-pull|



