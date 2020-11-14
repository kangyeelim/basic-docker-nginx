# basic-docker-nginx

## To run on local:
Git clone the repository

Go into the Docker Quickstart terminal (Windows)

cd into the directory where this repository is on local 

Pull the NGINX docker image from Docker Hub
This is the official image in Docker Hub
```
 $ docker pull nginx:latest
```

Pull the python3 docker image from Docker Hub
This is the official image in Docker Hub
```
$ docker pull python:3
```

Using the Dockerfile, install flask and create new docker image with docker build
```
$ docker build -t flask:v1 .
```

Deploy containers with service name to be created first 
```
$ docker-compose up -d nginx

$ docker-machine ip
```
Using the returned IP address, curl or use the browser to go to the {IP address}:80. For example:
Go to 192.168.99.101:80

 
Since NGINX is acting as a reverse proxy, we get the response from the flask application. 
The reverse proxy provides an additional level of abstraction and control to ensure smooth network traffic flow between clients and servers.

To stop and remove use:
```
$ docker stop <Container Name>
$ docker rm <Container Name>
```

## To push the image to Docker Hub
Build image
```
$ docker build -t <YOUR_USERNAME>/flask:v1 .
```

Login
```
$ docker login
```

Push image
```
$ docker push <YOUR_USERNAME>/flask:v1
```
 


