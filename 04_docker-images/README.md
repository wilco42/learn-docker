# Docker images
Docker images are similar to golden images for VMs.  They are the snapshot from which docker containers are initially launched.  Docker images are distributed at the [Docker Hub](https://hub.docker.com/).  You can launch a Docker container from any Docker image.

# Dockerfile    
Docker images are binaries that can be distributed.  Dockerfiles are used to create a Docker image.  A Dockerfile is a text document that contains all of the commands necessary to create an image.

    #
    # Ubuntu Dockerfile
    #
    # https://github.com/dockerfile/ubuntu
    #
    
    # Pull base image.
    FROM ubuntu:14.04
    
    # Install.
    RUN \
      sed -i 's/# \(.*multiverse$\)/\1/g' /etc/apt/sources.list && \
      apt-get update && \
      apt-get -y upgrade && \
      apt-get install -y build-essential && \
      apt-get install -y software-properties-common && \
      apt-get install -y byobu curl git htop man unzip vim wget && \
      rm -rf /var/lib/apt/lists/*
    
    # Add files.
    ADD root/.bashrc /root/.bashrc
    ADD root/.gitconfig /root/.gitconfig
    ADD root/.scripts /root/.scripts
    
    # Set environment variables.
    ENV HOME /root
    
    # Define working directory.
    WORKDIR /root
    
    # Define default command.
    CMD ["bash"]


## Docker image management
    # see all docker images available locally
    docker images
    
    # remove a docker image
    docker rmi [NAME OF IMAGE]



Refs:  
[Dockerfile Reference Documentation](https://docs.docker.com/engine/reference/builder/)   
[Dockerfiles to automate building images](https://www.digitalocean.com/community/tutorials/docker-explained-using-dockerfiles-to-automate-building-of-images)
