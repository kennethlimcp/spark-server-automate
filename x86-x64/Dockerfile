#Docker image to setup Spark-server
FROM ubuntu:14.04

MAINTAINER Kenneth Lim<kennethlimcp@gmail.com>

RUN     apt-get update && apt-get install -y \
        git \
        nodejs \
        npm

#symlink nodejs to node
RUN ln -s /usr/bin/nodejs /usr/bin/node

RUN git clone http://github.com/spark/spark-server.git spark-server
WORKDIR  /spark-server/js
RUN sudo npm install

WORKDIR /spark-server/js

EXPOSE 8080

CMD ["node","./main.js"]
