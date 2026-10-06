OpenShift CI/CD Pipeline Automation

Project Overview

This project demonstrates the implementation of a complete CI/CD pipeline for a sample application using GitHub Actions, Tekton, and OpenShift.

The project automates key software delivery activities including code linting, unit testing, pipeline task execution, application deployment, and validation on an OpenShift cluster.

Project Objectives

The main objectives of this project are:

- Implement continuous integration using GitHub Actions
- Automate code quality checks using Flake8/ESLint
- Execute automated unit tests using Nose/Jest
- Create reusable CI/CD tasks using Tekton
- Configure cleanup and testing tasks in Tekton
- Deploy the application using an OpenShift Pipeline
- Verify successful application deployment and execution
- Monitor application logs and pipeline execution

Technologies Used

- GitHub
- GitHub Actions
- Tekton Pipelines
- OpenShift
- YAML
- Python / JavaScript
- Flake8 / ESLint
- Nose / Jest
- Docker / Containers

CI/CD Workflow

The project follows this general workflow:

Developer
    |
    v
GitHub Repository
    |
    v
GitHub Actions
    |
    +----> Lint / Code Quality Check
    |
    +----> Unit Tests
    |
    v
Tekton Tasks
    |
    +----> Cleanup Task
    |
    +----> Test Task
    |
    v
OpenShift Pipeline
    |
    v
Application Deployment
    |
    v
OpenShift Application
    |
    v
Application Logs / Validation

GitHub Actions

The GitHub Actions workflow performs automated validation whenever the workflow is triggered.

The workflow includes:

1. Checking out the source code
2. Installing required dependencies
3. Running the linting step using Flake8/ESLint
4. Running unit tests using Nose/Jest
5. Reporting the workflow status

Workflow configuration:

.github/workflows/workflow.yml

Tekton Pipeline Tasks

Tekton is used to define reusable pipeline tasks for the CI/CD process.

The Tekton configuration includes:

- Cleanup task
- Application testing task
- Required parameters and workspaces
- Task execution required by the OpenShift pipeline

Tekton configuration:

.tekton/tasks.yml

OpenShift Deployment

The application is deployed to an OpenShift cluster using an OpenShift Pipeline.

The project includes verification of:

- PersistentVolumeClaim configuration
- OpenShift pipeline configuration
- Successful pipeline execution
- Application deployment
- Application logs

Project Validation

The implementation is validated using:

- Successful GitHub Actions workflow execution
- Successful linting and unit tests
- Successful Tekton task execution
- OpenShift PersistentVolumeClaim details
- Successful OpenShift pipeline execution
- Successful application deployment
- Application logs confirming the application is running

Repository Structure

.
├── .github/
│   └── workflows/
│       └── workflow.yml
│
├── .tekton/
│   └── tasks.yml
│
├── README.md
│
└── application source files

Final Project

This project was completed as part of the Coursera CI/CD course final project and demonstrates practical knowledge of CI/CD automation, GitHub Actions, Tekton, and OpenShift.

---

Project Description

A complete CI/CD pipeline project that automates application linting, unit testing, and deployment using GitHub Actions, Tekton, and OpenShift. The project demonstrates continuous integration, pipeline task automation, containerized application deployment, and successful application delivery on an OpenShift cluster.
