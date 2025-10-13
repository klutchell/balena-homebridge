# https://github.com/homebridge/homebridge/wiki/Install-Homebridge-on-Docker
# https://github.com/homebridge/docker-homebridge
# https://hub.docker.com/r/homebridge/homebridge

# renovate: datasource=docker depName=homebridge/homebridge
ARG HOMEBRIDGE_DOCKER_VERSION=beta-2025-06-27

FROM homebridge/homebridge:${HOMEBRIDGE_DOCKER_VERSION}

# hadolint ignore=DL3008
RUN apt-get update && apt-get install -y --no-install-recommends \
    bluetooth bluez libbluetooth-dev libudev-dev && \
    rm -rf /var/lib/apt/lists/*
