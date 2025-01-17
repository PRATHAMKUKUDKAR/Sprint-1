# Salary API Deployment

| Created     |    Version   | Author | Comment | Reviewer |
|:------------------:|:-------------:|:-------------:|:-------------:|:------------------:|
| 12-11-2024   | V1   | Pratik | Initial Commit |  |
| 13-11-2024   | V1   | Pratik | L0 feedback | Khushi Malhotra |
| 14-11-2024   | V2   | Pratik | L0 | Khushi Malhotra |
| 15-11-2024 | V2 | Pratik | L1  | Deepak Nishad |
| 17-11-2024 | V3 |  pratik | L2 Feedback | Sandeep sir |  
| 18-11-2024 | V4 |  pratik | L2 Feedback| Mahesh Kumar   |
| 21-11-2024 | V5 |  pratik | L2 Feedback| Mahesh Kumar   |
| 23-11-2024 | V6 |  pratik | L2 Feedback| Mahesh Kumar   |
| 04-12-2024 | V6 |  pratik | L2 | anjali kaushal |

## Table of Contents

- [Understanding the Goal](#understand-the-goal)
- [Pre-requisite](#pre-requisite)
- [Databases](#pre-requisite)
- [Application Backend](#application-backend)
- [Architecture](#architecture)
- [Implementation](#implementation)
- [Final Output](#final-output)
- [Other Endpoints](#other-endpoints)
- [Contact Information](#contact-information)
- [Reference Links](#reference-links)

---
     

## Understand the Goal

Salary API is responsible for storing all the salary-related transactions and records of employees in the OT-Microservices stack. This application must be independent and able to run on multiple operating systems.


## Pre-requisite

**Databases**

- **[ScyllaDB](https://www.scylladb.com/)**: To store salary-related transaction records that remain highly available and highly secure. It must be fault-tolerant. ScyllaDB is chosen for this task.
- **[Redis](https://redis.io/)**: To achieve low latency for transactions, we use Redis as a cache manager to store the cache response.

### **Application Backend:**

- **[Java 17](https://www.java.com/en/)**: We will use Java runtime for our application. Ensure it meets the project requirements and integrates seamlessly with the databases.

## Architecture
![image](https://github.com/user-attachments/assets/edea203e-06a1-4215-aa5d-f9684ff61291)




## Implementation
### Step 1 :-  Clone the salary-api repo in your instance

```
git clone https://github.com/OT-MICROSERVICES/salary-api.git
```
### Step 2: Setup Required Prerequisites

To proceed, ensure the following components are installed and configured:

1. **ScyllaDB**  
   Follow the [ScyllaDB Installation Guide](https://opensource.docs.scylladb.com/stable/getting-started/install-scylla/install-on-linux.html) to set up ScyllaDB and configure it for your instance.

2. **Redis**  
   Refer to the [Redis Installation Guide](https://redis.io/docs/getting-started/installation/) to install Redis and configure the required user permissions.

### Step 3: Configure user Scylla and space

Optimizes the I/O settings of your system for ScyllaDB
```
sudo /opt/scylladb/scripts/scylla_io_setup
```

Go to `scylla.yaml`

```
sudo vi /etc/scylla/scylla.yaml
```

Edit the following entries in `scylla.yaml` for securing:

```yaml
authenticator: PasswordAuthenticator
authorizer: CassandraAuthorizer
```


**1: Save `scylla.yaml` and restart Scylla-server**

```
sudo systemctl restart scylla-server.service
```

**2: Access ScyllaDB and configure**
```
cqlsh <PRIVATE_IP> 9042 -u cassandra -p cassandra
CREATE USER scylladb WITH PASSWORD 'password' SUPERUSER;
LIST USERS;
CREATE KEYSPACE employee_db WITH REPLICATION = { 'class': 'SimpleStrategy', 'replication_factor': 1 };
DESCRIBE KEYSPACES;
```


## Step 4. **Setup Redis server**

**1: Install Redis and test**

```
sudo apt update
sudo apt install redis-server -y
```
**2: Configure Redis permissions**
```
redis-cli
ACL SETUSER scylla on >password ~* +@all
ACL LIST
```


## Step 5. **Setup Salary API**

**1: Install JDK 17 and Maven**

```
sudo apt install openjdk-17-jdk
sudo apt install maven
```


**2: Change the private IP in `application.yml`**

In `application.yml`:

```yaml
sudo vi salary-api/src/main/resources/application.yml
sudo vi salary-api/src/test/resources/application.yml
```

## Step 6. Create and Configure the Service File
**1: Create a Service User and Directory**
```
sudo useradd -r -m -d /var/lib/salary-api -s /bin/false salary-api-user
sudo mkdir -p /var/lib/salary-api
sudo chown -R salary-api-user:salary-api-user /var/lib/salary-api
```
**2: Create the Service File**
```
sudo vi /etc/systemd/system/salary-api.service
```
Add the following:

```
[Unit]
Description=Salary API Service
After=network.target

[Service]
Type=simple
User=salary-api-user
Group=salary-api-user
WorkingDirectory=/var/lib/salary-api
ExecStart=java -jar /var/lib/salary-api/target/salary-0.1.0-RELEASE.jar --server.port=8081
Restart=on-failure
RestartSec=5
StandardOutput=journal
StandardError=journal

[Install]
WantedBy=multi-user.target
```
**3: Enable and Start the Service**
```
sudo systemctl enable salary-api.service
sudo systemctl start salary-api.service
```


## Step7. **Install Migration Tool**

**1: Download and move the migration tool:**
```
curl -L https://github.com/golang-migrate/migrate/releases/download/v4.15.2/migrate.linux-amd64.tar.gz | tar xvz
sudo mv migrate /usr/local/bin/migrate
migrate --version
```

**2: Run Migrations**
- Install the make command and update migration.json:
```
sudo apt install make
sudo vi salary-api/migration.json
```

- Run migrations:
```
make run-migrations
```
**3: Package the Application**
```
mvn clean package
```

## Step8. **Restart the Salary-API Service**

```
sudo systemctl restart salary-api.service
```

## Final Output

#### Check the health:

#### Open browser and hit the URL:

```
http://<server>:8081/actuator/health
```
![image 25](https://github.com/user-attachments/assets/d378e77a-f5a9-4f61-b42d-32d32ada33cf)


#### Run in debug mode on browser:

```
http://<server>:8081/salary-documentation
```
![image 20](https://github.com/user-attachments/assets/54bf101b-3720-4b82-8052-65b8eecdeeb6)


## Other Endpoints:

| Endpoint                    | Method | Description                                                         |
|-----------------------------|--------|---------------------------------------------------------------------|
| `/api/v1/salary/create/record` | POST   | Data creation endpoint which accepts a JSON body to add salary info  |
| `/api/v1/salary/search`     | GET    | Endpoint for searching data information using the params in the URL |
| `/api/v1/salary/search/all` | GET    | Endpoint for searching all information across the system            |
| `/actuator/prometheus`      | GET    | Application health check and performance metrics                    |
| `/actuator/health`          | GET    | Endpoint for providing shallow health check information about the application |

## Contact Information

| Name| Email Address      |
|-----|--------------------------|
| Pratik  |  pratik.gondkar.snaatak@mygurukulam.co      | 

##  Reference Links

| Links | Description      |
|-----  |--------------------------|
| https://opensource.docs.scylladb.com/stable/getting-started/install-scylla/install-on-linux.html |  For scyllaDb  setup  | 
| https://redis.io/docs/latest/operate/oss_and_stack/install/install-redis/  |  For Redis Setup |
