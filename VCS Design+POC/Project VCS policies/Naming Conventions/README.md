# Naming Conventions Documentation


| Created/Modified | Version | Author              | Comment         |  Reviewer     |
|-------------------|---------|---------------------|-----------------|-----------------|
| 11-11-2024        | V1      | Pratham Kukudkar | Initial Commit  |                |
| 15-11-2024        | V2      | Pratham Kukudkar | L0               |    Tapan      |
| 3-12-2024        | V2      | Pratham Kukudkar | L1               |    Kirti     |

<img src="https://github.com/user-attachments/assets/cb6dc273-23da-42c6-a50c-b8f32158dafe" alt="hero" width="400"/>


## Table of Contents

- [Introduction](#Introduction)
- [Branch Naming Conventions](#branch-naming-conventions)
- [Tag Naming Conventions](#tag-naming-conventions)
- [Commit Message Conventions](#commit-message-conventions)
- [Features](#key-features)
- [Contact Information](#Contact-information)
- [References](#references)

## Introduction

This documentation provides a comprehensive guide to the naming conventions for branches, tags, and commit messages used in our project. Adhering to these conventions ensures consistency, clarity, and ease of collaboration across the development team.

## Branch Naming Conventions

Branches are used to encapsulate specific features, fixes, or other workstreams. Consistent branch naming makes it easier to understand the purpose and scope of each branch at a glance.


### Types

| **Type**   | **Description**                                                                 |
|------------|---------------------------------------------------------------------------------|
| `feat`     | Introduces a new feature to the codebase.                                       |
| `fix`      | Resolves a bug or an issue in the code.                                         |
| `chore`    | Performs maintenance tasks like refactoring, updating dependencies, or cleanup.|
| `docs`     | Updates or adds documentation.                                                 |
| `test`     | Adds or updates tests to ensure code quality and reliability.                  |
| `hotfix`   | Addresses critical issues that require immediate attention and merging.         |

### Examples

- `feat/1234-add-user-login`
- `fix/5678-fix-login-bug`
- `chore/91011-update-dependencies`
- `docs/1213-update-readme`
- `test/1415-add-login-tests`
- `hotfix/1617-fix-critical-login-issue`

## Tag Naming Conventions

Tags are used to mark specific points in the repository's history, such as releases.

### Examples

- `v1.0.0`: Initial stable release
- `v1.1.0`: New feature added in a backwards-compatible manner
- `v1.1.1`: Bug fix in a backwards

### Commit Message Conventions
Commit messages are crucial for understanding the history and context of changes. A consistent format helps maintain clear project history and facilitates easier code reviews.

### Scope
The scope provides additional context about the section of the codebase affected by the change. It should be consistent with the module or component being modified.

### Subject
The subject is a concise summary of the change. It should be:

Written in imperative, present tense: "change" not "changed" or "changes"
No more than 50 characters long
Should not end with a period

### Body
The body should include:

A detailed explanation of what the commit does
The motivation for the change and its context
Any relevant information that helps understand the change


## Key Features 

| **Feature**                 | **Description**                                                                                   |
|-----------------------------|---------------------------------------------------------------------------------------------------|
| **Consistency**              | Ensures that naming conventions are consistently used across branches, tags, and commit messages. |
| **Clarity**                  | Names should clearly describe the purpose of a branch, tag, or commit.                           |
| **Traceability**             | Allows for tracking the history of changes and releases.                                          |
| **Automation-Friendly**      | Allows automated processes based on branch or tag names (CI/CD).                                 |
| **Versioning**               | Tags and branches follow a predictable versioning system (e.g., Semantic Versioning).            |
| **Meaningful Commit Messages**| Commit messages follow a structured template (e.g., `feat`, `fix`, `docs`).                        |

## Conclusion
Using consistent naming conventions for branches, tags, and commit messages helps keep our project organized and easy to manage. It makes collaboration smoother, allows us to track changes easily, and ensures everyone understands the purpose of each part of the project. Following these guidelines also helps with automating tasks and managing versions more effectively.

## Contact Information

| Name | Email address | 
|--------|------------|
| Pratham Kukudkar   | pratham.kukudkar.snaatak@mygurukulam.co   | 

### References
| Links | Descriptions | 
|--------|------------|
| https://dev.to/shinjithdev/git-good-best-practices-for-branch-naming-and-commit-messages-oj4 | This link explains the naming conventions  | 
