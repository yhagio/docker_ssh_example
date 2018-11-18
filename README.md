# Docker, Docker-Compose, SSH

This repo is to show how to install private package using local SSH in your Docker image

```sh
cd compose

# build images using your local ssh keys
docker-compose -f docker-compose.install.yml build --build-arg KEY=\"$(cat ~/.ssh/id_rsa)\" --build-arg PUB=\"$(cat ~/.ssh/id_rsa.pub)\"

# build containers and run the app
docker-compose up
```