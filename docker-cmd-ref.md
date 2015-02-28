###Useful Docker commands


```bash
#!/bin/bash
# Delete all containers
docker rm $(docker ps -a -q)
# Delete all images
docker rmi $(docker images -q)
# list all containers (even not running)
docker ps -a
```

###Resources

- http://techoverflow.net/blog/2013/10/22/docker-remove-all-images-and-containers/
