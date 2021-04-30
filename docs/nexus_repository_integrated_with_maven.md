<img src="images/c4logo.png">

### Steps:
1. Login to your Linux VM and [Install docker](https://github.com/submah/docker-tutorials/blob/master/docker-installation.md)
2. We are going to launch nexus through docker image. Execute the below commands to access nexus UI

```docker
# Create a docker volume

docker volume create local-nexus-data

docker run -d -p 8081:8081 --name nexus -v local-nexus-data:/nexus-data sonatype/nexus3

```