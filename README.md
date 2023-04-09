# Unbound Container

[![Docker Automated build](https://img.shields.io/docker/automated/linuxcontainers/alpine.svg?style=for-the-badge&logo=docker)](https://hub.docker.com/r/linuxcontainers/unbound/)
[![Docker Pulls](https://img.shields.io/docker/pulls/linuxcontainers/alpine.svg?style=for-the-badge&logo=docker)](https://hub.docker.com/r/linuxcontainers/unbound/)
[![Docker Image Size (latest by date)](https://img.shields.io/docker/image-size/linuxcontainers/unbound?logo=docker&style=for-the-badge)](https://hub.docker.com/r/linuxcontainers/unbound)

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
