DevOps task
---
<img src="Logotype primary.png" width="30%" height="30%" />

It's answear to devops task given to me at recrutaion process.

Based on react example from *create-react-app* tutorial.

[See the react app details](https://github.com/ahfarmer/calculator).


Description
--
App is docerized and send to dockerhub by github actions.
Files pod.yml and service.yml is used at kubernetes.


How to use - DockerCompose way
--
To build app with DockerCompose clone repo to your server with 
```
 git clone https://github.com/tomekcrm/devops-task.git
```
go to /app folder and use
 
```
#Use sudo if needed
~ sudo docker-compose -f docker-compose.dev.yml build
~ sudo docker-compose -f docker-compose.dev.yml up -d
```


How to use - Local Docker Way
--
To build app with DockerCompose clone repo to your server:
```
~ git clone https://github.com/tomekcrm/devops-task.git

# Go to /app folder and use:

~ docker-compose -f docker-compose.dev.yml build
~ docker-compose -f docker-compose.dev.yml up -d
```


How to use - DockerHub way
--
To build app with container from dockerhub use:
```
# Use sudo if needed
~ sudo docker run --name appcalc  -p 8080:3000 -d tomaszcrm/devops-ci-pipeline

```


How to use - Kubernetes way
--
To build app at kuberentes cluster:
```
# Clone repo and use pod.yml to build pod next service.yml to make kuberentes service

~ git clone https://github.com/tomekcrm/devops-task.git
~ kubectl apply -f pod.yaml
~ kubectl apply -f service.yaml
 
# Default use NodePort: 8080

```

