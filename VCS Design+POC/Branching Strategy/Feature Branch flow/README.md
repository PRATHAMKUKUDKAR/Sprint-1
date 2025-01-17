# Branching Strategy | Feature Branch Workflow

| Created     |    Version   | Author | Comment | Reviewer |
|:------------------:|:-------------:|:-------------:|:-------------:|:------------------:|
| 11-11-2024   | V1   | Pritam Kondapratiwar | Initial Commit | Tapan shahu
| 12-11-2024 | V2 | Pritam Kondapratiwar | L1  |  Deepak Nishad  
| 17-11-2024 | V3 |  Pritam Kondapratiwar | L2 |    |         |  

## Table of Contents



- [Introduction](#introduction)
- [Why Feature Branch Workflow](#why-feature-branch-workflow)
- [Feature Branch Workflow](#feature-branch-workflow)
- [Advantages](#advantages)
- [Disadvantages](#disadvantages)
- [Conclusion](#conclusion) 
- [Contact Information](#contact-information)
- [Refrences](#refrences)


## Introduction

> Branching strategies are essential for effective version control and efficient software development. The Feature Branch Workflow means that whenever a new feature is being developed, it should be done in a separate branch instead of the main branch. This way, multiple people can work on the feature without affecting the main code. 

## Why Feature Branch Workflow ?

The Feature Branch Workflow is designed to streamline the development process by allowing individual features to be developed in isolated branches. This approach offers several benefits:

>- **Isolation of Changes:**  Developers can work on features independently without affecting the main codebase.
>- **Easier Collaboration:**  Developers work on feature branches and only merge to the main branch after review and approval. Pull requests allow team members to review, discuss, and ensure code quality.
>- **Parallel Development:** Developers can work on multiple features at the same time, each in its own branch.


## Feature Branch Workflow ?

**1. Create a New Branch:**
When starting work on a new feature, create a new branch from the main branch (often main or master).
![Alt](https://images.prismic.io/bunnyshell-blog/145a8d27-2e0b-46d7-81d6-c646718b96c8_Feature%20branch.png?ixlib=gatsbyFP&auto=compress%2Cformat&fit=max)

**2. Develop the Feature:**
Make changes and commit them to the feature branch. Use descriptive commit messages to document your changes.

**3. Push the Feature Branch:**
Push the feature branch to the remote repository to share your work with the team.

**4. Open a Pull Request:**
When the feature is complete, open a pull request (PR) to merge the feature branch into the main branch. This step typically involves code review and testing.

**5. Review and Merge:**
Review the PR, address any feedback, and ensure all tests pass. Once approved, merge the feature branch into the main branch.

![Alt](https://buddy.works/blog/images/feature-branch.png)

**6. Delete the Feature Branch:**
After merging, delete the feature branch to keep the repository clean.
 

## Advantages 

|  Advantages  | Description
|:------------------:|:--------------------------:|
| Improved Code Quality | Features are developed in isolation, developers can write and test code without the risk of introducing bugs or conflicts into the main branch.
| Simplified Bug Fixes |     If a bug is found in a specific feature, developers can focus on fixing it in the respective feature branch without worrying about affecting other features.

## Disadvantages 
| Disdvantages  |   Description
|:---------------:|:---------------:|
| Merge Conflicts  | When developers work on separate branches, their code can get out of sync with the main code. This can cause big conflicts when they try to merge everything back together.
|Continuous Merging|Constantly merging changes from the main branch to keep the feature branch up to date can be time-consuming.|
| Increased Overhead|Managing multiple branches can be cumbersome and requires disciplined practices.|

## Conclusion

>The Feature Branch Workflow is a popular and useful approach in software development, but it comes with some challenges, like extra work, merge conflicts, and delayed feedback. Managing multiple branches can be tricky, and it requires disciplined practices like regular syncing, frequent merging, clear branch names, and good communication.

## Contacts
|    NAME           |   Email Address                       |
|:-----------------:|:-------------------------------------:|
|Pritam Kondapratiwar| 	pritam.pratiwar.snaatak@mygurukulam.co

## References

| Website name |   Link |
|:------------------:|:-------------------:|
|www.atlassian.com|  https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow 
|www.craftquest.com | https://craftquest.io/guides/git/git-workflows/feature-branch-workflow
