# https://github.com/homebridge/homebridge/wiki/Install-Homebridge-on-Docker
# https://github.com/homebridge/docker-homebridge
# https://hub.docker.com/r/homebridge/homebridge
# https://github.com/homebridge/docker-homebridge/blob/latest/Dockerfile
FROM homebridge/homebridge:2025-06-10@sha256:bf911d5b043c80ea120674a1e870814d66d3dd24f0f4fb1013ffbaab3567eb7f

# hadolint ignore=DL3008
RUN apt-get update && apt-get install -y --no-install-recommends \
    bluetooth bluez libbluetooth-dev libudev-dev && \
    rm -rf /var/lib/apt/lists/*
