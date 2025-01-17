# Git Flow

<img src="https://github.com/user-attachments/assets/663808fd-b9cd-4174-84e0-a453fede1713" alt="Branching Strategy Diagram" width="600" height="300">

## Author

| Created     |    Version   | Author | Comment | Reviewer |
|:------------------:|:-------------:|:-------------:|:-------------:|:------------------:|
| 13-11-2024   | V1   | Pratik | Initial Commit |  |
| 15-11-2024   | V1   | Pratik | L0 Feedback | Tapan |
| 18-11-2024   | V2   | Pratik | L0 | Tapan  |
| 20-11-2024   | V2   | Pratik | L1 Feedback | Shashi Kumar |
| 20-11-2024   | V3   | Pratik | L1  | Shashi Kumar |
| 04-12-2024 | V3 |  pratik | L2 | anjali kaushal |

## Table of Contents
- [Introduction](#introduction)
- [Why Use Git Flow?](#why-use-git-flow)
- [Git Flow](#git-flow)
    - [Feature Branches](#feature-branches)
    - [Develop Branch](#develop-branch)
    - [Release Branches](#release-branches)
    - [Hotfix Branches](#hotfix-branches)
- [Advantages of Git Flow](#advantages-of-git-flow)
- [Disadvantages of Git Flow](#disadvantages-of-git-flow)
- [Conclusion](#conclusion)
- [Contact Information](#contact-information)
- [References](#references)

## Introduction
Git Flow is a branching strategy for Git, a popular version control system. It provides a set of guidelines to manage and organize branches in a repository, making it easier to collaborate on complex projects. Vincent Driessen first proposed Git Flow in 2010, and it has since become a widely adopted standard in software development.

## Why Use Git Flow?
Using Git Flow helps maintain a clear and structured workflow, especially in projects with multiple contributors. It defines a strict branching model designed around the project release. Git Flow is particularly useful for teams that have a planned release cycle and can benefit from a structured approach to managing features, releases, and hotfixes.

## Git Flow
Git Flow involves several types of branches, each with a specific purpose. The main branches are:

### Feature Branches
| **Attribute**         | **Description**                                                                                       |
|-----------------------|-------------------------------------------------------------------------------------------------------|
| **Purpose**           | Used to develop new features for the upcoming or a distant future release.                           |
| **Naming Convention** | `feature/{feature-name}`                                                                               |
| **Branching Off**     | `develop`                                                                                             |
| **Merging Back**      | `develop`                                                                                             |

<img src="https://github.com/user-attachments/assets/52f333dc-2733-46bd-880e-eeb682adea0e" alt="Feature Branch Diagram" width="600" height="300">

### Develop Branch
| **Attribute**         | **Description**                                                                 |
|-----------------------|---------------------------------------------------------------------------------|
| **Purpose**           | Serves as an integration branch for features and is the main branch where the combination of all features is tested. |
| **Naming Convention** | `develop`                                                                       |
| **Branching Off**     | `main`                                                                          |
| **Merging Back**      | `main`                                                                          |

<img src="https://github.com/user-attachments/assets/4708e802-b176-4afd-970d-a89312d0e249" alt="Develop Branch Diagram" width="600" height="300">

### Release Branches
| **Attribute**         | **Description**                                                                                                            |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| **Purpose**           | Used to prepare a new production release. Allows for last-minute minor bug fixes and preparing meta-data for a release.    |
| **Naming Convention** | `release/{version}`                                                                                                        |
| **Branching Off**     | `develop`                                                                                                                  |
| **Merging Back**      | `main` and `develop`                                                                                                       |

<img src="https://github.com/user-attachments/assets/25b030ff-8c3a-40d4-b160-2a75f885571b" alt="Release Branch Diagram" width="600" height="300">

### Hotfix Branches
| **Attribute**         | **Description**                                                                                                             |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **Purpose**           | Used to quickly patch production releases. Arises from the necessity to act immediately upon an undesired state of a live production version. |
| **Naming Convention** | `hotfix/{version}`                                                                                                         |
| **Branching Off**     | `main`                                                                                                                     |
| **Merging Back**      | `main` and `develop`                                                                                                       |

<img src="https://github.com/user-attachments/assets/0589a867-cf2d-4e72-ae67-23412e3bd1f7" alt="Hotfix Branch Diagram" width="600" height="300">

### Advantages and Disadvantages of Git Flow

| **Advantages of Git Flow**                                      | **Disadvantages of Git Flow**                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------|
| **Structured Workflow:** Provides a clear process for managing branches. | **Complexity:** Can be overly complex for small projects or small teams.   |
| **Parallel Development:** Supports multiple parallel developments and easy integration. | **Overhead:** Involves more overhead in terms of branch management and merging. |
| **Release Isolation:** Ensures that release preparation is isolated from new development. | **Learning Curve:** Requires developers to understand and follow the branching strategy strictly. |
| **Hotfix Management:** Allows for quick fixes on the main branch without disturbing ongoing work. | |



## Conclusion
Git Flow is a structured branching strategy ideal for projects with planned release cycles and multiple contributors. While it adds some complexity, it ensures a clear workflow for features, releases, and hotfixes. For simpler workflows, consider using a feature branch model, which focuses on creating isolated branches for new features, reducing overhead while maintaining clarity.

## Contact information

| Name | Email address | 
|--------|------------|
| Pratik   | pratik.gondkar.snaatak@mygurukulam.co | 


## References 
|links | Description |
|-------|------------|
|https://nvie.com/posts/a-successful-git-branching-model/|For Git branching model |
| https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow| For Gitflow workflow|
|https://danielkummer.github.io/git-flow-cheatsheet/|For git-flow cheatsheet|

