# go app
## Description

This is a sample `Go` application which connects to Redis. The app increments a `counter` on an incoming request.

## Prerequisites:
1. Docker should be installed and running.
2. `docker-compose` should be installed and is accessible for all users.
3. Dockerhub account/private registry to push the docker image. (Kindly upfate image name in docker-compose.yaml)

## Steps to run:
1. Build the docker image by using `docker build -t <image name> .`.
2. Once the image is built it can be pushed to registry by using `docker push <image name>`.
3. Run the docker image by using `docker run -d -p 8000:80 <image name>` or `docker-compose up -d`.