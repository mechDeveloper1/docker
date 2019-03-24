# docker

## Basic docker commands

### Check docker version

`docker version`

### Check docker info

`docker info`

### List running containers

`docker ps`

### List all containers

`docker ps -a`

### List all images on docker host

`docker images`

### Search for an image on Docker hub

`docker search <imageName>`

### Pull an image from docker hub or on premise registry

`docker pull <imageName>`

### Start a container

`docker start -p <HostPort>:<ContainerPort> <imageName>`

### check container logs by attach command

`docker attach <containerId>`

### execute a command on a running container

`docker exec <containerId> <command>`

### execute a command on a running container interactive mode

`docker exec -it <containerId> <command>`
 

## Docker Swarm commands

### docker swarm help

`docker swarm --help`

### initialize swarm

`docker swarm init`

### check swarm nodes

`docker node ls`

### list stack of services on swarm

`docker stack ls`

### list stack tasks

`docker stack ps <stackName>`

### create docker secret

`docker secret create`

### list docker secret

`docker secret ls`

### list networks

`docker network ls`

### create network

`docker network create <networkName>`

### inspect network

`docker network inspect <networkName>`

