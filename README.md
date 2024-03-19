# Kubernetes manifests with Helm

This repository contains the source code and Helm charts for managing applications on Kubernetes, along with a CI/CD pipeline for automated deployment.

## Overview

This project is designed to simplify the deployment and management of applications on Kubernetes using Helm charts. The included CI/CD pipeline automates the process of deploying Helm releases to your Kubernetes cluster.

# Getting Started

### Prerequisites

Before you begin, ensure you have the following prerequisites:

- [Helm](https://helm.sh/docs/intro/install/) installed

### Project Structure

Sure, I can help you generate a project structure for your README file. Based on the `Chart.yaml` file, it seems like your project is structured with each microservice having its own chart. Here's a suggested project structure:

## Project Structure

```
├── Chart.yaml
├── charts/
│   ├── order-app/
│   │   ├── Chart.yaml
│   │   ├── templates/
│   │   ├── values.yaml
│   ├── payment-app/
│   │   ├── Chart.yaml
│   │   ├── templates/
│   │   ├── values.yaml
│   ├── kitchen-app/
│   │   ├── Chart.yaml
│   │   ├── templates/
│   │   ├── values.yaml
│   ├── customer-app/
│   │   ├── Chart.yaml
│   │   ├── templates/
│   │   ├── values.yaml
│   ├── sonarqube/
│   │   ├── Chart.yaml
│   │   ├── templates/
│   │   ├── values.yaml
├── values.yaml
```

Each application (order-app, payment-app, kitchen-app, customer-app, sonarqube) has its own directory under the `charts/` directory. Each of these directories contains a `Chart.yaml` file that describes the chart, a `values.yaml` file that specifies default configuration values, and a `templates/` directory that contains templates for Kubernetes resources.


### Usage

1. Customize Helm charts in their respective directories according to application.

2. Commit and push changes to your branch and make a pull request to the main branch. This should trigger the CI/CD pipeline, which will validate if the Chart is successfully compiled, and right after the merge, it will apply the changes to the Kubernetes cluster.

### Local Development

For local development and testing, you can use the following commands:

- To lint and validate Helm charts:

  ```shell
  helm lint .
  ```