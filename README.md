# Atavism server built with Docker Compose

This is a basic Atavism Docker environment built using Docker Compose. It consists following:

* OpenJDK8
* MySQL 5.7
* phpMyAdmin

## Installation

Clone this repository on your local computer. Run the `docker-compose up -d`.

```shell
git clone https://github.com/sprintcube/docker-compose-lamp.git
cd docker-compose-lamp/
git fetch --all
git checkout 7.1.x
docker-compose up -d
```

Extract your server files to the 'atavism_server' folder.
Change the following:

* database hostname to 'mysql:3306'
* database password to 'tiger'
 in auth.properties and world.properties.


Follow below instructions for phpmyadmin access to upload your database contents.

#### Connect via SSH

You can connect to web server using `docker exec` command to perform various operation on it. Use below command to login to container via ssh.

```shell
docker exec -it atavism-2019.1.2 /bin/bash
```

Once connected you can run your server by connecting via SSH and running:

```shell
cd /root/bin
./auth.sh -vC start
./world.sh -vC start
```

Docker should auto start these but my docker skills have not worked that out yet.


To shut down run docker-compose down

## phpMyAdmin

phpMyAdmin is configured to run on port 8080. Use following default credentials.

http://localhost:8080/  
username: root  
password: tiger

## Connecting to your server

Connecting is the same as if you were running the server on your machine. so `localhost` for the
host name in the Unity Editor.


