# Sonobus Docker AoO server

Repo based on both
essej/aooserver github repo [https://github.com/essej/sonobus] *for base aooserver files to be compiled*

and

topjor/sonobus-aooserver github repo [https://github.com/topjor/sonobus-aooserver] *for Dockerfile*

---

This repository will simply automate Docker container builds with Github actions and publish them on _ghcr.io_.

The aooserver files are automatically fetched from essej/sonobus repo when building.

Dockerfile are using *debian:stable* and *debian:stable-slim* images.

The amd64 and arm64 builds can be fetched using:
```
docker pull ghcr.io/simomatte/sonobus-docker-aooserver:latest
```
