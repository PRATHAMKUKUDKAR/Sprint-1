# Employee API Detailed Documentation 

| Created     |    Version   | Author | Comment | Reviewer |
|:------------------:|:-------------:|:-------------:|:-------------:|:------------------:|
| 11-11-2024   | V1   | Radha | Initial Commit |  |
| 14-11-2024   | V2   | Radha | L0 | Aakash Tripathi |  
| 21-11-2024   | V2   | Radha | L1 | Deepak Nishad | 
| 29-11-2024   | V3   | Radha | L2 | Mahesh Kumar |         


# Table of Contents
- [Introduction](#introduction)
- [Architecture](#Architecture)
- [Pre-requisites](#Prerequisites)
- [Features](#Features)
- [Tools Used](#Tools-Used)
- [Database and Caching](#Database-and-Caching)
- [Conclusion](#Conclusion)
- [Contact Information](#Contact-Information)
- [Reference Links](#Reference-Links)

# Introduction

The Employee API is a Golang-based REST API designed for managing employee information. This application integrates ScyllaDB as its primary database and uses Redis for caching. The API is built with the Gin framework, which ensures fast and scalable operations for RESTful transactions.


# Architecture
![image](https://github.com/user-attachments/assets/50d18e52-0e94-48d3-9db7-28ba439e819f)

# Prerequisites
To get started, ensure you have the following installed and set up on your machine:

- Go (Golang) - Version 1.18
- ScyllaDB - Make sure you have an accessible ScyllaDB instance with the appropriate keyspaces and tables for employee data and RAM of VM (20).
- Redis (optional) - For caching functionality, an active Redis instance is recommended but not required.
These components must be accessible over the network or from within the same environment as the API.

# Features

The Employee API is designed for efficient management of employee information and seamless integration into larger systems. Below are its key features:

| Feature                  | Description                                                                                  |
|--------------------------|----------------------------------------------------------------------------------------------|
| **CRUD Operations**      | Provides full Create, Read, Update, and Delete functionality for managing employee records.  |
| **High-Performance Storage** | Built on ScyllaDB, optimized for distributed and high-throughput workloads, with a Cassandra-compatible interface. |
| **Redis Caching**        | Optionally integrates with Redis to cache frequently requested employee data, improving response times and reducing database load. |
| **API Documentation with Swagger** | Offers self-updating, interactive API documentation for testing and understanding available endpoints. |
| **Scalable and Lightweight** | Developed in Go, ensuring high efficiency and scalability to handle a large volume of requests. |

# Tools Used
| **Technology/Tool** | **Description** | **Purpose** |
|---------------------|------------------|-------------|
| **Go (Golang) 1.22** | A fast and statically typed programming language known for simplicity and strong concurrency support. | Primary language for API development due to its performance and efficient handling of concurrent requests. |
| **ScyllaDB** | A distributed NoSQL database that is Cassandra-compatible and optimized for low-latency and high-throughput operations. | Stores and manages data for high availability and quick access. |
| **Redis** | An in-memory data store used for caching. It supports various data structures like strings, lists, and sets. | Caches frequently accessed data to reduce database load and improve API response times. |
| **Swagger** | An open-source tool that automatically generates interactive API documentation. | Provides a web interface for API documentation and testing endpoints. |
| **Make Command** | A build automation tool that uses a Makefile to execute commands automatically. | Simplifies repetitive tasks such as building the application and running migrations. |
| **Migrate** | A command-line tool for managing database schema changes. | Ensures database schema is consistent with application requirements during development and deployment. |
| **JQ** | A command-line processor for JSON data. | Used for parsing and manipulating JSON data for various scripting purposes. |

## Usage
- Ensure all dependencies are installed and configured as required.
- Use `make` commands defined in the Makefile to automate common tasks like building, testing, and running migrations.
- Swagger documentation can be accessed at `[API endpoint]/swagger` for interaction and testing.


## Installation and Setup
Follow these steps to set up the API and its environment:
1. Install Go 1.22 from [the official Go website](https://golang.org/dl/).
2. Set up ScyllaDB and configure connection parameters.
3. Install and configure Redis.
4. Run `make build` to build the application.
5. Use `make migrate` to run database migrations.
6. Access Swagger documentation at `/swagger` endpoint after running the server.



# Database and Caching
This microservice utilizes ScyllaDB and Redis to efficiently handle data storage and retrieval. Each of these components serves a distinct purpose within the application.

## 1. ScyllaDB
ScyllaDB is the primary persistent database for the Employee API, responsible for storing all core employee-related data, such as employee details, locations, and designations.

## 2. Redis
Redis serves as an in-memory caching layer to enhance performance by storing frequently accessed data temporarily.


# Conclusion
The Employee API is a robust microservice designed to manage employee data within the OT Microservices architecture. It integrates seamlessly with the Attendance API and Salary API, and leverages ScyllaDB for high-performance data storage. By incorporating Redis for caching, Swagger for API documentation, and Prometheus for monitoring, it ensures efficient operations and scalability. This API is intended to serve as a backbone for employee-related services, providing easy extensibility and maintainability.

We encourage contributions, bug reports, and feedback to help improve the overall functionality and usability of the project. For any issues or feature requests, feel free to open an issue or pull request.

## Contact Information
| Name| Email Address      |
|-----|--------------------------|
| Radha Gondchor |radha.gondchor.snaatak@mygurukulam.co |



## Reference Links
| Links | Description      |
|-----  |--------------------------|
| https://github.com/OT-MICROSERVICES/employee-api/tree/main?tab=readme-ov-file | Employee api | 
|https://github.com/MyGurukulam-p11/Documentation-P11/tree/Radha_scrum_04/OT-MS-understanding/Employee/POC|Employee api POC
| https://www.simplyblock.io/glossary/what-is-scylladb/    | Scylladb |
| https://www.geeksforgeeks.org/introduction-to-redis-server/ | Redis |
