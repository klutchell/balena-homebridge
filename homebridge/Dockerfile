# https://github.com/homebridge/homebridge/wiki/Install-Homebridge-on-Docker
# https://github.com/homebridge/docker-homebridge
# https://hub.docker.com/r/homebridge/homebridge
FROM homebridge/homebridge:2025-12-28@sha256:083ee619cac419fe2d234dec057cdc162e76c4d0c10ecedc3d451b56c36042a6

# hadolint ignore=DL3008
RUN apt-get update && apt-get install -y --no-install-recommends \
    bluetooth bluez libbluetooth-dev libudev-dev && \
    rm -rf /var/lib/apt/lists/*
