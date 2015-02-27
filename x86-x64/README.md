Spark-server Dockerfile
======

The image can be found at [Docker Hub](): [spark-server](https://registry.hub.docker.com/u/kennethlimcp/spark-server)

###How to use this?

1.) Install [Docker](https://docs.docker.com/installation)
2.) Use `docker pull kennethlimcp/spark-server:0.0.1`
3.) `docker run kennethlimcp/spark-server -d -p 8080:8080 -p 5683:5683`
4.) `curl $(boot2docker ip):8080` will show:

```
{
  "code": 400,
  "error": "invalid_request",
  "error_description": "The access token was not found"
}
```

5.) or simply run the command `boot2docker ip` and copy the ip address. Head over to the browser and run `IP_ADDRESS:8080`

There's no way to proceed futher though verifications have been made that shows the core connecting to the server successfully. Current Docker implementation does not allow the copying of files to the container so we have to manage the files seperately from the container itself.



###Current issues to be resolved
- Install on a data container or external volume mount to persist server public key
- Reload `main.js` whenever a new core key is placed in the `core-keys` directory


###Resources
- http://docker.com
- http://viget.com/extend/how-to-use-docker-on-os-x-the-missing-guide
- http://build-podcast.com/docker
