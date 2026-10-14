# CI/CD Capstone Project - Application Deployment Pipeline

This repository contains the source code and CI/CD configuration for the final capstone project. The project demonstrates a complete automated delivery pipeline using **GitHub Actions** for continuous integration and **Tekton / OpenShift Pipelines** for cloud-native deployment.

## Project Overview

The main objective of this project is to automate the application development lifecycle, including code linting, unit testing, containerization, and continuous deployment to an Red Hat OpenShift cluster.

### Architecture & Components

- **Source Code**: Microservice application.
- **Continuous Integration (CI)**: Managed via **GitHub Actions** (`.github/workflows/workflow.yml`).
  - Code Linting (`flake8` / `eslint`)
  - Automated Unit Testing (`nosetests` / `jest`)
- **Continuous Deployment (CD)**: Managed via **Tekton Pipelines** on OpenShift (`.tekton/tasks.yml`).
  - Workspace Cleanup Task
  - Automated Testing Task
  - Image Build & Deployment to OpenShift Cluster

## Project Structure

```text
.
├── .github/
│   └── workflows/
│       └── workflow.yml    # GitHub Actions workflow definition (lint & test)
├── .tekton/
│   └── tasks.yml           # Tekton custom tasks definition (cleanup & test)
├── README.md               # Project documentation
└── ...                     # Application source files and configuration
