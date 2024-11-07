# Car Management Application

This project is a three-tier web application for managing car and owner details. It includes frontend and backend components, along with a MySQL database for data persistence. The project utilizes Docker for containerization and Jenkins for CI/CD automation.

## Table of Contents
- [Repositories](#repositories)
- [Application Overview](#application-overview)
- [Setup Requirements](#setup-requirements)
- [Deployment Steps](#deployment-steps)
- [Server Configuration](#server-configuration)
- [License](#license)

## Repositories

Fork the following repositories to get started:

- **Frontend**: [lbg-car-react-starter](https://github.com/qa-instructor/lbg-car-react-starter)
- **Backend**: [lbg-car-spring-app-starter](https://github.com/qa-instructor/lbg-car-spring-app-starter)

## Application Overview

The application has a three-tier architecture:
1. **Frontend**: React-based user interface.
2. **Backend**: Spring-based API server.
3. **Database**: MySQL database for data persistence.

Your task is to containerize and deploy the frontend, backend, and database.

## Setup Requirements

To complete the setup, you will need:

1. **New Server Setup**:
   - Provision a new server for deploying the containerized application.

2. **Dockerization**:
   - Write `Dockerfile`s for both the frontend and backend applications.
   - Follow Docker best practices to minimize the size of the final built images.

3. **CI/CD with Jenkins**:
   - Write a `Jenkinsfile` to automate the build process for both applications.
   - Create a `docker-compose.yml` file to define and deploy the application stack.

4. **Database Configuration**:
   - Include a MySQL container in your deployment to act as the database for the application.
   - Configure a mounted volume to persist database data.

## Deployment Steps

1. **Dockerize Applications**:
   - Create `Dockerfile`s for both the frontend and backend.
   - Ensure minimal image sizes by following Docker best practices.

2. **Jenkins Setup**:
   - Write a `Jenkinsfile` to define build and deployment pipelines for the applications.
   - Use `docker-compose` to deploy the services.

3. **Database Setup**:
   - Add a MySQL container in the `docker-compose.yml`.
   - Use a volume to persist MySQL data for reliability.

## Server Configuration

### Jenkins Server
- **SSH Key**: Generate an SSH key pair for Jenkins to securely connect to the deployment server.
  
### Target Deployment Server
- **Docker**: Install `docker` and `docker-compose`.
- **Jenkins User**:
  - Create a `jenkins` user.
  - Add the user to the Docker group.
  - Add the public key from the Jenkins server to the `authorized_keys` of this user.
- **Firewall**: Ensure ports 80 (HTTP) and 8000 (application) are open in the firewall for incoming connections.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

This README provides a clear structure and actionable steps, making it easy for others to understand the project requirements and follow the setup instructions. Let me know if you'd like any further customization!

Install docker and docker-compose.
Create a jenkins user with Docker permissions and add the Jenkins server’s public key to the authorized keys.
Open ports 80 and 8000 for web traffic, with the necessary firewall rules.
