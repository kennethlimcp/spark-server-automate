Spark-server installation automation
======

###Installation Procedures

- `sudo apt-get update`
- `sudo apt-get upgrade`
- check whether **nodejs** is installed and install if not found
- check whether **npm** is installed and install if not found (should come with nodejs installation)
- check whether **git** is installed and install if not found
- clone **spark-server** repo to the ~ directory
- `npm install spark-server` dependencies
- fire up **spark-server** for the first time to generate server public key
- kill the server
- check whether **upstart** is installed and install if not found
- Setup **spark-server** with upstart and run on boot up, restart and shutdown


###Current plan
Use a traditional **shell script** method as **Ansible** does not love Windows users


###Questions

- install **DFU-util** and flash the public keys + server IP Address?

    Involves using [Spark-cli](http://github.com/spark/spark-cli)

- extract the core private keys and upload to the core-keys directory?

    Openssl will be an installation requirement


###Resources
Most steps are based off the tutorial written here: http://kennethlimcp.gitbooks.io/spark-local-cloud-on-raspberry-pi
