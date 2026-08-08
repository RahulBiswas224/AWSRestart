```markdown
# 🗄️ Database Migration to Amazon RDS

**Project Objective:** Migrate a dynamic web application's local database (running on an EC2 instance) to a fully managed Amazon Relational Database Service (Amazon RDS) instance, resulting in a more secure, scalable, and highly available architecture. 

---

## 🏗️ Architecture Overview

<div align="center">
  <img src="image_5bff80.jpg" alt="Cafe Web Application Migration - Before and After Architecture">
</div>

<br>

**Before Migration (Starting Architecture):**
The café web application and its MariaDB database were hosted together on a single Amazon EC2 LAMP (Linux, Apache, MySQL, PHP) instance within a public subnet.

**After Migration (Final Architecture):**
The local database was migrated to a fully managed Amazon RDS MariaDB instance residing in a private subnet. The application on the EC2 instance now connects securely to the RDS instance across the Virtual Private Cloud (VPC).

---

## 🛠️ Step-by-Step Execution

### Phase 1: Infrastructure Provisioning (AWS CLI)
To build a secure environment for the new database, I utilized the AWS CLI via an EC2 CLI Host to configure the networking and security perimeters.

1. **Security Group Configuration:**
   Created a dedicated security group (`CafeDatabaseSG`) for the RDS instance. Added an inbound rule to allow TCP traffic on port 3306 (MySQL) *only* from the application's specific security group (`CafeSecurityGroup`), ensuring the database is not publicly accessible.
   
   ```bash
   aws ec2 authorize-security-group-ingress \
     --group-id <CafeDatabaseSG_Group_ID> \
     --protocol tcp --port 3306 \
     --source-group <CafeSecurityGroup_Group_ID>

```

2. **Subnet and DB Subnet Group Creation:**
Created two new private subnets across different Availability Zones to ensure high availability (e.g., CIDR blocks `10.200.2.0/23` and `10.200.10.0/23`). Grouped these into a DB Subnet Group (`CafeDB Subnet Group`).
3. **Deploying the RDS Instance:**
Launched a `db.t3.micro` MariaDB instance within the newly created private subnet group and attached the dedicated security group.

### Phase 2: Data Extraction & Migration

Connected securely to the application instance using EC2 Instance Connect to extract the existing data and push it to the new RDS environment.

1. **Database Export:**
Utilized the `mysqldump` utility to extract the schema and data from the local `cafe_db` database into a SQL backup file.
```bash
mysqldump --user=root --password='Re:Start!9' \
  --databases cafe_db --add-drop-database > cafedb-backup.sql

```


2. **Database Import:**
Used the `mysql` client to connect to the new RDS endpoint and restored the data from the backup file.
```bash
mysql --user=root --password='Re:Start!9' \
  --host=<RDS_Instance_Endpoint> < cafedb-backup.sql

```



### Phase 3: Application Reconfiguration

To cut over the application to the new database without hardcoding credentials, I leveraged **AWS Systems Manager Parameter Store**.

* Navigated to the `/cafe/dbUrl` parameter in Systems Manager.
* Updated the connection string value to point to the new Amazon RDS endpoint address.
* Verified the web application successfully loaded and that the historical order data was intact.

### Phase 4: Observability & Monitoring

To ensure the database was performing optimally post-migration, I utilized **Amazon CloudWatch** through the RDS Management Console.

* Monitored key metrics including `CPUUtilization`, `FreeStorageSpace`, and `FreeableMemory`.
* Specifically tracked the `DatabaseConnections` metric, successfully observing the active connection spike when executing an interactive SQL session from the EC2 instance.

---



```

```
