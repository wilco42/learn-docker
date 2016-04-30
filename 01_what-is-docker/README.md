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
- Better resource utilization per server
- Near instantaneous container startup

## What are the cons?
- All containers must use the same OS as its host.  Cannot use multiple versions of an OS within the same server.
- Container management tools are primitive and mostly command line driven
- Containers do not have an /etc/rc.d

Refs:  
[What is Docker?](https://www.docker.com/what-docker)
