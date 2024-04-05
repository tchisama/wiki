



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




