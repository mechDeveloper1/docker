# docker-machine

https://docs.docker.com/machine/

## boot2docker

https://docs.docker.com/machine/

## basic docker-machine commands

### show the docker machine version or a machine docker version

`docker-machine version`

### shows a list of commands or help for one command

`docker-machine help`

### list machines

`docker-machine ls`

### create a machine

`docker-machine create default`


### create a machine with proxy
docker-machine create -d virtualbox \
    --engine-env HTTP_PROXY=http://example.com:8080 \
    --engine-env HTTPS_PROXY=https://example.com:8080 \
    --engine-env NO_PROXY=example2.com \
    proxybox



### remove a machine

`docker-machine rm default`

### display commands to set up the environment of the docker client

`docker-machine env default`

### command to set up environment of docker client in bash on windows

`eval $(docker-machine env default)`

### inspect information about a machine

`docker-machine inspect default`

### get status of a machine

`docker-machine status default`

### get the url of a machine

`docker-machine url default`

### restart a machine

`docker-machine restart default`

### stop a machine

`docker-machine stop default`

### start a machine

`docker-machine start default`

### get ip of a running machine

`docker-machine ip default`

### upgrade a machine to the latest version of docker

`docker-machine upgrade docker`

### Log into or run a command on a machine with SSH

`docker-machine ssh default`

`sudo -i` // change to root user for boot2docker linux 

### SSH into VM
`$ docker-machine ssh default`
Docker Machine auto logs in using the generated SSH key, but if you want to SSH into the machine manually (or you're not using a Docker Machine managed VM), the credentials are:
```
user: docker
pass: tcuser
```
### restart docker from inside boot2docker
`/etc/init.d/docker restart`
