###Useful Docker commands


```bash
#!/bin/bash
# Delete all containers
docker rm $(docker ps -a -q)
# Delete all images
docker rmi $(docker images -q)
# list all containers (even not running)
docker ps -a
#Remove containers created before another container
docker rm $(docker ps --before b43e3946768a -q)
#Remove containers created after a certain container
docker rm $(docker ps --since a6ca4661ec7f -q)
#Mass remove images except...
docker rmi $(docker images | grep -v 'ubuntu\|my-image' | awk {'print $3'})

#Attach to a container (Ctrl + c to detach)
docker attach -sig-proxy=false
```

###Resources

- http://techoverflow.net/blog/2013/10/22/docker-remove-all-images-and-containers
- http://stackoverflow.com/questions/17236796/how-to-remove-old-docker-containers
- http://stackoverflow.com/questions/17665283/how-does-one-remove-an-image-in-docker
