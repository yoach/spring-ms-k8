# Spring-MS-k8
Basic spring ms example  with k8 deploy

![alt text](https://kubernetes.io/images/favicon.png)

## Requirements

* [Java 11](https://www.oracle.com/java/technologies/javase/jdk11-archive-downloads.html)
* [Idea](https://www.jetbrains.com/idea/)
* [Docker ](https://docs.docker.com/engine/install/)
* [Dockerhub](https://hub.docker.com/)
* [Spring ms-k8 sample](https://github.com/yoach/spring-ms-k8)
* [Minikube](https://kubernetes.io/docs/tutorials/hello-minikube/)

 
## Getting Started

### Gitub
1.Pull spring ms-k8 sample to your local mechine.
2.run code and check it by enter browser

### Preper Docker Image

1.Dockerfile build image -- > docker build -t spring-boot-ms-docker .

2.Run docker local --> docker run -p 8080:8080 spring-boot-ms-docker

3.Dockerhub login -->  docker login -u *****-p ***** docker.io

4.Tag docker -- > docker tag spring-boot-ms-docker example-spring-boot-ms-docker

5.Push docker --> docker push yoachpi/example-spring-boot-ms-docker

### minikube Deploy image 
1.Run minikube https://kubernetes.io/docs/tutorials/hello-minikube

2.minikube dashboard --url

3.Create deployment  -- > kubectl create deployment example-spring-boot-ms-docker  --image=yoachpi/example-spring-boot-ms-docker

4.Create service -- > kubectl expose deployment example-spring-boot-ms-docker --type=LoadBalancer --port=8080

5.Connect using external port  -- >  kubectl get services 


