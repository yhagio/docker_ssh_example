### Docker Compose files

* `docker-compose.install.yml` is for installing private package and build image
* `docker-compose.yml` is for building the container and starting the app


Some Docker commands
```sh
# build images
docker-compose -f docker-compose.install.yml build --build-arg KEY=\"$(cat ~/.ssh/id_rsa)\" --build-arg PUB=\"$(cat ~/.ssh/id_rsa.pub)\"

# build containers and run the app
docker-compose up

# Stop all
docker stop $(docker ps -a -q)
# Delete all containers
docker rm $(docker ps -a -q)
# Delete all images
docker rmi $(docker images -q)
```
