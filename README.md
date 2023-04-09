# Unbound Container

![Docker Pulls (tag)](https://hub.docker.com/r/linuxcontainers/unbound/?logo=docker&style=for-the-badge)
![Docker Stars (tag)](https://hub.docker.com/r/linuxcontainers/unbound/?logo=docker&style=for-the-badge)
![Docker Build (tag)](https://hub.docker.com/r/linuxcontainers/unbound/?logo=docker&style=for-the-badge)
![Docker Build Status (tag)](https://hub.docker.com/r/linuxcontainers/unbound/?logo=docker&style=for-the-badge)
![Docker Image Size (tag)](https://img.shields.io/docker/image-size/linuxcontainers/unbound/latest?logo=docker&style=for-the-badge)

[UNBOUND](https://nlnetlabs.nl/projects/unbound/about/) server running on [Alpine Linux](https://hub.docker.com/_/alpine/).

## Quickstart

```yml
unbound:
  image: linuxcontainers/unbound

  volumes:
    # You must provide a config file
    - ./uncound.conf:/etc/unbound/named.conf

    # Zone files
    - ./zones:/etc/unbound/local-zones.conf

  ports:
    - "53:53/udp"
