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
1.pull spring ms-k8 sample to your local mechine.

2.docker build -t spring-boot-ms-docker . -->dockerfile build image

3.docker run -p 8080:8080 spring-boot-ms-docker

4.docker login -u *****-p ***** docker.io

5.
