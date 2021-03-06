# What is Docker ?

**Docker** is a tool used to automate the deployments of an application in lightweight containers so that application can work efficiently in different environments 

<p align='center'>
	<img width="336" height="270" src="https://github.com/priyansh19/Fun-With-Docker/blob/master/Images/geektechstuff_docker.png">
</p>

## What are containers ?

**Containers** are completely **Isolated Environments** as in they can have their own processes, services, networking and a lot of things using the **Kernel** of the Host machine. There are various types of containers and Docker uses LXC type of containers.

The **Biggest difference** between Containers and Virtual Machines is that the container are quiet different as they all shares one kernel and the virtual machines have a seperate kernel running in each and the containers don't use the principle of virtualization its just using a kernel for different operating os.

<p align='center'>
	<img width="700" height="350" src='https://github.com/priyansh19/Fun-With-Docker/blob/master/Images/Containers_vs_images.png'>
</p>

Docker can't run Windows OS with linux kernel on the same hardware because unlike Hypervisors, Docker is not meant to run and virtualise different Operating Systems and kernels on same hardware. The main aim of Docker is to package, maintain an environment and to ship them and to run them anywhere and as many times as you want.

## Architechture of Docker

<p align='center'>
	<img src="https://github.com/priyansh19/Fun-With-Docker/blob/master/Images/architechture.webp">
</p>

### Components of Docker architechture are :

**Docker Client**

- It is the primary way to interact with Docker. When we use commands like Docker run it is the client which sends this command to docker daemon which then executes the command.

**Docker Host or Docker Daemon**

- The Docker daemon (dockerd) listens for Docker API requests and manages Docker objects such as images, containers, networks, and volumes. A daemon can also communicate with other daemons to manage Docker services.

**Docker Registry**

- A Docker registry stores Docker images. Docker Hub is a public registry that anyone can use, and Docker is configured to look for images on Docker Hub by default. You can even run your own private registry. If you use Docker Datacenter (DDC), it includes Docker Trusted Registry (DTR).</br>
When you use the docker pull or docker run commands, the required images are pulled from your configured registry. When you use the docker push command, your image is pushed to your configured registry.

## Why do you need Docker ? 

* Compatibility and Dependency issues over long term use of a same environment.
* Long time to setup similar environment for a new user
* There are different environments with different dependencies for development/Testing and for production as well 

## Is Docker Useful for running GUI Applications?

Docker could help solve some challenges associated with desktop apps. For example, it could enable truly platform-agnostic app packages. We’ve come a long way since the days when you had to compile your app from source to make it run on your system. But most installation packages available today are still tied to a particular Linux distribution or version of Windows. With Docker, it finally would be possible to have a single package format for installing a given application on any Linux or Windows system.

In further excersises we will build a simple docker container to run a simple GUI Application.

 

