# Commit Hooks Recommendations 

| **Created**     | **Version**   | **Author** | **Comment**       | **Reviewer**      |
|:----------------:|:-------------:|:-----------:|:------------------:|:-----------------:|
| 17-11-2024       | V1            | Sahil        | Initial Commit   |      Tapan             |
|                  | V2            | Sahil         | L1 Review        |         Kirti          |
|                  | V3            | Sahil        | L2 Review        |                   |
        

## Table of Contents
- [Introduction](#introduction)
- [Overview of Commit Hooks](#overview-of-commit-hooks)
  - [Client-Side Hooks](#client-side-hooks)
  - [Server-Side Hooks](#server-side-hooks)
- [Recommended Commit Hooks](#recommended-commit-hooks)
  - [Pre-Commit Hooks](#pre-commit-hooks)
  - [Commit-msg Hooks](#commit-msg-hooks)
  - [Pre-Push Hooks](#pre-push-hooks)
- [Conclusion](#conclusion)
- [Contact Information](#contact-information)
- [References](#references)

## Introduction 
Commit hooks are scripts that run automatically during the Git workflow. They enforce coding standards, automate repetitive tasks, and improve collaboration. By implementing the appropriate hooks, teams can enhance code quality, prevent errors, and streamline development workflows. This document provides a simplified and concise recommendation for various commit hooks.

---

## Overview of Commit Hooks

### Client-Side Hooks
Client-side hooks run locally on developers' machines to verify code quality and standards before pushing to a remote repository.

| Hook Type           | Purpose                                                       | Examples                                                           |
|---------------------|--------------------------------------------------------------|--------------------------------------------------------------------|
| **Pre-commit**      | Checks code formatting, linting, or runs tests before a commit. | Code formatting with Prettier, linting with ESLint.               |
| **Prepare-commit-msg** | Populates commit messages with templates or metadata.          | Adds issue numbers to commit messages automatically.              |
| **Commit-msg**      | Validates commit messages before finalizing the commit.       | Enforces message format with Commitlint.                          |
| **Post-commit**     | Executes tasks like notifications or CI triggers post-commit. | Sends Slack alerts or updates Jira with commit information.       |
| **Pre-push**        | Runs tests or verifies branch policies before pushing code.   | Ensures tests pass before pushing to remote repositories.          |

### Server-Side Hooks
Server-side hooks enforce repository-level policies and ensure compliance with project standards.

| Hook Type           | Purpose                                                       | Examples                                                           |
|---------------------|--------------------------------------------------------------|--------------------------------------------------------------------|
| **Pre-receive**     | Blocks non-compliant changes before applying them.            | Rejects commits that do not pass tests.                           |
| **Update**          | Enforces branch-specific policies.                            | Ensures only certain users can push to protected branches.         |
| **Post-receive**    | Triggers deployment or notifications after a successful push. | Deploys code or triggers Jenkins pipelines.                       |

---

## Recommended Commit Hooks

### Pre-Commit Hooks
Run before a commit is finalized. These ensure code quality and compliance.

| **Check**             | **Purpose**                                     | **Tool**                                   | **Why Use It?**                                |
|-----------------------|-------------------------------------------------|-------------------------------------------|------------------------------------------------|
| **Code Formatting**   | Enforces consistent code style across the team. | `Prettier` (JavaScript/TypeScript), `Black` (Python) | Prevents unnecessary formatting changes, reducing code review friction. |
| **Linting**           | Detects syntax errors and enforces coding standards. | `ESLint` (JavaScript/TypeScript), `Pylint` (Python) | Avoids potential bugs and maintains coding standards. |
| **Running Basic Tests** | Ensures critical functionality works before committing. | `Jest` (JavaScript/TypeScript), `Pytest` (Python) | Prevents committing code that breaks existing functionality. |

---

### Commit-msg Hooks
Run after entering a commit message to ensure it follows a standardized format.

| **Check**                      | **Purpose**                                  | **Tool**          | **Why Use It?**                                |
|--------------------------------|----------------------------------------------|-------------------|------------------------------------------------|
| **Enforcing Commit Message Format** | Ensures consistent and meaningful commit messages. | `Commitlint`      | Helps maintain a clear and traceable commit history. |

---

### Pre-Push Hooks
Run before code is pushed to a remote repository, verifying that the codebase is stable.

| **Check**              | **Purpose**                                     | **Tool**                                   | **Why Use It?**                                |
|------------------------|-------------------------------------------------|-------------------------------------------|------------------------------------------------|
| **Running Tests**      | Ensures all tests pass before pushing changes.  | `Jest` (JavaScript/TypeScript), `Pytest` (Python) | Avoids breaking the build on the remote repository. |
| **Code Coverage Checks** | Verifies that code coverage meets the required threshold. | `Coverage.py` (Python), Integrated Jest reports (JavaScript/TypeScript) | Prevents untested code from being pushed.      |


## Conclusion 
The recommended commit hooks, including Pre-commit, Commit-msg, and Pre-push, are crucial for maintaining code quality, consistency, and stability during development. Pre-commit hooks catch issues like formatting errors and failed tests early in the process, saving time and effort during code reviews. Commit-msg hooks enforce clear and standardized commit messages, ensuring a traceable and collaborative workflow. Pre-push hooks verify that tests and code coverage requirements are met, preventing unstable code from being pushed to the repository.

These hooks were chosen for their significant impact on workflow efficiency and code reliability. Other hooks, such as Prepare-commit-msg or server-side hooks, are valuable in specific contexts but less critical for day-to-day development tasks, making the selected hooks the most practical and impactful choices.

---

## Contact Information 
| Name              | Email Address                            |
|-------------------|------------------------------------------|
|  Sahil  |  [sahil.pathania.snaatak@mygurukulam.co](mailto:sahil.pathania.snaatak@mygurukulam.co) | 

---

## References 

| **Resource**                      | **Description**                                                                                     | **Link**                                 |
|-----------------------------------|-----------------------------------------------------------------------------------------------------|------------------------------------------|
| **Git Hooks Documentation**       | Official documentation detailing the various Git hooks and their usage.                            | [Git Hooks Documentation](https://git-scm.com/docs/githooks) |
| **Understanding Git Hooks**       | A concise guide explaining the types of Git hooks and their practical applications.                | [Understanding Git Hooks](https://tinyurl.com/3822mhpr) |
| **Unstop Guide to Git Hooks**     | Overview of Git hooks with tips on how to integrate them effectively in development workflows.      | [Unstop Guide to Git Hooks](https://unstop.com/blog/git-hooks) |
| **DevDynamics on Commit Hooks**   | In-depth blog discussing the benefits and implementation of commit hooks in modern development.     | [DevDynamics on Commit Hooks](https://devdynamics.ai/blog/untitled-2/) |
