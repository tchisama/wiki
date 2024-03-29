
**1. docker run**  
Runs a command in a new container.
Example: `docker run -d -p 8080:80 nginx` (Runs an nginx web server in the background, mapping port 8080 on the host to port 80 on the container)

**2. docker build**  
Builds an image from a Dockerfile.
Example: `docker build -t myimage .` (Builds an image named "myimage" from the Dockerfile in the current directory)

**3. docker images**  
Lists all images available locally.
Example: `docker images` (Lists all images available on your local machine)

**4. docker ps**  
Lists all running containers.
Example: `docker ps` (Lists all running containers along with their details)

**5. docker stop**  
Stops one or more running containers.
Example: `docker stop container_id` (Stops the container with the specified container ID)

**6. docker start**  
Starts one or more stopped containers.
Example: `docker start container_id` (Starts the container with the specified container ID)

**7. docker restart**  
Restarts one or more containers.
Example: `docker restart container_id` (Restarts the container with the specified container ID)

**8. docker rm**  
Removes one or more containers.
Example: `docker rm container_id` (Removes the container with the specified container ID)

**9. docker rmi**  
Removes one or more images.
Example: `docker rmi image_id` (Removes the image with the specified image ID)

**10. docker pull**  
Pulls an image or a repository from a registry.
Example: `docker pull ubuntu:latest` (Pulls the latest version of the Ubuntu image from Docker Hub)

**11. docker push**  
Pushes an image or a repository to a registry.
Example: `docker push myusername/myimage` (Pushes the image named "myimage" to a Docker registry under the username "myusername")

**12. docker exec**  
Executes a command in a running container.
Example: `docker exec -it container_id bash` (Executes a bash shell in the running container with the specified container ID)

**13. docker network ls**  
Lists all networks.
Example: `docker network ls` (Lists all Docker networks on your system)

**14. docker volume ls**  
Lists all volumes.
Example: `docker volume ls` (Lists all Docker volumes on your system)

**15. docker-compose up**  
Builds, (re)creates, starts, and attaches to containers for a service.
Example: `docker-compose up -d` (Starts services defined in the `docker-compose.yml` file in detached mode)

**16. docker-compose down**  
Stops and removes containers, networks, volumes, and images created by `up`.
Example: `docker-compose down` (Stops and removes containers, networks, and volumes created by `up`)

**17. docker-compose exec**  
Executes a command in a running container.
Example: `docker-compose exec service_name command` (Executes a command in a running service container)

**18. docker-compose build**  
Builds or rebuilds services.
Example: `docker-compose build` (Builds or rebuilds services defined in the `docker-compose.yml` file)

**19. docker-compose logs**  
Displays log output from services.
Example: `docker-compose logs service_name` (Displays logs for a specific service)

**20. docker-compose stop**  
Stops services.
Example: `docker-compose stop` (Stops services defined in the `docker-compose.yml` file)

**21. docker-compose start**  
Starts services.
Example: `docker-compose start` (Starts services defined in the `docker-compose.yml` file)

**22. docker-compose restart**  
Restarts services.
Example: `docker-compose restart` (Restarts services defined in the `docker-compose.yml` file)

These examples illustrate how each Docker command is used in practical scenarios.
