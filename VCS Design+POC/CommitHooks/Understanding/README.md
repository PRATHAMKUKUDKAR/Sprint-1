<img src="https://github.com/user-attachments/assets/ee5f6954-99f9-4a4e-a918-e3ea8b40aaf7" alt="Image Description" width="600" height="400">



# Understanding Commit Hooks in Git 

| Created     |    Version   | Author | Comment | Reviewer |
|:------------------:|:-------------:|:-------------:|:-------------:|:------------------:|
| 16-11-2024   | V1   | Pratik | Initial Commit |  |
| 25-11-2024   | V1   | Pratik | L0 | Aakash Tripathi | 
| 26-11-2024   | V1   | Pratik | L1 | Kirti Nehra |



## Table of Contents
- [Introduction](#introduction)
- [Purpose of Commit Hooks](#purpose-of-commit-hooks)
- [Types of Commit Hooks](#types-of-commit-hooks)
- [How to use Commit Hooks](#how-to-use-commit-hooks)
- [FAQ](#faq)
- [Conclusion](#conclusion-of-commit-hooks)
- [Contact Information](#contact-information)
- [References](#references)
  

## Introduction

**Git Hooks** are scripts that Git automatically executes before or after specific events occur in the Git workflow. These hooks are installed in a project's `.git/hooks` directory and are customizable to automate tasks like running tests, formatting code, sending notifications, or preventing certain actions.

## Purpose of Commit Hooks

The primary purpose of commit hooks is to maintain the quality and consistency of code throughout the development lifecycle. Some common purposes include:
Automating Code Quality Checks:
| **Purpose**                                 | **Description**                                          |
|------------------------------------------------|------------------------------------------------------------|
| **Automating Code Quality Checks** | Automatically running linters, formatters, or tests before a commit. |
|**Ensuring Consistent Commit Messages**| Enforcing commit message standards for better collaboration and history readability.|
|**Preventing Common Mistakes**|Blocking commits with errors or sensitive data (e.g., API keys, credentials)|
|**Streamlining Team Workflows**|Reducing manual tasks by automating repetitive actions.|

## Types of Commit Hooks
Git supports several types of hooks for different stages of the commit process. The following are the primary commit hooks:
| **Types**                                 | **Description**                                          |
|------------------------------------------------|------------------------------------------------------------|
|  **Pre-Commit Hook** |  Triggered before the commit is created. Commonly used to run tests, lint code, or check for trailing spaces. |
|**Prepare-Commit-Message Hook**| Triggered before the commit message editor opens.Can be used to automatically add information to a commit message (e.g., ticket numbers).|
|**Commit-Message Hook**|Triggered after the commit message is created but before the commit is finalized. Used to validate commit messages against a regex pattern or check for certain keywords.|
|**Post-Commit Hook**|Triggered after the commit has been created.Commonly used to notify a team or update a bug-tracking system.|

## How to use Commit Hooks
To use commit hooks in Git, first navigate to the .git/hooks directory within your repository, where Git stores sample hook scripts. Choose the appropriate hook (such as pre-commit or commit-msg), and create a script with the desired commands (e.g., running tests or checking code style). Make the script executable by using the chmod +x command. When a commit action is performed, Git will automatically execute the corresponding hook script. This helps enforce consistent practices, such as validating commit messages or preventing flawed code from being committed. Hooks can be customized to fit the specific needs of your project or workflow.


---

## FAQ

### 1. What are some common use cases for commit hooks?
Commit hooks are often used to automate code checks, enforce commit message standards, run tests, and prevent sensitive data from being committed. They can also trigger notifications, streamline team workflows, and integrate with bug-tracking systems.

### 2. How do I disable a commit hook temporarily?
To temporarily disable a hook, rename the file in the `.git/hooks` directory by changing its extension or moving it to another folder. Renaming, for example, `pre-commit` to `pre-commit.bak` will prevent Git from running it. To re-enable, rename it back.

### 3. Can I use the same commit hooks across multiple repositories?
Yes! You can create a global hook template directory to share commit hooks across repositories. Set up a global template directory with `git config --global init.templatedir <path>`, place your hooks there, and run `git init` in each repo to apply them.

### 4. How can I share commit hooks with my team?
For team sharing, add hook scripts to the repository (e.g., in a `hooks` directory) and use automation tools like Husky or add setup instructions in documentation. You can also create a script that copies hooks into each team member’s `.git/hooks` directory.

### 5. Do commit hooks apply to GitHub and other remote platforms?
No, commit hooks only run locally on your machine. However, you can enforce similar checks in remote repositories by configuring CI/CD pipelines with tools like GitHub Actions, GitLab CI, or Jenkins to enforce rules on pull requests or pushes.

## Conclusion
Commit hooks (or Git hooks) are a powerful feature provided by Git that enables developers to automate tasks during various stages of the Git workflow. By providing custom scripts that execute automatically at key points in the commit lifecycle (like before or after a commit), commit hooks help enforce project standards, improve code quality, and streamline development processes.

## Contact Information
For more information, feedback, or assistance, feel free to contact us:
| Name | Email address|
|------|---------------------|
| Pratik | pratik.gondkar.snaatak@mygurukulam.co |


## References
| Links                                             | Descriptions                                                    |
|---------------------------------------------------|-----------------------------------------------------------------|
|https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks |Git Documentation - Customizing Git|
|https://git-scm.com/book/en/v2 | Pro Git Book - Git Hooks|
