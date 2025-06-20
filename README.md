# balena-homebridge

[![balena-homebridge](https://img.shields.io/badge/balena-homebridge-blue.svg)](https://github.com/klutchell/balena-homebridge)

Run [Homebridge](https://homebridge.io/) on any balena device.

## About

This project provides a simple way to run
[Homebridge](https://github.com/homebridge/homebridge) on a balena device. It
uses the official Homebridge Docker image and persists data using a named
volume.

From the official documentation:

> Homebridge allows you to integrate with smart home devices that do not
> otherwise support HomeKit. There are over 2,000 Homebridge plugins supporting
> thousands of different smart accessories.

## Deployment

### Deploy with balena

You can deploy this project to a new or existing balena fleet in one click:

[![Deploy with balena](https://balena.io/deploy.svg)](https://dashboard.balena-cloud.com/deploy?repoUrl=https://github.com/klutchell/balena-homebridge)

### Manual Deployment

1. Sign up for or login to [balenaCloud](https://dashboard.balena-cloud.com).
2. Create a new fleet, select a device type, and download the OS.
3. Provision your device with the downloaded OS.
4. Clone this repository to your local workstation.
5. Using [balenaCLI](https://www.balena.io/docs/reference/cli/), push the code
    to your fleet: `balena push <FLEET_NAME>`.

## Configuration

Homebridge is configured using a `config.json` file located in the `/homebridge`
directory inside the container. This directory is mounted as a named volume
(`homebridge`) to persist your configuration.

To configure Homebridge:

1. Once the container is running, access the Homebridge UI. By default, it is
    available on port `8581` of your device's IP address (e.g.,
    `http://<DEVICE_IP>:8581`). The `docker-compose.yml` uses
    `network_mode: host`, so Homebridge will be accessible on your device's IP
    address.
2. The default username is `admin` and the default password is `admin`. You
    should change this on first login.
3. Use the UI to install plugins and configure your smart home devices.

After configuring Homebridge and adding your devices, you can add Homebridge to
the Home app on your Apple device by scanning the QR code shown in the
Homebridge UI.

## Contributing

Please open an issue or submit a pull request with any features or fixes.
