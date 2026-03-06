# 🧾 Project 4 - Sales System with PostgreSQL and MongoDB

This Java project simulates a **sales management system** with data
persistence in a **relational database (PostgreSQL)** and also stores
**sales logs in a document database (MongoDB)**.

------------------------------------------------------------------------

# 🚀 Technologies Used

-   Java 17
-   Maven
-   Hibernate (JPA)
-   PostgreSQL (via JPA)
-   MongoDB (for logs)
-   Docker and Docker Compose
-   PgAdmin4

------------------------------------------------------------------------

# 📦 Features

-   Registration of **customers**, **products**, and **sales**
    (relational storage with PostgreSQL)
-   Storage of **sales logs** in MongoDB (document database)
-   Application execution via Maven (`exec-maven-plugin`)
-   Database environment running with Docker
-   Visual database interface with PgAdmin

------------------------------------------------------------------------

# 🛠️ How to Run the Project

## 1️⃣ Start the environment with Docker

``` bash
docker-compose up -d
```

Services available:

**PostgreSQL**

    localhost:5432

**MongoDB**

    localhost:27017

**PgAdmin4**

    http://localhost:5050

Login:

    Email: admin@admin.com
    Password: admin

------------------------------------------------------------------------

## 2️⃣ Build the project with Maven

``` bash
mvn clean install
```

------------------------------------------------------------------------

## 3️⃣ Run the application

``` bash
mvn exec:java
```

Expected output:

    Sales log successfully sent to MongoDB!

------------------------------------------------------------------------

# 🗃️ Project Structure

    src/
    ├── main/
    │   ├── java/
    │   │   ├── app/                # Main.java class
    │   │   ├── dao/                # PostgreSQL DAOs + LogVendaDAO (Mongo)
    │   │   ├── model/              # JPA entities
    │   │   └── database/           # JPA + MongoDB connection
    │   └── resources/
    │       └── META-INF/
    │           └── persistence.xml # JPA configuration
    docker-compose.yml
    pom.xml
    README.md

------------------------------------------------------------------------

# 🧪 Testing MongoDB

You can use:

### MongoDB Compass

Connect to:

    mongodb://localhost:27017

### Command line (mongosh)

``` bash
mongosh
use vendasdb_mongo
db.log_vendas.find().pretty()
```

------------------------------------------------------------------------

# 📄 Databases

### PostgreSQL

Database:

    vendasdb

User:

    postgres

Password:

    postgres

------------------------------------------------------------------------

### MongoDB

Database:

    vendasdb_mongo

Collection:

    log_vendas

------------------------------------------------------------------------

# ✍️ Author

Made with 💻 by **Igor Programmer**
