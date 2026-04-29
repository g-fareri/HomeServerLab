# HomeLab
Virtualized Home Lab for Networking, Server Infrastructure, and Media Services

A self-built home lab environment designed to simulate a small-scale enterprise infrastructure using virtualization, structured networking, and self-hosted services. This project focuses on hands-on experience with server deployment, network configuration, and system administration.

# Overview
This lab demonstrates a fully functional home server environment built from repurposed enterprise hardware. It includes virtualization using Proxmox, a self-hosted media server, and a structured physical network using patch panels and managed cabling.

The goal of this environment is to gain practical experience in:

*Server virtualization and management
*Network design and segmentation
*Linux system administration
*Infrastructure troubleshooting and optimization

# Hardware
Server Host: Dell OptiPlex 7050 SFF
* CPU: Intel i5-7600
* RAM: 16GB DDR4
  * Storage:
    * Samsung 970 EVO 250GB NVMe (OS / Proxmox)
    * 4TB WD Blue HDD (media storage)
* Networking Equipment
  * Netgear GS308 8-Port Gigabit Switch (unmanaged)
  * Structured patch panel and Ethernet cabling
  * Small rack-mounted setup for cable management and organization

# Software Stack
* Proxmox VE 9.1-1 (virtualization platform)
* Ubuntu Server VM (Jellyfin host)
* Jellyfin Media Server
* Tailscale (secure remote access)

#Architecture Overview
ISP Router
     ↓
Netgear GS308 Switch
     ↓
Patch Panel → Structured Ethernet Cabling
     ↓
Proxmox Host (Dell OptiPlex 7050)
     ↓
Ubuntu VM
     ↓
Jellyfin Media Server
     ↓
Remote Access via Tailscale VPN

# Configuration & Setup
## Virtualization
* Installed and configured Proxmox VE on bare metal
* Created Ubuntu Server VM for media hosting
* Allocated dedicated storage for media library
## Networking
* Built structured LAN using Ethernet cabling and patch panel termination
* Connected all devices through Netgear GS308 switch
* Assigned static IP to Proxmox host for consistent access
* Configured static IP inside Ubuntu VM for stable service hosting
## Services
* Deployed Jellyfin media server inside Ubuntu VM
* Enabled remote access using Tailscale VPN
* Verified connectivity using ping and SSH testing
# Key Features
* Full virtualization environment using Proxmox
* Self-hosted media server accessible remotely
* Structured physical network with patch panel organization
* Stable static IP configuration for host and VM
* Secure remote access via VPN (Tailscale)
  # HomeLab Setup
![image alt](https://github.com/g-fareri/HomeServerLab/blob/230c99800142a4e4b28331b95289490e5c38cfb6/homelab.png)

#Future Improvements
* Implement VLAN segmentation for network isolation
* Add monitoring tools (Grafana / Prometheus)
* Expand storage with RAID or NAS integration
* Upgrade to managed switch for advanced network control
* Add backup and redundancy strategy
