



2024-03-29 15:01

## learning sources

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

-  if you want to run a container `docker run ubuntu `
- turns out the video is learning linux in the last part of it



[Docker crash course tutorial](https://www.youtube.com/watch?v=31ieHmcTUOk&list=PL4cUxeGkcC9hxjeEtdHFNYMtCpjNBm3h7)
