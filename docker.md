



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


- if you want to pull a image use  `sodu docker pull hello-docker`

- if you want to run a container `docker run ubuntu `
- turns out the video is learning linux in the last part of it



[Docker crash course tutorial](https://www.youtube.com/watch?v=31ieHmcTUOk&list=PL4cUxeGkcC9hxjeEtdHFNYMtCpjNBm3h7)
### images 
images they are like blueprints for creating containers

### containers
containers are running images ,

so i can create a image that have node 17 and create a container above it and put on the container my code and it will work separet from my pc

actually each image in docker is based on another image for example the node image is based on a linux ubuntu image ex





