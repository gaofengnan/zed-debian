![GitHub Downloads (all assets, all releases)](https://img.shields.io/github/downloads/gaofengnan/zed-debian/total)
![GitHub Downloads (all assets, latest release)](https://img.shields.io/github/downloads/gaofengnan/zed-debian/latest/total)
![GitHub Release](https://img.shields.io/github/v/release/gaofengnan/zed-debian)
![GitHub Release Date](https://img.shields.io/github/release-date/gaofengnan/zed-debian?display_date=published_at)

<h1>
   <p align="center">
     <a href="https://zed.dev/"><img src="https://github.com/gaofengnan/zed-debian/blob/main/zed-logo.png" alt="zed Logo" width="128" style="margin-right: 20px"></a>
     <a href="https://www.debian.org/"><img src="https://github.com/gaofengnan/zed-debian/blob/main/debian-logo.png" alt="Debian Logo" width="104" style="margin-left: 20px"></a>
     <br>zed for Debian
   </p>
</h1>
<p align="center">
 A high-performance, multiplayer code editor from the creators of Atom and Tree-sitter.
</p>

# zed for Debian

> Fork of [dariogriffo/zed-debian](https://github.com/dariogriffo/zed-debian) (MIT); the original packaging is by Dario Griffo. Served at [deb.gaofn.xyz](https://deb.gaofn.xyz) for Debian 12 (bookworm) and 13 (trixie).

This repository contains build scripts to produce the _unofficial_ Debian packages
(.deb) for [zed](https://github.com/zed-industries/zed/) hosted at [deb.gaofn.xyz](https://deb.gaofn.xyz)

Currently supported Debian distros are:
- Bookworm
- Trixie
- Forky
- Sid

Supported architectures:
- amd64 (x86_64) - All distributions
- arm64 (aarch64) - All distributions

This is an unofficial community project to provide a package that's easy to
install on Debian. If you're looking for the zed source code, see
[zed](https://github.com/zed-industries/zed/).

## Install/Update

### The Debian way

```sh
sudo install -d -m 0755 /etc/apt/keyrings
sudo curl -fsSL https://deb.gaofn.xyz/deb.gaofn.xyz.gpg -o /etc/apt/keyrings/deb.gaofn.xyz.gpg
sudo curl -fsSL https://deb.gaofn.xyz/deb.gaofn.xyz.sources -o /etc/apt/sources.list.d/deb.gaofn.xyz.sources
# Debian 12 (bookworm): fetch deb.gaofn.xyz-bookworm.sources instead
sudo apt update
sudo apt install -y zed
```

### Manual Installation

1. Download the .deb package for your Debian version available on
   the [Releases](https://github.com/gaofengnan/zed-debian/releases) page.
2. Install the downloaded .deb package.

```sh
sudo dpkg -i <filename>.deb
```
## Updating

To update to a new version, just follow any of the installation methods above. There's no need to uninstall the old version; it will be updated correctly.

## Building

### Build for single architecture
```sh
./build.sh <zed_version> <build_version> <architecture>
# Example: ./build.sh 0.8.11 1 arm64
```

### Build for all architectures
```sh
./build.sh <zed_version> <build_version> all
# Example: ./build.sh 0.8.11 1 all
```

## Roadmap

- [x] Produce a .deb package on GitHub Releases
- [x] Set up a debian mirror for easier updates
- [x] Multi-architecture support (amd64, arm64, armel, armhf, ppc64el, s390x)

## Disclaimer

- This repo is not open for issues related to zed. This repo is only for _unofficial_ Debian packaging.
