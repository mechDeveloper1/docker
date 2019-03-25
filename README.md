# docker

## Basic docker commands

### check docker version

`docker version`

### check docker info

`docker info`

### create an image

`docker build -t <imageName>:<imageTag> .`

### list all images on docker host

`docker images`

### search for an image on Docker hub

`docker search <imageName>`

### pull an image from docker hub or on premise registry

`docker pull <imageName>`

### push an image from docker hub or on premise registry

`docker push <imageName>`

### tag an image with a different name

`docker tag <newImageName> <oldImageName>` 

### run a container from an image

`docker run -d -p <hostPort>:<containerPort> <imageName> <containerName>`

### run a container from an image with a volume mount

`docker run -d -v <localPath>:<containerPath> -p <hostPort>:<containerPort> <imageName> <containerName>`

### stop a running container

`docker stop <CONTAINERID>`

### commit a running container as a new image

`docker commit <CONTAINERID> <imageName>`

### list running containers

`docker ps`

### list all containers

`docker ps -a`

### start a stopped container

`docker start -p <HostPort>:<ContainerPort> <imageName>`

### check container logs by attach command

`docker attach <containerId>`

### execute a command on a running container

`docker exec <containerId> <command>`

### execute a command on a running container interactive mode

`docker exec -it <containerId> <command>`

### copy a file from localmachine to dockercontainer

`docker cp <localFilePath> <CONTAINERID>:<contianerPath>`

### copy a file from localmachine to dockercontainer

`docker cp <CONTAINERID>:<contianerPath> <localFilePath> `

### kill a container

`docker kill <containerId>`

### remove a container

`docker rm <containerId>`

## Docker Swarm commands

### docker swarm help

`docker swarm --help`

### initialize swarm

`docker swarm init`

### check swarm nodes

`docker node ls`

### create a service 

`docker service create [OPTIONS] <imageName>`

### deploy a stack

`docker stack deploy --compose-file docker-compose.yml <stackName>`

### list stack

`docker stack ls`

### list stack tasks

`docker stack ps <stackName>`

### list stack services 

`docker stack services <stackName>`

### remove a stack

`docker stack rm <stackName>`

### create docker secret

`docker secret create <secretName> <secretSourcePath>`

### list docker secret

`docker secret ls`

### list networks

`docker network ls`

### create network

`docker network create <networkName>`

### inspect network

`docker network inspect <networkName>`

### check live stream of contianer(s) usage statistics

`docker stats`

