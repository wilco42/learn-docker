# Intro to containers
You can think of containers as "short-lived" instances of VMs which expect to run a command and once that command is completed, it shuts the container down.  Every container is configured to run a command.  When a container is started, that command is run.  The command can be any command line program.  The command run is configured in the container's image.

## Launch a new container
To launch a new container:
docker run -it --name [NAME OF CONTAINER]* [CONTAINER IMAGE]**

    # launch an ubuntu container
    # this will fetch the ubuntu image, run the container, and log you in to the container
    docker run -it --name ubuntu1 ubuntu

    # launch a different ubuntu container from the same image
    docker run -it --name ubuntu2 ubuntu

    # launch a centos container
    docker run -it --name centos centos

    
## List all containers installed
To see a list of all containers that have been run:

    docker ps -a    

## Container management
    # start a container
    docker start [NAME OF CONTAINER]
    
    # stop a container
    docker stop [NAME OF CONTAINER]
    
    # remove a container
    docker rm [NAME OF CONTAINER]
    
    # login to a container
    docker exec -it ubuntu1 bash

## Docker image management
    # see all docker images available locally
    docker images
    
    # remove a docker image
    docker rmi [NAME OF IMAGE]
