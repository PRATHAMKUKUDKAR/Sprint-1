# VCS Notification Documentation


| Created/Modified | Version | Author              | Comment         |  Reviewer     |
|-------------------|---------|---------------------|-----------------|-----------------|
| 11-11-2024        | V1      | Pratham Kukudkar | Initial Commit  |                 |
| 15-11-2024        | V2      | Pratham Kukudkar | L0             |    Tapan            |
| 3-12-2024        | V2      | Pratham Kukudkar | L1               |    Kirti    |


## Table of Contents

- [Introduction](#introduction)
- [Pre-requisites](#pre-requisites)
- [Step-by-Step Setup Guide](#step-by-step-setup-guide)
- [Best Practices](#best-practices-for-setting-up-and-managing-vcs-notifications)
- [Conclusion](#conclusion)
- [Contact Information](#contact-information)
- [References](#references)

---

## Introduction
Version Control Systems (VCS) are essential tools in modern software development, allowing teams to manage changes to source code over time. Notifications in VCS help keep team members informed about changes, updates, and activities within repositories. This document provides a comprehensive guide on setting up and managing VCS notifications effectively.

## Pre-requisites
Before setting up the VCS Notification System, ensure you have the following:

- A version control system (e.g., GitHub, GitLab, Bitbucket) installed and configured.
- Access to a repository on a VCS hosting platform (e.g., GitHub, GitLab, Bitbucket).
- Administrative or sufficient permissions to configure notification settings.
- A communication platform for notifications (e.g., Slack, Microsoft Teams, email) for receiving notifications.
- Basic knowledge of VCS and webhooks.

## Step-by-Step Setup Guide

## 1. Email Notifications

### Step 1: GitHub's Notification Settings

1. **Navigate to Notification Settings**:
    - Go to GitHub's notification settings.
  ![Screenshot from 2024-11-20 10-35-01](https://github.com/user-attachments/assets/867e01f2-f470-4e30-a525-0e896f89545f)

2. **Select Activities**:
    ![Screenshot from 2024-11-20 10-37-33](https://github.com/user-attachments/assets/fdd6c232-aeeb-4c51-bc12-14c1f0a28d68)
4. **Customize Preferences**:
    - Adjust your notification preferences as needed.

  
## Best Practices for Setting Up and Managing VCS Notifications

| Best Practice            | Purpose                                                                       | Action                                                                                      |
|--------------------------|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| Regular Testing          | Ensure notifications work correctly.                                            | Regularly test by making commits or pull requests to verify notifications.                   |
| Security                 | Protect sensitive information (e.g., webhook URLs, email credentials).          | Securely store credentials as secrets and limit access to trusted personnel.                  |
| Customization            | Tailor notifications to team needs.                                              | Customize settings to deliver relevant information without unnecessary noise.                |
| Selective Notifications  | Avoid overload by focusing on important events.                                  | Enable notifications only for critical activities like major changes or urgent issues.        |
| Structured Messages      | Ensure notifications are clear and informative.                                 | Format messages with essential details like commit messages, authors, and branches.          |
| Monitor and Adjust       | Improve notification effectiveness over time.                                   | Regularly review settings based on team feedback and adjust for better communication flow.    |



## Conclusion
Setting up a VCS Notification System enhances team collaboration and keeps everyone informed of important changes in the codebase. By following the steps outlined in this guide and adhering to best practices, you can ensure a smooth and efficient notification system that supports your development workflow.

## Contact Information

| Name          | Email address           |
|---------------|-------------------------|
| Pratham Kukudkar | pratham.kukudkar.snaatak@mygurukulam.co |

## References

| Reference                                                               | Name                       |
|-------------------------------------------------------------------------|----------------------------|
| https://support.atlassian.com/bitbucket-cloud/docs/manage-webhooks/ | Bitbucket Webhooks         |
| https://api.slack.com/messaging/webhooks     | Slack Incoming Webhooks    |
| https://docs.github.com/en/developers/webhooks-and-events/webhooks | GitHub Webhooks            |
| https://docs.gitlab.com/ee/user/project/integrations/webhooks.html | GitLab Webhooks            |
