# Intro to containers
You can think of containers as short-lived instances of VMs which expect to run a single command and once that command is completed, it shuts the container down.  Every container is configured to run a command.  When a container is started, that command is run.  The command can be any command line program.  The command run is configured in the container's image.

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

Note: When you run a container, you are launching a new container.  If you want to login to a running container, you will need to execute a command within the container attached to an interactive tty.

## Logging in to container
It is considered best practice not to run an sshd server within your docker container and allow ssh connections into it.  Instead, running a bash command within the container is considered the most secure best practice.

    # login to a running container
    docker exec -it ubuntu1 bash
    
## List all containers installed
To see a list of all containers that have been run:

    docker ps -a

## Container management
Containers are not started when the docker-machine is first started up.  You can start, stop, or remove containers as you wish.

    # start a container
    docker start [NAME OF CONTAINER]
    
    # stop a container
    docker stop [NAME OF CONTAINER]
    
    # remove a container
    docker rm [NAME OF CONTAINER]
