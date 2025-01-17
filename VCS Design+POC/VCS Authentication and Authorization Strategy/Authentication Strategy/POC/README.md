
# POC to Setup Authentication



| Created     |    Version   | Author | Comment | L0 reviewer | L1 reviewer | L2 reviewer |
|:------------------:|:-------------:|:-------------:|:-------------:|:---------------:|:--------:|:------------:|
| 18-11-2024   | V1   | Sahil | Initial Commit | Aakash     |Kirti      |          |  

## Table of Content
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Authentication Setup](#authentication-setup)
-  [ Two-Factor Authentication](two-factor-authentication)
- [Conclusion](#conclusion)
- [Contact](#contacts)
- [References](#references)

## Introduction
Authentication is the process of verifying the identity of a user, device, or system to ensure that the entity requesting access is actually who or what it claims to be. This process helps secure systems by confirming the legitimacy of an entity before granting access to resources.

## Prerequisites

- Email Id



## Authentication Setup

## Step 1

**Below is a detailed guide for setting up  for GitHub, a popular distributed version control system.**

Search Github.com on any Browser and put your email id and create username and create strong password for your account using this link (https://www.strongpasswordgenerator.org) and then verify your account.

## Step 2
**Check your email for the verification code enter the verification code**


![7](https://github.com/user-attachments/assets/5efd6d70-d0cb-475c-9fc6-cbf6184b0351)


## Step 3
 **Now put login details and  you will be loged into Github portal and start exploring.**

 
![8](https://github.com/user-attachments/assets/dda51544-10d7-46c0-bd43-062a515bef6c)



![9](https://github.com/user-attachments/assets/4d681c95-c72b-4ced-b60f-5efda85515ad)


# Two-Factor Authentication

Two-Factor Authentication (2FA) is an enhanced security process that requires two distinct forms of identification from the user to access an account or system. It adds an extra layer of protection by combining something you **know** (e.g., a password) with something you **have** (e.g., a smartphone, security token, or email). The goal of 2FA is to make it much harder for unauthorized users to gain access, even if they have stolen or guessed the password.

## How Two-Factor Authentication Works:

### First Factor: Something You Know
- Typically, this is a **password**, **PIN**, or **passphrase**. This is the first step in the authentication process.

### Second Factor: Something You Have
The second factor can be one of the following methods:
# Authentication Methods

 1. **Code sent via SMS or Email**
   - A one-time code is sent to the user’s registered phone number or email address. The user must enter this code to complete the authentication process.
   - This method adds an extra layer of security but is vulnerable to SIM-swapping or email account hacks.

2. **Authenticator App**
   - An app (like Google Authenticator or Authy) generates time-based one-time passwords (TOTP) that users enter during the login process.
   - This method is more secure than SMS-based codes as it does not rely on network transmission and is less vulnerable to interception.

 3. **Biometric Verification**
   - Uses unique physical characteristics like fingerprints, face recognition, or retina scans to verify a user’s identity.
   - It is a highly secure and convenient method but can raise privacy concerns and may not work in certain conditions (e.g., poor lighting or damaged fingers).

   

## **Enable Two-Factor Authentication**

> Go to github setting then go to Password and authentication and enable Two-factor authentication .
## Step 1
![Screenshot from 2024-11-17 21-16-11](https://github.com/user-attachments/assets/d1d8b034-6d78-436c-a971-751b0827e8bf)
## step 2
![Screenshot from 2024-11-17 21-16-37](https://github.com/user-attachments/assets/615cb489-b1f7-44f1-8769-eb030f03ca16)

## Advantages of Two-Factor Authentication:

- **Enhanced Security**: Even if an attacker obtains your password, they would still need access to the second factor (e.g., your phone or authentication device) to log in.

- **Protection Against Common Attacks**: 2FA significantly reduces the risk of common cyber threats like **phishing**, **brute-force attacks**, and **credential stuffing**.

- **Compliance**: Many industries and regulatory standards, such as **banking**, **healthcare (HIPAA)**, and **e-commerce (PCI-DSS)**, require 2FA as a security measure to protect sensitive data.
- 
## Conclusion

> In conclusion, authentication is a vital process in securing digital systems and protecting sensitive information from unauthorized access. By verifying the identity of users, devices, or systems, authentication ensures that only legitimate entities can interact with critical resources. 


## Contacts

|    NAME           |   Email Address                       |
|:-----------------:|:-------------------------------------:|
|Sahil| 	sahil.pathania.snaatak@mygurukulam.co

## References

| Description                                        | Link                                                                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Git Documentation                                  | [Git Documentation](https://git-scm.com/doc)                                                                                                    |
| VCS Documentation                                  | [VCS Documentation](https://www.atlassian.com/git/tutorials/what-is-version-control)                                                           |
| GitHub Documentation                               | [GitHub Documentation](https://www.geeksforgeeks.org/introduction-to-github/)                                                                  |
| Detailed documentation of VCS (Github) setup       | [Detailed documentation of VCS (Github) setup](https://github.com/MyGurukulam-p11/Documentation/blob/Pritam_scrum25/VCS/Setup/README.md)         |
| Detailed Documentation Authentication              | [Detailed Documentation Authentication](https://github.com/MyGurukulam-p11/Documentation/tree/main/VCS/Authentication-%26-Authorization-strategy/Detailed-Documentation-Authentication) |
