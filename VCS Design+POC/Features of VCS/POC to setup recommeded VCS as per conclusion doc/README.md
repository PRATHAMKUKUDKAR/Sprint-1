# GitHub Version Control System (VCS) Setup: Proof of Concept

| Author      | Created on | Version   | Last updated by | Last edited on | Reviewed By  | **DATE** |
|-------------|------------|-----------|-----------------|----------------|----------------|-----|
| Chander Kant       | 19-11-24   | Version 1 | Chander Kant   | 25-11-24       | Aakash            (L0)   | 25-11-2024



## Table of Contents

1. [Purpose](#Purpose)
2. [System Requirements](#System-Requirements)
3. [Architecture](#architecture)
4. [Step-by-step installation of GitHub](#Step-by-step-installation-of-Github)
5. [Adding/Assigning roles](#Addingassigning-roles)
6. [Conclusion](#Conclusion)
7. [Contact Information](#Contact-Information)
8. [Reference](#Reference)

## Purpose 
This Poc demonstrates how to set up and use GitHub as a Version Control System. GitHub provides a centralized platform for collaborative software development, offering features like version control, issue tracking, and project management.

## System Requirements
  

| Name    | Version | Description |
|---------|---------|-------------|
| Git     | 2.34    | Distributed version control system |


## Architecture 
![Architecture VCS](https://github.com/user-attachments/assets/c63761a8-b791-4e64-99a6-d687c2d6a624)

## Step-by-step installation of GitHub 

1. Install Git:
   ```bash
   # Windows (using Chocolatey)
   choco install git

   # macOS (using Homebrew)
   brew install git

   # Ubuntu
   sudo apt-get update
   sudo apt-get install git
   ```

2. Create a GitHub account at [github.com](https://github.com)

3. Create a new repository on GitHub:
   - Click the "+" icon in the top-right corner
   - Select "New repository"
   - Name your repository
   - Click "Create repository

![image](https://github.com/user-attachments/assets/85372eff-8f07-4247-a638-c0bf0142e312)
![image](https://github.com/user-attachments/assets/e1cdfa46-c663-40bf-9ade-54a85cb552f5)



4. Set up local repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   # Make changes to files
   touch index.html
   git add index.html
   git commit -m "added index.html"
   git push origin main
   ```
![image](https://github.com/user-attachments/assets/b71a525f-1fab-4728-8482-cdb8d888aa17)
![image](https://github.com/user-attachments/assets/dcd79a3b-03cf-4920-ad9a-0793d7cb9d96)


## Adding/Assigning roles 

![1732197825301](https://github.com/user-attachments/assets/e7162b13-edf9-45b8-9fc1-e3a8f018912f)
![1732197825319](https://github.com/user-attachments/assets/ff4f49bc-28fb-49aa-a548-e542cec8c287)
![1732197825339](https://github.com/user-attachments/assets/fb9a9d3c-e24f-49e6-953f-2d310fd89930)
![1732197825307](https://github.com/user-attachments/assets/53be954b-34eb-413e-982d-9625778d1b58)
![org](https://github.com/user-attachments/assets/c39deccc-b101-489d-9d80-5f54adb2d9b1)
![member](https://github.com/user-attachments/assets/67d261f1-e35b-465a-a1d5-2e293529a43a)


For more details please visit  [Link](https://docs.github.com/en/organizations/managing-peoples-access-to-your-organization-with-roles/using-organization-roles)  For Roles - Assign .



## Conclusion 

In this Proof of Concept (PoC), we demonstrated the basic process of creating a repository, cloning it, and pushing changes. This workflow allows developers to track modifications, collaborate smoothly, and ensure an organized approach to managing project files and updates. By following these steps, teams can streamline their development efforts and enhance productivity across the board.

## Contact Information 

| Name | Email address|
|------|---------------------|
| Chander Kant   | chanderkant.soni.snaatak@mygurukulam.co |

## References  
| Links                                             | Descriptions                                                    |
|---------------------------------------------------|-----------------------------------------------------------------|
| [Link](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks) |Git Documentation - Customizing Git|


