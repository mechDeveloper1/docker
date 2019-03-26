# docker-machine

## basic docker-machine commands

### show the docker machine version or a machine docker version

`docker-machine version`

### shows a list of commands or help for one command

`docker-machine help`

### list machines

`docker-machine ls`

### create a machine

`docker-machine create default`

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

### upgrade a machine to the latest version of docker

`docker-machine upgrade docker`

### Log into or run a command on a machine with SSH

`docker-machine ssh default`

`sudo -i` // root user for boot2docker linux 
