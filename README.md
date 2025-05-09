# Sonobus Docker AoO server

Docker image for Sonobus AoO connection server, also published in [**GHCR**](https://ghcr.io/simomatte/sonobus-docker-aooserver) and [**Docker Hub**](https://hub.docker.com/r/simomatte/sonobus-docker-aooserver)

---

Repo based on both

**essej/aooserver** github repo [[https://github.com/essej/aooserver](https://github.com/essej/aooserver)] **for base Sonobus aooserver files**

and

**topjor/sonobus-aooserver** github repo [[https://github.com/topjor/sonobus-aooserver](https://github.com/topjor/sonobus-aooserver)] **for Dockerfile**

---

This repository will simply automate Docker container builds with Github actions and publish on _ghcr.io_ and _Docker Hub_.

The aooserver files to be compiled are automatically fetched from essej/aooserver repo when building images.

Using **debian:stable** for the builder container and **debian:stable-slim** images for the service container.

The **amd64** and **arm64** builds can be fetched using:
* **GHCR**
```
docker pull ghcr.io/simomatte/sonobus-docker-aooserver:latest
```
* **Docker Hub**
```
docker pull simomatte/sonobus-docker-aooserver:latest
```

---

# USAGE WITH DOCKER

Using the container image:

* **GHCR**
```
docker run -p 10998:10998/udp -p 10998:10998 ghcr.io/simomatte/sonobus-docker-aooserver:latest
```

* **Docker Hub**
```
docker run -p 10998:10998/udp -p 10998:10998 simomatte/sonobus-docker-aooserver:latest
```

How to run with flags: 

* **GHCR**
```
docker run -p PORT:PORT/udp -p PORT:PORT ghcr.io/simomatte/sonobus-docker-aooserver:latest aooserver [flags]
```

* **Docker Hub**
```
docker run -p PORT:PORT/udp -p PORT:PORT simomatte/sonobus-docker-aooserver:latest aooserver [flags]
```

A docker-compose.yml file is included in the repository for usage with docker compose. The docker-compose.yml file will use the image published on GHCR, if you want to use the image from Docker Hub, simply remove the _ghcr.io/_ prefix from **image** line.
