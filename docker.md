



2024-03-29 15:01

## *learning sources*

[[docker commands]]
[[Dockerfile]]

[Docker Tutorial for beginners](https://www.youtube.com/watch?v=pTFZFxd4hOI)

- ok first you need to install docker from the docker website
- then create a new project a simple app.js says helo world
- then create a file with the `Dockerfile` name without any extension
the file should look like something like this
```dockerfile
FROM node:alpine
COPY . /app
CMD node /app/app.js
```
- then you type `sodu docker build -t hello-docker .` in the terminal
- then you can log all image by running `sodu docker image ls`
- then you can run the image by running `sodu docker run hello-docker`

- this line i'm just teaching zobair

- if you want to pull a image use  `sodu docker pull hello-docker`

- if you want to run a container `docker run ubuntu `
- turns out the video is learning linux in the last part of it



- how to push an image to docker hub
- use this command `sodu docker push hello-docker`



[Docker crash course tutorial](https://www.youtube.com/watch?v=31ieHmcTUOk&list=PL4cUxeGkcC9hxjeEtdHFNYMtCpjNBm3h7)
### images 
images they are like blueprints for creating containers

### containers
containers are running images ,

so i can create a image that have node 17 and create a container above it and put on the container my code and it will work separet from my pc

actually each image in docker is based on another image for example the node image is based on a linux ubuntu image ex


## *.dockerignore*
```dockerignore
node_modules
```
- you can ignore any type of files to not push them to the container

## *starting and stopping containers*

```bash
sodu docker run --name imagename  myapp

sodu docker stop container_name
```
### ports
- you can open ports in the container

- you can list to see all the images by running `sodu docker images` or `sodu docker image ls`


- to show all the containers running `sodu docker ps`

- how to publish a port 

`bash 
sudo docker run --name myapp -p 4000:4000 -d image <--- this is the image name
                       ^        ^    ^     ^ 
                       |        |    |     |
                       |        |    |     this to fre the terminal
                       |        |    the port we want to link to
                       |        container port
                       container name
`


| Command                                    | Description                               |
| ------------------------------------------ | ----------------------------------------- |
| docker build -t image_name .               | Build an image from a Dockerfile          |
| docker run image_name                      | Run a container from a specific image     |
| docker pull image_name                     | Pull an image from a registry             |
| docker ps                                  | Show running containers                   |
| docker ps -a                               | Show all containers, even if not running  |
| docker stop container_name                 | Stop a running container                  |
| docker start container_name                | Start a stopped container                 |
| docker image ls                            | List all images                           |
| docker container ls                        | List all containers                       |
| docker build -t image_name .               | Build an image from a Dockerfile          |



- show all the container even the not running `sodu docker ps -a`
- now you can start from them any container you want `sodu docker start container_name`


## *layer caching*

- each line in the dockerfile is a layer that added to the image
- you can build a container by using the `sudo docker build -t imagename .<-- location of the Dockerfile command `
- waht if you changed your code, would you make a new image ? that will build the whole container again
- 
- [[learn more about docker caching]]

## *Managing images and containers*

- you can remove images `sodu docker image rm imagename`
- you can remove containers `sodu docker container rm container_name`
- you can list images `sodu docker image ls`
- you can list containers `sodu docker container ls`

warning
- you can't remove images that a container is running on it
- you can't remove containers that are running
