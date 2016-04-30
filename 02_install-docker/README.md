# Install Docker
## Install The Docker Toolbox
### Mac
[Mac install instructions](https://docs.docker.com/mac/step_one/)  

### Windows
[Windows install instructions](https://docs.docker.com/windows/step_one/)

## Run Docker container Hello World
In a command prompt/terminal window, run the following command:

    docker run hello-world

You should see output similar to:

    mtanaka@LM-SJL-00876424 ~/s/l/01_install-docker> docker run hello-world
    Unable to find image 'hello-world:latest' locally
    latest: Pulling from library/hello-world
    
    4276590986f6: Pull complete
    a3ed95caeb02: Pull complete
    Digest: sha256:4f32210e234b4ad5cac92efacc0a3d602b02476c754f13d517e1ada048e5a8ba
    Status: Downloaded newer image for hello-world:latest
    
    Hello from Docker.
    This message shows that your installation appears to be working correctly.
    
    To generate this message, Docker took the following steps:
     1. The Docker client contacted the Docker daemon.
     2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
     3. The Docker daemon created a new container from that image which runs the
        executable that produces the output you are currently reading.
     4. The Docker daemon streamed that output to the Docker client, which sent it
        to your terminal.
    
    To try something more ambitious, you can run an Ubuntu container with:
     $ docker run -it ubuntu bash
    
    Share images, automate workflows, and more with a free Docker Hub account:
     https://hub.docker.com
    
    For more examples and ideas, visit:
     https://docs.docker.com/engine/userguide/
