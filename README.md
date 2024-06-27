# Bazzite Nvidia System76 &nbsp; [![build-ublue](https://github.com/blue-build/template/actions/workflows/build.yml/badge.svg)](https://github.com/ZxDs3/bazzite-nvidia-system76/actions/workflows/build.yml)

A custom image of Bazzite Nvidia from uBlue that includes system76-driver, system76-power, and firmware-manager.

This image was created using [BlueBuild](https://blue-build.org/).

## Installation

To rebase an existing atomic Fedora installation to the latest build:

- First rebase to the unsigned image, to get the proper signing keys and policies installed:
  ```
  rpm-ostree rebase ostree-unverified-registry:ghcr.io/zxds3/bazzite-nvidia-system76:latest
  ```
- Reboot to complete the rebase:
  ```
  systemctl reboot
  ```
- Then rebase to the signed image, like so:
  ```
  rpm-ostree rebase ostree-image-signed:ghcr.io/zxds3/bazzite-nvidia-system76:latest
  ```
- Reboot again to complete the installation
  ```
  systemctl reboot
  ```

## ISO

There is no ISO, sorry.

## Things to Know

You might need to add yourself to the "adm" group manually. This is for the firmware-manager package.
