# POSTGRES INSTALLATION POC

![image](https://github.com/user-attachments/assets/411ac711-209a-4bbe-a20c-7f89f3ae32dc)





| **Author** | **Created on** | **Version** | **Last updated by** | **Last edited on** | **Reviewed BY** |
|------------|----------------|-------------|----------------------|---------------------|----------|
| Priyanshu Yadav| 16-11-2024   | version 1   | Priyanshu Yadav  |      20-11-24       | Tapan Kumar Sahu (L0)|
| Priyanshu Yadav|20-11-24     | version 2   | Priyanshu Yadav  |  20-11-24           | Kirti Nehra (L1)|
| Priyanshu Yadav|    20-11-24   | version 3   | Priyanshu Yadav  |     26-11-24     |   Anjali    |
   

**Table of Contents**                               

[Introduction]( #introduction)  
      
[Prerequisite]( #prerequisite)

[Important Port](#imoprtant-Port) 

[Step-by-Step Setup Guide](#step-by-step-setup-guide)

[Conclusion](#conclusion)

[Contact Information](#contact-information)  
   
[References](#references)                               



## Introduction

PostgreSQL is a relational SQL database, which means it stores data in rows and columns. It was developed in 1986 by the University of California, Berkeley. It is widely used by many companies such as Apple, Cisco, Fujitsu, Instagram, Spotify, Skype, etc.
**"Additionally, we are using PostgreSQL in our project for the Attendance API."**

## Prerequisite


| Dependency          | Description                                                       |
|---------------------|-------------------------------------------------------------------|
| Python              | Recommended  3.6 or later                  |


## Important Port
 | 5432 |


## Step-by-Step Setup Guide 

### Install Postgres
We can install PostgreSQL in Window , Ubuntu and Mac etc. But As per our documentation we are moving forward with **ubuntu**.

#### STEP 1 : install from [official website](https://www.postgresql.org/download/)

To install postgres directly with apt command

```
sudo apt install postgresql postgresql-contrib -y
```
<img width="1083" alt="Screenshot 2024-11-13 at 11 43 54 PM" src="https://github.com/user-attachments/assets/334fdb04-d782-4e77-b81d-6a1f50e1ada9">




#### STEP 2 : To verify the installation and check the version of postgres

```
psql --version
```

<img width="1075" alt="image" src="https://github.com/user-attachments/assets/2a9ee9e6-e59f-4e76-8cb5-17627b6f8d97">

#### STEP 3 :  To start, enable, and check the status of PostgreSQL
```
sudo systemctl start postgresql
```
```
sudo systemctl enable postgresql
```
```
sudo systemctl status postgresql
```


<img width="974" alt="Screenshot 2024-11-13 at 11 44 14 PM" src="https://github.com/user-attachments/assets/c21b45c3-fc12-4e45-a5da-c8b9a903b949">

#### STEP 4 : for switching into postgres user
```
sudo -i -u postgres
```
<img width="804" alt="image" src="https://github.com/user-attachments/assets/b0f01aef-34e2-4a86-bfe0-961c5595a3a2">


#### STEP 5 : To go into postgres shell

```
psql
```

<img width="885" alt="image" src="https://github.com/user-attachments/assets/0cdb9877-908e-4668-8f01-d4910fcae11a">



#### STEP 6 : To create a database we can do 

```
create database database_name
```
For example, if you want to create a database called `my_new_db`, you would run:
```
CREATE DATABASE my_new_db;

```
<img width="713" alt="image" src="https://github.com/user-attachments/assets/a2386976-2f1d-4b84-82f0-52b8a4c87aba">


### To list the database 

```
\l
```

<img width="1176" alt="image" src="https://github.com/user-attachments/assets/35f9c2a1-4fdf-4190-827b-706ca62f9125">

### To delete a particular database

```
drop database database_name
```

<img width="1242" alt="image" src="https://github.com/user-attachments/assets/6088b4b7-e6b3-40b8-9656-4acedf5c3d6d">

## Conclusion
PostgreSQL is an ideal database for microservices due to its reliability, scalability, and support for complex queries. It helps manage data efficiently across distributed services, ensuring consistency, high performance, and flexibility as the system grows. Its advanced features make it a powerful choice for handling large volumes of data in microservice architectures.

## Contact Information 

| Name | Email address | 
|--------|------------|
|  priyanshu Yadav   | priyanshu.yadav.snaatak@mygurukulam.co  | 

## References
| Links | Description |
|-------|-------------|
| [Postgres](https://www.postgresql.org/download/linux/ubuntu/) | Postgres download |
|      https://mygurukulam25.atlassian.net/jira/software/projects/SCRUM/boards/1?label=%23Radha&selectedIssue=SCRUM-14  |           For more information on PostgreSQL.  |

