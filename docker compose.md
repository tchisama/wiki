



trick to remove all images from the docker registry
```
      // Remove all containers
      docker container rm -f $(docker container ls -a -q)
      // -f flag is used to force the removal of the containers
      // $(docker container ls -a -q) returns a list of all container IDs


      // Remove all images
      docker image rm $(docker image ls -q)
      // $(docker images ls -q) returns a list of all image IDs
  
```






#step 1 install docker compose 

first you need to have docker compose installed on your system . you can follow the instalation instructions provided in the dockerdocumenttaion for you specific operation system .4





# create docker compose file 

Next you'll need to create a docker-compose.yml file in you project directory . this file will contain the configuration for all the services in your application.


heres a basic example of what a docker-compose.yml file might look like:

```yml
version: '3'
services:
  web:
    image: nginx:latest
    ports:
      - "8080:80"
  db:
    image: mysql:5.7
    environment:
      MYSQL_ROOT_PASSWORD: example
```


# Run your docker compose application ,


once you have your docker-compose.yml file ready you can  use the **docker-compose up** command to start your application



# stop your docker compose application
to stop your docker compose applictaion and remove the co=ntainers you can use the **docker compose down** 
this command will stop all the runnnign containers and remove them, along with any networds and volumes create by 'dockers-compose up'




