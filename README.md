# RustScan 2.4.1 .deb Package

![RustScan Logo](https://raw.githubusercontent.com/RustScan/RustScan/master/pictures/rustscan.png)

## Overview

This repository contains the Debian package (.deb) for RustScan 2.4.1 "Guaranteed Speed 🦔" - a lightning-fast port scanner written in Rust.

## About RustScan

RustScan is designed to be a faster alternative to Nmap, capable of scanning all 65,535 ports in just a few seconds. It can be used as a standalone tool or in conjunction with Nmap for more detailed scanning.

## Installation

### 1: Direct Installation

```bash
# Download the .deb package
git clone https://github.com/ibrahimsql/rustscan-deb.git
cd rustscan-deb

# Install the package
sudo dpkg -i rustscan_2.4.1-1_amd64.deb
sudo apt-get install rustscan #dependencies
```

### 2: One-liner

```bash
wget -O rustscan.deb https://github.com/ibrahimsql/rustscan-deb/raw/main/rustscan_2.4.1-1_amd64.deb && sudo dpkg -i rustscan.deb && sudo apt-get install rustscan
```

## Usage

### Basic Scanning

```bash
# Scan a single IP
rustscan -a 192.168.1.1

# Scan multiple IPs
rustscan -a 192.168.1.1,192.168.1.2

# Scan an IP range
rustscan -a 192.168.1.0/24
```

### Advanced Options

```bash
# Scan specific ports
rustscan -a 192.168.1.1 -p 80,443,8080

# Adjust scan speed (lower is faster but may cause issues)
rustscan -a 192.168.1.1 --batch-size 2500

# Pass additional arguments to Nmap
rustscan -a 192.168.1.1 -- -sC -sV -A
```

## Features

- ⚡ **Fast**: Scans all 65,535 ports in seconds
- 🔎 **Smart**: Automatically adjusts scan rates to avoid overwhelming targets
- 🔄 **Nmap Integration**: Seamlessly passes discovered ports to Nmap
- 🛠️ **Customizable**: Configure batch size, timeout, and more

## Uninstallation

```bash
sudo apt-get remove rustscan
```

## Credits

This is just a packaged version of the original [RustScan](https://github.com/RustScan/RustScan) project. All credit for the tool goes to the original developers.

## License

RustScan is licensed under the [GPL-3.0 License](https://github.com/RustScan/RustScan/blob/master/LICENSE).

---
