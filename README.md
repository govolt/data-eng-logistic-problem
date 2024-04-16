# Data Engineering Logistic Problem

This project is designed to solve a logistic problem using data engineering tools and practices. It leverages Docker Compose to create a multi-container Docker application, which includes services for data processing and database management.

## Using Docker Compose

Docker Compose is used to define and run multi-container Docker applications. With a single command, you can spin up multiple containers that are required for this project, ensuring they are interconnected.

### What Docker Compose Will Spin Up

Running `docker-compose up` in the root directory of this project will spin up the following services:

- **PostgreSQL Database**: A PostgreSQL container to store and manage your data.
- **Data Processing Service**: This could be a custom application or a set of services designed to process your data, depending on how the `docker-compose.yml` is configured.

### How to Connect to the PostgreSQL Database

To connect to the PostgreSQL database, you will need to use the following connection details:

- **Hostname**: `localhost` (or the name of the service defined in `docker-compose.yml` if accessing from another service within the same network)
- **Port**: The default PostgreSQL port is `5432`.
- **Username**: The username specified in your `docker-compose.yml` file.
- **Password**: The password specified in your `docker-compose.yml` file.
- **Database Name**: The database name specified in your `docker-compose.yml` file.

You can use these details to connect to the database using your preferred PostgreSQL client.

### CSV in Input Folder

The CSV file located in the `input` folder is used to emulate data coming from external sources. This file can be processed by the data processing service to simulate real-world data ingestion and processing scenarios. Ensure that your data processing service is configured to watch this folder for new files or to process existing files upon startup.

## Getting Started

To get started with this project, follow these steps:

1. Fork this repo.
2. Ensure you have Docker and Docker Compose installed on your machine.
3. Clone this repository to your local machine.
4. Navigate to the root directory of the project in your terminal.
5. Run `docker-compose up` to build and start the containers.
6. Once the containers are running, you can connect to the PostgreSQL database using the connection details provided above.
7. To simulate data ingestion, you can add new CSV files to the `input` folder according to your testing needs.
8. Commit and push the solution to your repo.
