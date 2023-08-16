
# 💻Deploy Vue App in Azure using Azure Container Instances

This repository contains instructions and resources for deploying a Vue.js application as a Docker container with Nginx in Azure Container Instances.

## Table of Contents

- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Deployment Steps](#deployment-steps)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Welcome to the "Deploy Vue App in Azure using Azure Container Instances" project! This guide will walk you through the steps to deploy your Vue.js application as a Docker container with Nginx using Azure Container Instances, ensuring that your app is easily deployable and scalable.

## Prerequisites

Before you begin, make sure you have the following tools and accounts set up:

- [Docker](https://www.docker.com/)
- [Azure Account](https://azure.microsoft.com/)
- [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli)

## Deployment Steps

Follow these steps to deploy your Vue.js app as a Docker container with Nginx in Azure Container Instances:

1. Clone this repository: `git clone https://github.com/yourusername/deploy-vue-app-azure.git`
2. Navigate to the project directory: `cd deploy-vue-app-azure`
3. Build your Vue app: `npm install && npm run build`
4. Build your Docker image: `docker build -t vue-app .`
5. Push the Docker image to Docker Hub: `docker push yourusername/vue-app:latest`
6. Login to your Azure account: `az login`
7. Create an Azure Container Instance with port mapping: `az container create --name <container-name> --image yourusername/vue-app:latest --cpu <cpu-cores> --memory <memory-in-gb> --ports 80 --ip-address Public`

## Configuration

You can customize the container configuration, Nginx setup, and deployment process as needed. Make sure to update your Dockerfile and Nginx configuration files accordingly.

## Contributing

We welcome contributions to improve this guide and the deployment process. If you find any issues or have suggestions, feel free to open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
