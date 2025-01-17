# Full Stack OT-Microservice Application Setup

 
| Created     |    Version   | Author | Comment | Reviewer |
|:------------------:|:-------------:|:-------------:|:-------------:|:------------------:|
| 19-11-2024  | V1   | Pritam Kondapratiwar | Initial Commit | Tapan Shahu
| 19-11-2024 | V2 | Pritam Kondapratiwar | L1  |  Rishabh Sharma    |
| 29-11-2024 | V3 |  Pritam Kondapratiwar | L2 |   Mahesh kumar   |          |  



## Table of Contents

- [Introduction](#introduction)
- [Architecture](#architecture)
- [Components](#components)
- [How to connect API with frontend ?](#how-to-connect-api-with-frontend)
- [Final output](#final-output)
- [Contact information](#contact-information)
- [References](#references)

## Introduction

In this document, we will explore how to set up a full OT-microservice application.

- **Frontend**: Builds user interfaces using technologies like React, HTML, CSS, and JavaScript.
- **Backend**: Handles APIs, business logic, and database operations using:
  - Go (`employee-api`)
  - Java (`salary-api`)
  - Python (`attendance-api`)
- **API Integration**: Connects the frontend and backend for seamless data flow.
- **Database**: Manages data storage, utilizing:
  - **ScyllaDB**
  - **PostgreSQL**

## Architecture
![image](https://github.com/user-attachments/assets/87ed90e9-5440-4380-b2bf-809254a611e1)



## Components
There are 3 API's which are written in go , java and python and frontend written in JS. 

|       API      |   Link                      |
|:-----------------:|:-------------------------------------:|
| **How to setup employee-API**| https://github.com/MyGurukulam-p11/Documentation-P11/tree/main/OT-Microservices/Application/Employee-API/POC
| **How to setup salary-API** |https://github.com/MyGurukulam-p11/Documentation-P11/tree/main/OT-Microservices/Application/Salary-API/POC
| **How to setup attendance-API** | https://github.com/MyGurukulam-p11/Documentation-P11/tree/main/OT-Microservices/Application/Attendance-API/POC
| **How to setup frontend** | https://github.com/MyGurukulam-p11/Documentation-P11/tree/main/OT-Microservices/Application/Frontend/POC


## How to connect API with frontend ?

>In all three API's there are cors issue for that we need to install cors module  in all three API's.

**Step 1:** In Employee-API we need to install module in main.go file.
```sh
go get github.com/gin-contrib/cors
```
![Screenshot from 2024-11-18 12-13-49](https://github.com/user-attachments/assets/8a9254d3-e884-42a7-98f6-5c1489fb9aeb)

    

**Step 2:** In salary-API we need to install module in SpringDataController.java file.

```sh
npm install cors
```

![Screenshot from 2024-11-18 12-13-17](https://github.com/user-attachments/assets/83744550-09a0-4dd0-9080-d55cc571be30)

**Step 3:** In attendance-API we need to install module in app.py file.

```sh
pip install flask-cors
```
   
![Screenshot from 2024-11-18 12-14-25](https://github.com/user-attachments/assets/bbc0c501-0e46-40e3-b67f-507e8b4c7354)


**Step 4:** In frontend we have to do some configuration in various file such as AttendanceForm.js , AttendanceList.js , EmployeeData.js , EmployeeForm.js , EmployeeList.js and ListSalary.js.
   - **AttendanceForm.js:**
     
     ![image](https://github.com/user-attachments/assets/2e9c5183-81f7-4c30-8c76-4da53d01680a)

   - **AttendanceList.js:**
     
     ![image](https://github.com/user-attachments/assets/72565106-717d-49a7-9e71-4e8f031e1be4)

   - **EmployeeData.js:**
     
     ![image](https://github.com/user-attachments/assets/2d96f5ae-91f2-4094-a0bf-37e559ebbced)

   - **EmployeeForm.js:**
     
     ![image](https://github.com/user-attachments/assets/fd2d3849-e6fe-4e58-9977-96ca95b72e6a)

   - **EmployeeList.js:**
    ![image](https://github.com/user-attachments/assets/5a57d5a6-0cd7-4778-a426-885698f39890)

   - **ListSalary.js:**
    ![image](https://github.com/user-attachments/assets/fd719350-f99d-4712-9985-2b5de14c82ea)


  
## Final output
  
  ![Screenshot from 2024-11-16 08-16-38](https://github.com/user-attachments/assets/4bcb480d-45f9-4036-81eb-60af05519cfe)

  ![Screenshot from 2024-11-16 08-16-45](https://github.com/user-attachments/assets/38f8cbdf-d5a1-40bd-ba0e-f1214d90e8f5)

  ![Screenshot from 2024-11-16 21-41-42](https://github.com/user-attachments/assets/37d6fe3e-9d03-47fa-96b7-be978f08ec5d)


## Contact information

|    NAME           |   Email Address                       |
|:-----------------:|:-------------------------------------:|
|Pritam Kondapratiwar| 	pritam.pratiwar.snaatak@mygurukulam.co

## References

|   Link |Description  |
|:------------------:|:-------------------:|
| https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS|Introduction of cors 
| https://spring.io/guides/gs/rest-service-cors | Cors for java
| https://stackoverflow.com/questions/50065875/how-to-enable-cors-in-python | Cors for python
| https://www.stackhawk.com/blog/golang-cors-guide-what-it-is-and-how-to-enable-it | Cors for go
