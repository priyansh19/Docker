# Exploring Docker Networks..:

In this excersise we will learn how to configure two container using a custom docker network. When we use conecpt of containerisation it need strong hold on networking also. In docker we have 5 types of network connections..

- bridge: The default network driver. If you don’t specify a driver, this is the type of network you are creating. Bridge networks are usually used when your applications run in standalone containers that need to communicate. 

- host: For standalone containers, remove network isolation between the container and the Docker host, and use the host’s networking directly. host is only available for swarm services on Docker 17.06 and higher. 

- overlay: Overlay networks connect multiple Docker daemons together and enable swarm services to communicate with each other. You can also use overlay networks to facilitate communication between a swarm service and a standalone container, or between two standalone containers on different Docker daemons. This strategy removes the need to do OS-level routing between these containers. 

- macvlan: Macvlan networks allow you to assign a MAC address to a container, making it appear as a physical device on your network. The Docker daemon routes traffic to containers by their MAC addresses. Using the macvlan driver is sometimes the best choice when dealing with legacy applications that expect to be directly connected to the physical network, rather than routed through the Docker host’s network stack. 

- none: For this container, disable all networking. Usually used in conjunction with a custom network driver. none is not available for swarm services. 

## Docker commands for networking:

#### To list all the networks we have in our docker use 

```shell
$ sudo docker network ls
```
#### Creating a docker network 

```shell
$ sudo docker network -d <Network type> <nameOfNetwork>

// here -d is simply used for specifying network type 
```
#### To connect with a network we have two ways :

- To directly attach network type while we start the instance along with command

```shell
$ sudo docker run -it --net=<NameOfNetwork> <ContainerName>
```
- To add an endpoint of a network while container is running
// Docker networking allows you to connect you to as many as containers you want with a single network

```shell
$ sudo docker network connect <NetworkName> <ContainerName>
```
#### Disconnecting a container from a network

```shell
$ sudo docker network disconnect <NameOfNetwork> <NameOfContainer> 
```