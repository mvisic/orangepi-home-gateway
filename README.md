# orangepi-home-gateway

Modular home network gateway built on Armbian and Orange Pi, delivering DNS filtering, firewall management, and scalable edge services.

## Overview

This project transforms an **Orange Pi Zero 3** into a reliable, always-on **Home Network Gateway** that provides:

- **DNS Filtering** (using AdGuard Home)  
- **Network Security Services**  
- **Infrastructure services expandable in future phases**  

This guide documents the *first phase* of the build — setup of the OS and AdGuard Home for network-wide DNS filtering.

## Phase 1 – System Setup (Completed)

### 1. Flash Armbian Server Image (Completed)

1. Download and flash the [latest Armbian **Server / CLI** image for Orange Pi Zero 3](https://www.armbian.com/orange-pi-zero-3/).  
2. Use balenaEtcher or ApplePi Baker on macOS to write the `.img.xz` to the microSD card.
3. Insert the card and power on the board with Ethernet connected.

### 2. Initial Login & Configuration (Completed)

1. Find the IP address of the Orange Pi on your router’s device list.
2. SSH into the board with:
   ```bash
   ssh root@<your-orangepi-ip-address>
3. Change the root password when prompted
4. Set up normal user account


### 3. Secure the System (Completed)

1. Upate and install curl:
 ```bash
   sudo apt install curl wget git htop vim tmux ufw -y

2. Configure basic firewall rules:
 ```bash
   sudo apt install ufw -y
sudo ufw allow OpenSSH
sudo ufw enable
 

