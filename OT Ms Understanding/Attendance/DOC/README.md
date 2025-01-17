
# Attendance-API
 

| **Author** | **Created on** | **Version** | **Last updated by** | **Last edited on** | **Reviewed BY** |
|------------|----------------|-------------|----------------------|---------------------|----------|
| Priyanshu Yadav| 12-11-24  | version 1   | Priyanshu Yadav  | 14-11-24         | Tapan Kumar Sahu (L0)|
| Priyanshu Yadav| 14-11-24  | version 2   | Priyanshu Yadav  | 20-11-24         | Shashi (L1)|
| Priyanshu Yadav| 20-11-24  | version 3   | Priyanshu Yadav  | 22-11-24         |    Mahesh Kumar           |




## Table of Content

- [Purpose](#Purpose)
- [Pre-requisite](#Pre-requisite)
- [System Requirements](#System-Requirements)
- [Dependencies](Dependencies)
- [Important Ports](#Important-Ports)
- [Architecture](#Architecture)
- [Dataflow](#Dataflow)
- [Application Configuration Changes](#Application-Configuration-Changes )
- [Application Build](#Application-Build)
- [How to run Api in the background](#How-to-run-Api-in-the-background)
- [Monitoring](#Monitoring)
- [High Availability](#High-Availability)
- [Troubleshooting](#Troubleshooting)
- [Endpoints Information](#Endpoints-Information)
- [Contact information](#Contact-information)
- [References](#References)

## Purpose
Attendance api is a Rest Api which is responsible for attendance related transaction in OT microservice . 

## Pre-requisites

- [Postgres](https://www.postgresql.org/download/linux/ubuntu/)
- [Redis](https://www.digitalocean.com/community/tutorials/how-to-install-and-secure-redis-on-ubuntu-18-04)
- [Poetry](https://python-poetry.org/)
- [Liquibase](https://docs.liquibase.com/start/install/liquibase-linux.html)



## System requirements

| **Hardware Specifications** | **Minimum Recommendation**  |
|--------------------------|------------------------|
| **Processor**                | Dual-core              |
| **RAM**                      | 8GB                    |
| **Disk**                     | 10GB                   |
| **OS**                       | Ubuntu(22.04)          |
| Instance type                | t2.large               |


## Dependencies

### Build time Dependencies

| **Name**              | **Version**           | **Description**                                                       |
| ----------------- | ----------------- | ------------------------------------------------------------------ |
| **Poetry**   | 1.83 | Required for Python modules                          |
| **Redis** | 7.0.12     | Install redis for data caching                         |
| **Postgres** | 16.3 | Required for creating database with which api will interact |
| **Liquibase** | 4.28 | For Schema Management |


### Run Time Dependency

| **Name** | **Version** | **Description** |
|------|---------|-------------|
| **python** | 3.11 | Application is built on this version only |

## Important Ports

| **Inbound Traffic** | **Description** |
|-----------------|-------------|
| **8080** | Used by Api |

## Architecture
<img width="983" alt="image" src="https://github.com/user-attachments/assets/e7d6fc60-0f0a-41ad-93c3-504edf12f714">


## Dataflow

- The application first checks Redis to see if the requested data is already cached.
- Cache Hit: If the data is found in Redis, it is returned immediately, reducing the need for a database query.
- Cache Miss: If the data is not found in Redis, the application proceeds to query the PostgreSQL database.




 

## Application Build

For building the application, we can use make command with our [Makefile](https://github.com/OT-MICROSERVICES/attendance-api/blob/main/Makefile). But as first and foremost step, we need to install all the dependencies and packages using poetry. We can simple use make command for it.

``` 
make build 
```




Now we need to run migrations to create database, schema etc . 

``` 
make run-migrations
```



Now lets create python environment and go into it 
```
python3 -m venv myenv
source myenv/bin/activate
```




Now lets initialize the application by below command 
```
gunicorn app:app --log-config log.conf -b 0.0.0.0:8080
```




To check wether the api is working or not we can use below command , replace localhost with your ip address if you are running the api on cloud
```
 http://< Your_Public_ip >:8080/apidocs
```

## How to run Api in the background

- create a service for api 

```
sudo vim /etc/systemd/system/attendance-api.service
```

```
[Unit]
Description=My API Service
After=network.target

[Service]
User=apiuser
Group=apiuser
WorkingDirectory=/opt/attendance-api/attendance-api
Environment=PATH=/opt/attendance-api/attendance-api/venv/bin:/usr/bin
ExecStart=/opt/attendance-api/attendance-api/venv/bin/gunicorn app:app --log-config /opt/attendance-api/attendance-api/log.conf -b 0.0.0.0:8080
Restart=always
RestartSec=3
Environment=NODE_ENV=production

[Install]
WantedBy=multi-user.target


```


#### Start the Attendance service
Run the following command to start the service:
```
sudo systemctl daemon-reload

```
```
sudo systemctl enable attendance-api.service
```
```
sudo systemctl start attendance-api.service 
```


## Monitoring

Api monitoring is crucial to analyze whether the api is working correctly or not , we can monitor logs that are generating , we can see what is the throughput of our api , we can detect and prevent unauthorized person trying to access our website .

#### Tools to Monitor API's

- **Postman** : Postman is a good tool for monitoring and testing our Api , it allows us to automate tests to check the health and performance of our API's. By setting up monitors , we can regularly test that our Api are working properly or not , this helps maintain high reliability.
- **CloudWatch** : If we are using Api Gateway service of aws , which can manage and create api's , we can fetch the logs that are generating from it and store it into cloudwatch.


- **Grafana** :  Grafana is used for visualization and monitoring. It collects metrics from APIs and displays them in customizable dashboards. You can set alerts to notify you when specific thresholds are crossed. Grafana integrates well with Prometheus and other time-series databases.

- **Prometheus** : Prometheus is designed for time-series data monitoring. It is ideal for collecting and querying real-time metrics such as API response times, error rates, and throughput. Prometheus can also trigger alerts based on predefined conditions.


## High Availability

We can deploy our api on multiple servers and then use load balancer for distributing traffic among different servers so that there won't one one single point of failure , means that if one instance will fail our whole Api will not go down .

We can acheive this by attaching load balancer with multiple servers running Api , and then these Api are storing data into one database only , this database can be AWS managed database or database that you have set up on some server . 

## Troubleshooting

if you don't create python environment and try to run api without it you might encounter this problem 
<img width="1324" alt="Screenshot 2024-11-12 at 11 16 52 PM" src="https://github.com/user-attachments/assets/80e0eed9-2dc9-4e1e-a6c8-6445d1fe95ed">


#### To solve this create virtual environment in python

```
source <your_environment_name>/bin/activate
```



## Endpoints Information

| Endpoint | Method | Description |
|----------|--------|-------------|
| **/metrics** | GET | Application healthcheck and performance metrics are available on this endpoint. |
| **/apidocs** | GET | Swagger endpoint for the application API documentation and their data models. |
| **/api/v1/attendance/create** | POST | Data creation endpoint which accepts certain JSON body to add attendance information in database. |
| **/api/v1/attendance/search** | GET | Endpoint for searching data information using the params in the URL. | 
| **/api/v1/attendance/search/all** | GET | Endpoint for searching all information across the system. |
| **/api/v1/attendance/health** | GET | Endpoint for providing shallow healthcheck information about application health and readiness. | 
| **/api/v1/attendance/health/detail** | GET | Endpoint for providing detailed health check about dependencies as well like - PostgresSQL and Redis. | 


## Conclusion 

Following these steps, you will be able to set up attendance api , and then after checking the endpoints you can check wether the api is working or not .

## Contact information

| **Name** | **Email address** | 
|--------|------------|
| **Priyanshu Yadav**  | **priyanshu.yadav.snaatak@mygurukulam.co**  | 


## References

| Links | Descriptions | 
|--------|------------|
| https://www.liquibase.com/download  |  For Installing Liquibase | 
| https://www.postgresql.org/download/linux/ubuntu/  | Postgress Istallation  | 
| https://redis.io/docs/latest/operate/oss_and_stack/install/install-redis/install-redis-on-linux/   | For installing Redis 
