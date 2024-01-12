# Dockerizing React App with NGINX and Kubernetes Deployment using Helm
This project demonstrates how to Dockerize a React app with NGINX, and deploy it on Kubernetes using Helm Chart. Follow these steps to build the Docker image, create a Kubernetes Deployment, expose it as a service, and access the application through Minikube.

## Prerequisites
+ `Docker` installed on your machine.
+ `kubectl` installed on your machine.
+ `Minikube` installed on your machine.
+ `Helm` installed on your machine.

## Step 1: Start Minikube
Start `Minikube` with the following command:
```js
minikube start --driver=docker
```

## Step 2: Enable Docker Environment for Minikube
Set the `Docker` environment variables to use the `Minikube Docker` daemon:
```js
eval $(minikube -p minikube docker-env)
```

## Step 3: Clone the Repository
```js
git clone <repository-url>
cd <repository-directory>
```

## Step 4: Create a .dockerignore file
Create a `.dockerignore` file in the root directory with the following content:
```js
node_modules
```

## Step 5: Create a Dockerfile
Create a `Dockerfile` in the root directory. Refer to the script above.

## Step 6: Create Kubernetes Deployment (deployment.yaml)
Create a `deployment.yaml` file in the root directory. Refer to the script above.

## Step 6: Create Kubernetes Service (service.yaml)
Create a `service.yaml` file in the root directory. Refer to the script above.

## Step 7: Create Helm Charts:
Create a `chart.yaml` in the new directory. Refer to the script above.

## Step 8: Install the Helm Chart
Install the `chart.yaml` using the following commands:
```js
helm install <helm_directory> --generate-name
```
## Step 9: Access the Application through Minikube
Get the `Minikube` IP and open the React app in your web browser:
```js
minikube service appserver-clusterip-service
```


