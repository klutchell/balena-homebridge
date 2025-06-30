# https://github.com/homebridge/homebridge/wiki/Install-Homebridge-on-Docker
# https://github.com/homebridge/docker-homebridge
# https://hub.docker.com/r/homebridge/homebridge
FROM homebridge/homebridge:beta-2025-06-27@sha256:2ff638f285befde9000f8451a8d5b14526255bf25cf97190113b9487a6740cab

# hadolint ignore=DL3008
RUN apt-get update && apt-get install -y --no-install-recommends \
    bluetooth bluez libbluetooth-dev libudev-dev && \
    rm -rf /var/lib/apt/lists/*
