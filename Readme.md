# Beginner Kubernetes Project

## Description

This project is an example application that demonstrates how to deploy a simple mern application using Kubernetes.

## Getting Started

### Prerequisites

To run this application, you need the following tools installed on your machine:

- Kubernetes (kubectl)
- Minikube
- Docker (for building custom images)

### Deployment

Clone this repository to your local machine:

```
git clone https://github.com/brf153/kubernetes-beginner-project
cd kubernetes-beginner-project
```

### First install kubectl and minicube 

If you have brew installed on your system, you can use the command:-

```
brew install kubectl
brew install minikube
```
Else read the docs for installation:-

Kubectl: https://kubernetes.io/docs/tasks/tools/install-kubectl-windows/

Minikube: https://minikube.sigs.k8s.io/docs/start/

### After Installation:-

Write the commands below in your terminal(note that you have to open terminal in administrator mode)

```
minikube start
kubectl apply -f mongo-config.yaml
kubectl apply -f secret.yaml
kubectl apply -f mongo-app.yaml
kubectl apply -f web-app.yaml

```

Now, in order to check whether everything has been done for the deployment:-

```
kubectl get pod
kubectl get pod
kubectl get configmap
kubectl get secret
kubectl get svc
minikube ip
kubectl get node -o wide
```

Now, start the service(or the deployment process):-

```
minikube service webapp-service
```

### $${\color{red}Note:}$$

$${\color{red}
You \space might \space face \space issue \space while \space running \space the \space Minikube \space commands \space if \space you \space are \space using \space Windows \space 11 \space Home \space edition
}$$

$${\color{red}\space as \space Hyper-V \space is \space not \space available.So, \space first \space install \space Hyper-V \space in \space you \space system \space and \space then \space run \space the \space minikube \space commands.
}$$



  


