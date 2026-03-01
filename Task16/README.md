# Task 16: RDS Database + SQL Workbench Connection & Queries

## Objective
To understand managed database services by deploying an Amazon RDS instance and establishing a secure remote connection to execute SQL queries.

## Implementation Steps

### 1. Database Provisioning
- Navigated to the Amazon RDS Console and initiated a Standard Create for a new database instance.
- Selected the MySQL engine using the Free Tier template to optimize cost.
- Configured master credentials (`admin`) and set the instance identifier.

### 2. Network and Security Configuration
- Enabled Public Access to allow external connections from a local workstation.
- Created a new VPC Security Group specifically for RDS to allow inbound traffic on TCP Port 3306 (MySQL default).

### 3. Remote Client Connection
- Utilized a local SQL Client (e.g., MySQL Workbench / DBeaver) to establish a connection.
- Successfully routed the connection using the provided AWS RDS Endpoint URL and master credentials.

### 4. Query Execution
- Executed Data Definition Language (DDL) commands to create a new `school` database and a `students` table.
- Executed Data Manipulation Language (DML) commands to insert records and verify data retrieval using a `SELECT` statement.

## Proofs of Completion
- rds_endpoint.png: Screenshot of the AWS console showing the RDS instance in an "Available" state along with its endpoint URL.
- sql_connection.png: Screenshot of the local SQL client successfully connecting to the RDS endpoint.
- sql_query.png: Screenshot demonstrating the execution of basic SQL queries and the resulting data grid.