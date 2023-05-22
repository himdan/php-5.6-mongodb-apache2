#Legacy PHP5.6 Apache2 MongoDB PHP PROJECT
Docker environment for a **Legacy php5.6** application.
## Prerequisites

Make sure you have installed all of the following prerequisites on your development machine: <br>
Check the official Docker documentation for information how to install Docker on your operating system. And then install Docker and supporting tools.

* Docker - [Official Website] - <a href="https://docs.docker.com/engine/install/">docker</a> <br>
* Docker Compose - [Official Website] - <a href="https://docs.docker.com/compose/install/">docker-compose</a> <br>

#Installation
to create php56_legacy_full docker image 
```bash
docker build -t php56_legacy_full docker/php/
```
to serve the application
```bash
docker-compose up -d 
```
## Check Applications
**Check that those URLS works properly :** <br>
> http://127.0.0.1:8080<br>