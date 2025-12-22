# https://github.com/homebridge/homebridge/wiki/Install-Homebridge-on-Docker
# https://github.com/homebridge/docker-homebridge
# https://hub.docker.com/r/homebridge/homebridge
FROM homebridge/homebridge:2025-12-16@sha256:ac49b1ae860468c2fa3cba6a7e543beb1ab93bf0f6eb620bfb736895a9430018

# hadolint ignore=DL3008
RUN apt-get update && apt-get install -y --no-install-recommends \
    bluetooth bluez libbluetooth-dev libudev-dev && \
    rm -rf /var/lib/apt/lists/*
