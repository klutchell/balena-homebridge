# https://github.com/homebridge/homebridge/wiki/Install-Homebridge-on-Docker
# https://github.com/homebridge/docker-homebridge
# https://hub.docker.com/r/homebridge/homebridge
FROM homebridge/homebridge:2026-10-30@sha256:0518217e47c66d62a1f618a5a134e7dce50d4ebcc9de2b754ca33d2593d324a1

# hadolint ignore=DL3008
RUN apt-get update && apt-get install -y --no-install-recommends \
    bluetooth bluez libbluetooth-dev libudev-dev && \
    rm -rf /var/lib/apt/lists/*
