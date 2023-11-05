# Kubernetes manifests with Helm

This repository contains the source code and Helm charts for managing applications on Kubernetes, along with a CI/CD pipeline for automated deployment.

## Overview

This project is designed to simplify the deployment and management of applications on Kubernetes using Helm charts. The included CI/CD pipeline automates the process of deploying Helm releases to your Kubernetes cluster.

# Getting Started

### Prerequisites

Before you begin, ensure you have the following prerequisites:

- [Helm](https://helm.sh/docs/intro/install/) installed

### Project Structure

- `/fourlanches-app`: Contains Helm charts for FourLanches application.

### Usage

1. Customize Helm charts in their respective directories according to application.

2. Commit and push changes to your branch and make a pull request to the main branch. This should trigger the CI/CD pipeline, which will validate if the Chart is successfully compiled, and right after the merge, it will apply the changes to the Kubernetes cluster.

### Local Development

For local development and testing, you can use the following commands:

- To lint and validate Helm charts:

  ```shell
  helm lint ./fourlanches-app
  ```