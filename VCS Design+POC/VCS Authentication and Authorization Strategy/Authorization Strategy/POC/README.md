# POC to Setup Authorization


| Created     |    Version   | Author | Comment | Reviewer L0|
|:------------------:|:-------------:|:-------------:|:-------------:|:------------------:|
| 18-11-2024   | V1   | Sahil | Initial Commit | Aakash | 


## Table of Content
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Role-Based Access Control (RBAC)](#role-based-access-control)
- [Authorization Setup](#authorization-setup)
- [Conclusion](#conclusion)
- [Contact](#contacts)
- [References](#references)

## Introduction
 

**Authorization (Authz)** refers to the process of determining what actions an authenticated user is allowed to perform within a Version Control System (VCS). Unlike **authentication (Authn)**, which verifies a user's identity, **authorization** ensures that users only have access to resources they are permitted to interact with.

In the context of VCS, proper authorization mechanisms are essential to safeguard code repositories, configurations, and other sensitive data from unauthorized access. By implementing robust authorization strategies, organizations can enforce security policies, maintain compliance, and promote collaboration in a controlled and secure environment.

## Prerequisites
1. Github account
2. Github Usernames of your team
   
## Role-Based Access Control (RBAC)

Role-Based Access Control (RBAC) is a widely used authorization model that assigns access to resources based on the roles assigned to users or entities within an organization. In this model, permissions are associated with roles, and users are assigned one or more roles. This allows for easy management of user access while ensuring that users only have the necessary permissions for their job responsibilities.

## Key Concepts

### 1. **Roles**
Roles are a way to group users based on their responsibilities and access needs within an organization. Each role has a predefined set of permissions that define what actions the users in that role can perform on various resources.

- **Example Roles:** `Admin`, `Manager`, `Employee`, `Guest`.
- **Example Permissions:** Read, Write, Delete, Execute.

### 2. **Permissions**
Permissions define the actions that can be performed on resources. Permissions are typically granted based on roles and can vary depending on the resource type and the user’s responsibilities.

- **Example Permissions:** 
  - `read`: Allows users to view data.
  - `write`: Allows users to modify data.
  - `delete`: Allows users to remove data.
  - `execute`: Allows users to run applications or scripts.

### 3. **Users**
Users are individuals or entities assigned one or more roles. Each role carries a set of permissions, so users inherit the permissions associated with their roles.

- **Example Users:**
  - **Admin:** Full access to all resources and permissions.
  - **Manager:** Can manage resources but cannot perform administrative tasks.
  - **Employee:** Can view and modify specific resources but cannot delete or manage system settings.

## How RBAC Works

1. **Assign Roles to Users:** Users are assigned one or more roles that best suit their responsibilities. Each role has associated permissions that define what the user can or cannot do.

2. **Define Permissions for Roles:** Roles are configured with permissions that determine the actions users can perform on resources.

3. **Grant Access Based on Roles:** When a user attempts to access a resource, the system checks the user’s roles and associated permissions to determine whether the action is authorized.

### Example Scenario

Imagine a company with three roles: `Admin`, `Manager`, and `Employee`.

- **Admin Role:** Has full access to all resources (can create, read, update, delete).
- **Manager Role:** Can read and update documents, but cannot delete them.
- **Employee Role:** Can only view documents but cannot modify or delete them.

By using RBAC, you can ensure that each user has access only to the resources and actions they need to perform their job.

## Advantages of RBAC

- **Simplified Management:** Rather than assigning permissions individually to each user, administrators can assign roles, making user access management more efficient.
- **Scalability:** RBAC scales well in large organizations where managing individual user permissions would be time-consuming.
- **Improved Security:** By granting users only the permissions associated with their roles, the principle of least privilege is enforced, reducing the risk of unauthorized access.
- **Auditing:** RBAC simplifies auditing by clearly associating permissions with roles, making it easier to track who has access to what resources.



## Authorization Setup

## Step 1 : Create a repo in your git hub account
![image](https://github.com/user-attachments/assets/9003cc1a-a9d2-4e74-b07f-d94f14747089)

## Step 2 : Go to the Setting option in your repo
![image](https://github.com/user-attachments/assets/f6a26f8c-3edb-454a-96eb-d40ca78f0c2a)

## Step 3 : Go to Collaborators and teams option
![image](https://github.com/user-attachments/assets/25f75691-595f-441c-baed-849969f647d4)

## Step 4 : There you can add People Create Team Add Teams
![Screenshot (46)](https://github.com/user-attachments/assets/c4056e4e-87a8-4a21-8ee4-00f0f279b40d)

## Step 5 : Now you can Create team and Add members to the Team  
![image](https://github.com/user-attachments/assets/392d43f4-8cd0-4607-af28-007c8eeedfa8)
![image](https://github.com/user-attachments/assets/f82902fc-7595-464f-9c2f-3c2a39e194bc)

## Step 6 : After adding members to team you can assign role to the Team 
![image](https://github.com/user-attachments/assets/ce99fde3-7264-4f82-8010-d2539d7ac238)


**By these steps we can give roles to the teams and members**



## Conclusion

**Authorization** is a cornerstone of securing VCS environments, ensuring that only authorized users can access sensitive resources and perform specific actions. By implementing a robust authorization strategy .

---
## Contacts
|    NAME           |   Email Address                       |
|:-----------------:|:-------------------------------------:|
|Sahil  | sahil.pathania.snaatak@mygurukulam.co

---
## References

|  Documentation name          |   Link                       |
|:-----------------:|:-------------------------------------:|
|Authorization Documentation| [Authorization Document](https://en.wikipedia.org/wiki/Authorization)
