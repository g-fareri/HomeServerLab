# HomeServerLab
Home lab project documenting server virtualization, networking, and infrastructure setup

## Hardware
- Dell Optiplex 7050 sff: CPU i5-7600, RAM 16gb ddr4, SSD Samsung 970 EVO 250gb M.2, HHD 4TB WD Blue internal
- 8-port Netgear GS308 switch
- Patch panel & cabling
- Server rack

## Software
- Proxmox VE 9.1-1
- Virtual Machines
  - Jellyfin Media Server (Ubuntu VM)

## Network Diagram
ISP Router
    |
Netgear GS308
    |
Patch Panel
    |
Proxmox Host
    |- Jellyfin VM (remote access using Tailscale)

## Network Configuration
- Configured LAN using Netgear GS308 unmanaged switch
- Assigned static IP to Proxmox host
- Configured static IP inside Ubuntu VM
- Verified connectivity via ping and SSH
- Organized rack-mounted patch panel for cable management

![image alt](https://github.com/g-fareri/HomeServerLab/blob/230c99800142a4e4b28331b95289490e5c38cfb6/homelab.png)
