## Insrall Docker:
1. [Docker Community Edition (CE)](https://www.docker.com/community-edition)
2. [Get Docker CE for Ubuntu](https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/)
3. [Post-installation steps for Linux](https://docs.docker.com/engine/installation/linux/linux-postinstall/)
4. Verify that Docker CE is installed correctly by running the Ubuntu image:
    ```
    docker run -it ubuntu /bin/bash
    ```

## Operation with docker
See running container:
```
docker ps
```
See all container:
```
docker ps -a
```
See all images:
```
docker images
```
To see what prosses is running:
```
docker top <id>
```
To see info about container:
```
docker hub container phusion/baseimage
```
Execute comand in container:
```
docker exec -it <id> /bin/bash
```
Instruction for build images:
```
docker build -t '<name>':'<version>' .
```
Other:
```
docker run -d -p 5001:80
```
```
docker run -it -p 8885:8888 tensorflow_cv2_lpm
```
```
docker run -it -v ~/Downloads:/data tf:0.2 /bin/bash
```
```
docker stop $(docker ps -a -q) && docker rm $(docker ps -a -q)
```
```
docker rmi $(docker images)
```
'-d'  запустить в фоне

'-it' запустить интерактивную консоль

Path to docker containers `/var/lib/docker/aufs/diff/`. Docker files
```
sudo ls -l /var/lib/docker/aufs/diff/
```