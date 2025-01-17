
![logo](https://github.com/user-attachments/assets/29d8c27b-4cfa-46ed-8913-dc65d08e2ca6)

# Redis POC (Proof Of Concept) 

| **Author** | **Created on** | **Version** | **Last updated by** | **Last edited on** | **Reviewed BY** |
|------------|----------------|-------------|----------------------|---------------------|----------|
| Chander Kant| 12-11-24  | version 1   | Chander Kant   | 14-11-24         | Aakash Tipathi (L0)|
| Chander Kant| 12-11-24  | version 2   | Chander Kant   | 14-11-24         | Tapan (L0)|
| Chander Kant| 12-11-24  | version 3   | Chander Kant   | 19-11-24         | Deepak (L1)|
| Chander Kant| 12-11-24  | version 4   | Chander Kant   | 29-11-24         | Mahesh Kumar (L2)|

   
## Table of Contents 
- [Introduction](#Introduction)
- [What is Redis?](#What-is-Redis?)
- [Redis Setup Prerequisites](#Redis-Setup-Prerequisites)
- [ Redis Installation on Ubuntu](#Redis-Installation-on-Ubuntu)
- [Conclusion](#Conclusion)
- [Contact Information](#Contact-Information)
- [References](#References)

## Introduction

This POC of Redis provides a comprehensive overview of Redis, an in-memory data store known for its speed and versatility.

## What is Redis? 
Please Vist the Link for [Redis Documentation](https://github.com/MyGurukulam-p11/Documentation-P11/blob/Chanderkant_SCRUM-12/OT-MS-Understanding/Redis/Detailed-documentation/README.md)  

## Redis Setup Prerequisites 

| **Requirement**        | **Details**                  |
|------------------------|------------------------------|
| **OS**                 | Linux , macOS , windows , Cloud Plateforms (AWS , GCP , AZURE , OCI) |
| **RAM**                | 4 GB minimum |
| **Disk Space**         | 100 MB or Depend on scale & size of Data              |
| **Processor**          | Dual-core recommended        |
| **Network**            |  6379 (PORT NO)               |
| **Redis Version**      | version 6 or Higher/Latest recommended    |

## Prerequisites

- Ubuntu 20.04 or any latest Machine
- A user having  `sudo` privileges to perform seamless action


## Redis Installation on Ubuntu 

This Installation guide provides the steps to install and configure Redis on Ubuntu.


## Installation Steps 

### Step 1: Update System Packages

Before starting the installation, ensure your system packages are up-to-date.

``` bash
sudo apt update
```
### Step 2: Install Redis 

To install Redis, use the apt package manager

``` bash
sudo apt-get install redis-server 
```

### Step 3: Start Redis Service 
Run the following command to start the Redis service:

``` bash
sudo systemctl start redis-server
sudo systemctl enable redis-server
```
### Step 4: Check Redis Service Status 
To confirm that Redis has started successfully, use the following command:

``` bash
sudo systemctl status redis-server
```

### Step 5. Stop Redis Service 
To stop the Redis service, run:

``` bash
sudo systemctl stop redis-server
```

### Step 6: Configure Redis 
To set up a password and username for Redis, follow these steps:
#### 1. Open the Redis configuration file

``` bash
sudo vi /etc/redis/redis.conf
```
#### 2. Set a Password
Find the line with # requirepass foobared and replace it with:

``` bash
requirepass <your_password_here>
```
#### 3. Save and Close the file

 #### 4.Restart Redis
To apply these changes, restart the Redis service:

``` bash
sudo systemctl restart redis
```

#### 5 verify the installation 
To Verify the installation is success use the below steps.
-  Go to Redis cli by entering the below commands
``` bash
redis-cli
```
After Entering into the redis-cli type
``` bash
 ping 
```
In revert we got PONG that show the successfull installation.

![4](https://github.com/user-attachments/assets/b369f078-d730-4b5d-b3a0-b7e186c8b329)

--- 


## Some Basic Data manipulation in Redis 
 To perform some basic Data manipulation we use the below commads

![6](https://github.com/user-attachments/assets/178db44d-3b31-4095-ad27-19820887255a)



## Conclusion 
Redis, an in-memory data store, has emerged as a powerful tool for modern application development. Its ability to handle a wide range of data structures, coupled with its exceptional performance and flexibility, makes it a valuable asset in optimizing application performance and scalability.



### Contact Information 

| **Name** | **Email address**            |
|----------|-------------------------------|
| Chander Kant   | chanderkant.soni.snaatak@mygurukulam.co           |


### References 


Link                                                                                       | Description                                              |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Redis Documentation - Linux Installation](https://redis.io/docs/latest/operate/oss_and_stack/install/install-redis/) | Document format followed from this link.
   
