# Introduction to Docker
## Docker vs. VMs
<table border="0">
<tr>
    <td>
    <img src="what-is-docker-diagram.png" width="250" />
    </td>
    <td>
    <img src="what-is-vm-diagram.png" width="250" />
    </td>
</tr>
<tr>
    <td>VMs</td>
    <td>Docker</td>
</tr>
</table>

## What are the pros?
- Better resource utilization per server.
- Near instantaneous container startup.
- Dockerfiles create and setup containers.

## What are the cons?
- All containers must use the same OS as its host.  Cannot use multiple versions of an OS within the same server.
- All containers must use the same kernel as its host.
- Container management tools are primitive and mostly command line driven.
- Containers do not have an /etc/rc.d, they expect to run only 1 command.
- Only runs on Linux.

## Docker terminology
### Docker host
A Docker host is the server that does the work of building and running containers by running the Docker Daemon.  Docker hosts only run on Linux, however the Docker host can be run inside a VM.

If a Docker host is run inside a VM (so you can run Docker on a Windows or Mac machine) it is called a Docker Machine.  The Docker Toolbox provides a command line interface to create and manage the Linux VM Host.

### Docker images
Docker images are like VM golden images.  They are templates that your docker containers are started from.

### Docker containers
Docker containers are like VM instances.  They can be created, started, stopped, deleted, etc.


Refs:  
[What is Docker?](https://www.docker.com/what-docker)
