# Unbound Container

[![Docker Pulls](https://img.shields.io/docker/pulls/linuxcontainers/unbound.svg)](https://hub.docker.com/r/linuxcontainers/unbound/)
[![Docker Stars](https://img.shields.io/docker/stars/linuxcontainers/unbound.svg)](https://hub.docker.com/r/linuxcontainers/unbound/)
[![Docker Build](https://img.shields.io/docker/cloud/automated/linuxcontainers/unbound.svg)](https://hub.docker.com/r/linuxcontainers/unbound/)
[![Docker Build Status](https://img.shields.io/docker/cloud/build/linuxcontainers/unbound.svg)](https://hub.docker.com/r/linuxcontainers/unbound/)

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
