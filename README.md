# BobApp

## Introduction
BobApp is a web application project aimed at providing users with a collection of jokes. The project involves both front-end and back-end components. The goal is to implement Continuous Integration/Continuous Deployment (CI/CD) pipelines for automated testing, code analysis, and Docker image publishing on Docker Hub. This README.md provides instructions on setting up and running the project, as well as configuring CI/CD pipelines.

## CI/CD Pipeline Implementation

The goal of the CI/CD pipeline is to automate the testing, code analysis, and Docker image publishing processes. The pipeline consists of the following steps:

1. **Unit Testing**: Run unit tests for both front-end and back-end components.
2. **Code Analysis**: Analyze code quality using SonarQube.
3. **Docker Image Publishing**: Publish Docker images to Docker Hub.

The CI/CD pipeline is triggered on each push to the repository. Configuration files for CI/CD tools like Jenkins, GitLab CI/CD, or GitHub Actions can be found in the respective folders.


## Setup Instructions

### Front-end Setup

Navigate to the front-end folder:

```
cd front
```

Install dependencies:

```
npm install
```

Launch the front-end:

```
npm run start
```

#### Docker Setup

Build the front-end container:

```
docker build -t bobapp-front .
```

Start the front-end container:

```
docker run -p 8080:8080 --name bobapp-front -d bobapp-front
```

### Back-end Setup

Navigate to the back-end folder:

```
cd back
```

Install dependencies:

```
mvn clean install
```

Launch the back-end:

```
mvn spring-boot:run
```

Launch the tests:

```
mvn clean install
```

#### Docker Setup

Build the back-end container:

```
docker build -t bobapp-back .
```

Start the back-end container:

```
docker run -p 8080:8080 --name bobapp-back -d bobapp-back
```

If you have any questions or suggestions, please reach out to [paul.marniquet@gmail.com].
