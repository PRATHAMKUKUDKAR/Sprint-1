
# Setup and run the ScyllaDB for POC
![download](https://github.com/user-attachments/assets/1212cddf-9ad6-4447-8ab2-b158ff0466db)

| Created     |    Version   | Author | Comment | L0 reviewer | L1 reviewer | L2 reviewer |
|:------------------:|:-------------:|:-------------:|:-------------:|:---------------:|:--------:|:------------:|
| 13-11-2024   | V1   | Sahil | Initial Commit |Aakash  | Kirti    |          |  



## Table of Contents

- [Introduction](#introduction)
- [ScyllaDB Setup](#scylladb-setup)

- [Contact](#contact)
- [References](#references)

## Introduction
![download](https://github.com/user-attachments/assets/6da2c659-bcbc-4211-af4e-599e9630c7f9)


**Below is a detailed guide for setting up ScyllaDB  using Docker   in loacl system, a popular NO-SQL Database.**


# ScyllaDB Setup

#  ScyllaDB
ScyllaDB is a high-performance, distributed database designed to handle large amounts of data quickly and efficiently. It's often seen as a faster alternative to Apache Cassandra, but with a number of improvements in terms of speed, ease of use, and scalability.

**Prerequisites:**
| Component         | Requirement                                                |
|-------------------|------------------------------------------------------------|
| **Operating System** | Linux , macOS  |
| **CPU**           | Multi-core processor (4 cores or more recommended)         |
| **Memory**        | Minimum 4 GB RAM (8 GB or more recommended)                |


# **Installation:**

## Step 1: Create the keyrings directory

First, you need to create the `keyrings` directory where the GPG key for ScyllaDB will be stored.

```bash
sudo mkdir -p /etc/apt/keyrings
```

## Step 2: Add the ScyllaDB GPG key

Next, download and store the ScyllaDB GPG key to ensure that the packages you install are verified.

```bash
sudo gpg --homedir /tmp --no-default-keyring --keyring /etc/apt/keyrings/scylladb.gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys a43e06657bac99e3
```

## Step 3: Add the ScyllaDB APT repository

Now, add the ScyllaDB repository to your system by downloading the `scylla.list` file.

```bash
sudo wget -O /etc/apt/sources.list.d/scylla.list http://downloads.scylladb.com/deb/debian/scylla-6.2.list
```
![image 1](https://github.com/user-attachments/assets/a90f02df-a78b-412e-86f0-23b353c49370)

## Step 4: Update your package list

To make the newly added repository available, update your package list.

```bash
sudo apt update
```

## Step 5: Install ScyllaDB packages

Finally, you can install the ScyllaDB packages.

```bash
sudo apt install scylla
```
![image 2](https://github.com/user-attachments/assets/22f7f5c5-994e-41a2-b838-2846a153eab3)

## Step 6 : Runs the scylla-io-setup script

The `scylla-io-setup` script is an important part of the ScyllaDB setup process. It is used to configure the input/output (I/O) settings for ScyllaDB in order to optimize disk I/O operations, ensuring that ScyllaDB can run efficiently and with high performance.



```bash
sudo /opt/scylladb/scripts/scylla-io-setup
```
![image 3](https://github.com/user-attachments/assets/4345623a-01c9-4708-b472-f0837f79eb78)

## Step 7 : Run ScyllaDB as a service (if not already running).



To run ScyllaDB as a service, you can use the `systemctl` command to start the ScyllaDB server. This will ensure that ScyllaDB runs in the background as a system service and automatically starts with your system.


```bash
sudo systemctl start scylla-server
```
## Step 8 : Check ScyllaDB Status 

```bash
sudo systemctl status scylla-server
```
![image 4-1](https://github.com/user-attachments/assets/56f84ab5-56ee-49b6-855b-4aa337662feb)

---





## Conclusion
ScyllaDB is a high-performance, horizontally scalable NoSQL database designed to handle large amounts of data with low-latency operations. It is fully compatible with Apache Cassandra but provides significant improvements in speed and resource efficiency, making it suitable for real-time data-intensive applications. With its ability to scale seamlessly across multiple nodes and data centers, ScyllaDB is an excellent choice for modern, distributed systems.


## Contacts
|    NAME           |   Email Address                       |
|:-----------------:|:-------------------------------------:|
|Sahil  | sahil.pathania.snaatak@mygurukulam.co
## References
- ScyllaDb Documentation: (https://docs.scylladb.com/stable/)
- ScyllaDb Detailed Documentation: (https://github.com/MyGurukulam-p11/Documentation-P11/tree/main/OT-Microservices/Softaware/ScyllaDB/Detailed-Documentation)
