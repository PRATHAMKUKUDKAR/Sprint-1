# PR (Pull Request) - POC 

##  Author

| Created     |    Version   | Author | Comment | Reviewer |
|:------------------:|:-------------:|:-------------:|:-------------:|:------------------:|
| 21-11-2024   | V1   | Radha | Initial Commit |  |
| 22-11-2024   | V2   | Radha | L0 | Aakash Tripathi |  
| 24-11-2024   | V2   | Radha | L1 | Deepak Nishad | 
| 05-11-2024   | V2   | Radha | L2 | Anjali | 

## Table of Contents
- [Introduction](#introduction)
- [Why Use Pull Requests?](#why-use-pull-requests)
- [What is a Pull Request?](#what-is-a-pull-request)
- [Workflow of a Pull Request](#workflow-of-a-pull-request)
- [PR Creation Steps](#pr-creation-steps)
- [PR Rules and Guidelines](#pr-rules-and-guidelines)
- [Types of Pull Requests](#types-of-pull-requests)
- [Advantages](#advantages)
- [Disadvantages](#disadvantages)
- [Conclusion](#conclusion)
- [Contact Information](#contact-information)
- [References](#references)
---
## Introduction
A Pull Request (PR) is a feature in Git-based systems that lets developers propose, review, and discuss code changes before merging them into the main branch. It ensures collaboration, code quality, and a clear change audit trail.

## Why Use Pull Requests?

### Feature Description

| **Feature**      | **Description**                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Code Review**  | Pull Requests facilitate code reviews by enabling team members to review, comment, and suggest improvements on changes before they are merged, which helps catch potential issues early and ensures high-quality code. |
| **Collaboration**| PRs encourage collaboration by allowing multiple developers to work on different features or fixes in parallel, making it easier to integrate their work into the main codebase. |
| **Accountability**| Since each PR is linked to a specific author and reviewed by others, it provides a clear record of who made changes and who approved them, promoting accountability within the team. |
| **Version Control**| PRs streamline the process of managing and merging changes, preventing conflicts by providing a structured approach to integrating code. |
| **Documentation**| Every PR includes a description of the changes made, which serves as valuable documentation for the team to understand the evolution of the project over time. |


## What is a Pull Request?
A Pull Request (PR) is a request to merge changes from one branch (typically a feature or bug-fix branch) into another, usually the main or development branch. It serves as a way to propose changes to a codebase, allowing team members to review the code before it is merged. When a developer completes a task or feature, they create a PR, which includes a summary of the changes made, such as new features, bug fixes, or code improvements. The PR then undergoes a review process, where other team members can comment, request changes, and approve or reject the proposed updates. Once the PR is approved, the changes are merged into the base branch, ensuring that only thoroughly reviewed and tested code is integrated into the main project.

## Workflow of a Pull Request

![image](https://github.com/user-attachments/assets/7faac0b6-20e7-4817-9b1f-03ae2fd357c0)


## PR Creation Steps
1. **Create a Branch**

   First, make a new branch from the main or development branch to work on a specific feature or fix. Name the branch clearly, like `feature/add-login`.
   ```
   git checkout -b feature/add-login
   ```

2. **Make Changes**

    Now, add the necessary changes in your code (e.g., adding a login feature). After that, add the files you changed to the staging area.
    ```
    git add .
    ```
3. **Commit Changes**

    Save your changes with a clear message. The message should explain what feature or fix you’ve added.
    ```
    git commit -m "added functionality"
    ```

4. **Push the Branch**

    Push your branch to the remote repository so others can see and review it.
    ```
    git push origin feature/add-login
    ```
5. **Open a Pull Request**

    Go to your project on GitHub or GitLab and open a new pull request. Choose your branch and the branch you want to merge it into (usually main or development). Add a short description of the changes.

6. **Request Reviews and Fix Comments**

    Ask your team members to review your PR. If they suggest changes, make them and update the PR.

7. **Merge the Pull Request**

    Once your PR is approved, merge it into the main branch. Use squash and merge to keep your project history clean.

## PR Rules and Guidelines
### Branch Naming

| **Branch Type**     | **Naming Convention**          | **Example**                        |
|---------------------|---------------------------------|------------------------------------|
| **Feature Branch**   | `feature/`                      | `feature/add-login`                |
| **Bugfix Branch**    | `bugfix/`                       | `bugfix/fix-login-error`           |
| **Hotfix Branch**    | `hotfix/`                       | `hotfix/fix-critical-bug`          |

### Commit Messages

| **Type**  | **Prefix** | **Example**                                | **Description**                                             |
|-----------|------------|--------------------------------------------|-------------------------------------------------------------|
| **Feature** | `feat:`    | `feat: added login functionality`           | Use for adding new features or major changes.                |
| **Bug Fix** | `fix:`     | `fix: corrected login issue`               | Use for fixing bugs or resolving issues in the codebase.     |
| **Documentation** | `docs:` | `docs: updated README with new setup instructions` | Use for changes or updates to documentation files.          |

### Code Reviews

| **Checklist**                                                       | **Description**                                                                                           |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| **Reviewed by a team member**                                       | Ensure that the code has been reviewed by at least one team member before merging.                         |
| **Passes checks**                                                   | All commits should pass checks such as linting, unit tests, and integration tests before merging.          |
| **Address reviewer feedback**                                       | Ensure that any requested changes or improvements from reviewers are addressed before merging.             |


## Types of Pull Requests

| **Type**           | **Description**                                                      |
|--------------------|----------------------------------------------------------------------|
| **Feature PR**     | Introduces new functionality or features to the codebase.            |
| **Bug Fix PR**     | Addresses defects or issues in the existing codebase.                |
| **Hotfix PR**      | Provides an urgent solution to critical issues, often in production. |
| **Refactor PR**    | Improves code structure, readability, or performance without changing functionality. |
| **Chore PR**       | Updates non-functional aspects, such as dependencies, configuration, or tooling. |


## Advantages

| **Advantage**           | **Description**                                                                |
|-------------------------|--------------------------------------------------------------------------------|
| **Improved Code Quality** | Peer reviews help spot issues early and ensure better code quality.            |
| **Team Collaboration**   | Encourages knowledge sharing and teamwork among developers.                    |
| **Reduced Conflicts**    | Merges are done systematically, reducing the likelihood of conflicts.          |
| **Audit Trail**          | Provides a clear history of changes and decisions made during the review process.|
| **Early Issue Detection**| Bugs or design flaws can be detected early, preventing larger problems later.   |

## Disadvantages

| **Disadvantage**         | **Description**                                                                |
|--------------------------|--------------------------------------------------------------------------------|
| **Time-Consuming**        | Reviews can delay merges and add extra time to the development process.        |
| **Overhead**              | Managing PRs and reviews may become complex, especially in large projects.      |
| **Dependency on Reviewers**| Progress can stall if key reviewers are unavailable or slow to respond.       |
| **Risk of Conflict**     | Long-lived branches may lead to merge conflicts, especially with frequent changes.|


## Conclusion 
Pull Requests (PRs) are key for team collaboration and ensuring code quality in software projects. They let teams review, test, and discuss changes before merging, helping to catch issues early and maintain a clear record of updates. While they take time, PRs greatly improve the development process.By following best practices and maintaining a proper PR workflow, teams can ensure a smooth and effective development process.


## Contact Information

| **Name**  | **Email**                                  |
|------------|---------------------------------------------------|
| Radha   |   radha.gondchor.snaatak@mygurukulam.co        |



## References

| **Reference**                                    | **Description**                                         |
|--------------------------------------------------|---------------------------------------------------------|
| [Atlassian Guide to Pull Requests](https://www.atlassian.com/git/tutorials/making-a-pull-request) | Comprehensive guide on creating and managing pull requests in Git. |
| [Git Documentation on Pull Requests](https://git-scm.com/docs/git-request-pull) | Official Git documentation for the `git-request-pull` command. |



