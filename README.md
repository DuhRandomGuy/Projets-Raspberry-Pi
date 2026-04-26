# Raspberry Pi 5 NAS et Home Server

This repository documents the complete configuration of my personal NAS based on a **Raspberry Pi 5**. The goal is to centralize file storage, manage local backups, and host essential network services (such as ad-blocking) via Docker.

## Key Features
* **Centralized Storage:** Managed via OpenMediaVault (OMV).
* **Containerization:** Services deployed using Docker and Portainer.
* **Secure Remote Access:** VPN connectivity via Tailscale.
* **Network Security:** DNS-level ad and tracker blocking with AdGuard Home.

## Hardware
* **Device:** Raspberry Pi 5 with an active cooling case.
* **OS Storage:** 32GB MicroSD Card.
* **Data Storage:** 1TB External HDD.
* **Networking:** Connected to the local Ethernet network via a Gigabit switch.

## Network Configuration & Services

The infrastructure relies on a clear separation between the host and containerized services:

| Service | Technology | Description |
| :--- | :--- | :--- |
| **OpenMediaVault** | Debian-based | Disk management, SMB/NFS shares, and monitoring. |
| **Tailscale** | Wireguard | Mesh VPN to access the NAS remotely without opening ports. |
| **AdGuard Home** | DNS | Network-wide ad and tracker filtering. |
| **Portainer** | Docker | Graphical interface for container management. |

For specific services like **AdGuard Home**, I use a **MacVLAN** network to assign them a dedicated IP address on my local network. This prevents port conflicts with the OMV web interface and allows for better network management.

## Installation

### 1. OS Preparation
Installed Raspberry Pi OS Lite (64-bit) using Raspberry Pi Imager on the SD card. 
> **Note:** The username and password set during this step are used for initial SSH access.

### 2. Connexion au Raspberry Pi
Once the Pi is connected to the network, I accessed it via SSH from my computer (Windows PowerShell). To connect, use the following command:
```bash
ssh username@ip
```

### 3. OMV installation
Now connected, use the following command to begin installing Open Media Vault on the Pi
```bash
wget -O - [https://github.com/OpenMediaVault-Plugin-Developers/installScript/raw/master/install](https://github.com/OpenMediaVault-Plugin-Developers/installScript/raw/master/install) | sudo bash
```
