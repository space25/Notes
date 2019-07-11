## Insrall Docker:
1. [Docker CE for Ubuntu](https://docs.docker.com/install/#supported-platforms)
1. [Get Docker CE for Ubuntu](https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/) or
    ```
    sudo snap install docker
    ```
1. [Post-installation steps for Linux](https://docs.docker.com/engine/installation/linux/linux-postinstall/)
1. Verify that Docker CE is installed correctly by running the Ubuntu image:
    ```
    docker run -it ubuntu bash
    ```
1. [Get started with Docker](https://docs.docker.com/get-started/)

## Operation with docker
1. See running container:
    ```
    docker ps
    ```
1. See all container:
    ```
    docker ps -a
    ```
1. See all images:
    ```
    docker images
    ```
1. To see what prosses is running:
    ```
    docker top <id>
    ```
1. To see info about container:
    ```
    docker hub container phusion/baseimage
    ```
1. Execute comand in container:
    ```
    docker exec -it <id> /bin/bash
    ```
1. Instruction for build images:
    ```
    docker build --network host -t '<name>':'<version>' .
    ```
1. Exit from a container without stopping it:
    ```
    CTRL +  P + Q
    ```
1. Stop a container from outside of the container:
    ```
    docker stop <container id or name>
    ```
    or
    ```
    docker kill <container id or name>
    ```
1. Restert a container:
    ```
    docker start <container id>
    ```
1. Attach to a container:
    ```
    docker attach <container id>
    ```
1. Create an image from a container:
    ```
    docker commit <container id> <image name>
    ```

1. [Purging All Unused or Dangling Images, Containers, Volumes, and Networks](https://www.digitalocean.com/community/tutorials/how-to-remove-docker-images-containers-and-volumes)
    * Docker provides a single command that will clean up any resources — images, containers, volumes, and networks — that are dangling (not associated with a container):
        ```
        docker system prune
        ```
    * To additionally remove any stopped containers and all unused images (not just dangling images), add the -a flag to the command:
        ```
        docker system prune -a
        ```


1. Other:
    ```
    docker run -d -p 5001:80
    ```
    ```
    docker run -it -p 8885:8888 <name>
    ```
    ```
    docker run -it -v ~/Downloads:/data <name> /bin/bash
    ```
    '-d' run in the background

    '-it' launch interactive mode

    Path to docker containers `/var/lib/docker/aufs/diff/`. Docker files
    ```
    sudo ls -l /var/lib/docker/aufs/diff/
    ```