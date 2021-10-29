# spring-ms-k8
basic spring ms example with k8 deploy

## Requirements

* [java 11](https://www.oracle.com/java/technologies/javase/jdk11-archive-downloads.html)
* [idea](https://www.jetbrains.com/idea/)
* [docker ](https://docs.docker.com/engine/install/)
* [dockerhub](https://hub.docker.com/)
* [spring ms-k8 sample](https://github.com/yoach/spring-ms-k8)
* [minikube](https://kubernetes.io/docs/tutorials/hello-minikube/)

 
## Getting Started

1.Pull spring ms-k8 sample to your local mechine.

### Preper Docker Image

1.Dockerfile build image -- > docker build -t spring-boot-ms-docker .

2.Run docker local --> docker run -p 8080:8080 spring-boot-ms-docker

3.Dockerhub login -->  docker login -u *****-p ***** docker.io

4.Tag docker -- > docker tag spring-boot-ms-docker example-spring-boot-ms-docker

5.Push docker --> docker push yoachpi/example-spring-boot-ms-docker

### minikube Deploy image 
1.Run minikube https://kubernetes.io/docs/tutorials/hello-minikube
2.minikube dashboard
3.Create deployment  -- > kubectl create deployment example-spring-boot-ms-docker  --image=yoachpi/example-spring-boot-ms-docker
4.Create service -- > kubectl expose deployment example-spring-boot-ms-docker --type=LoadBalancer --port=8080

