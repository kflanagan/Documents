# Building a homelab

In a homelab you can have a starter place where you can learn some things, and if you re-purpose it later, it makes a good media center or home automaiton computer, or even a light web surfing machine mabe for the kids in the family room

## Hardware
A PC with enough storage for everything you want, VMs, data, containers.  That's not really that much storage space needed for most of us.

### The least expensive [$139](https://www.amazon.com/dp/B0F13Q2SLL?th=1)
I would expect to run one VM, and a couple of containers at once. 
- N150 
- 16GB RAM  
- 256GB onboard storage 


### Mid-range cost [$327](https://www.amazon.com/GMKtec-ryzen-mini-pc-computers/dp/B0CD7Y4C5Y?th=1)
You can easily run multiple VMs and several containers at once.
- Ryzen 7
- 32GB RAM
- 1TB onboard storage
- Room for another SSD to add 1 or even 2 TB more storage


### Platform
[Proxmox Virtual Environment](https://www.proxmox.com/en/products/proxmox-virtual-environment/overview) ,a free hypervisor and containers platform. There is good documentation, that will help you with the installation. 

There is a rich community, someone started creating [Helper Scripts](https://community-scripts.github.io/ProxmoxVE/scripts) These will make it really easy to install many different VMs or containers.

### Guests
- Full VM development environment
  - Fedora Linux
  
  You get a full GUI and the ability to install all kinds of development tools, for free.

- Containers
  - [Plex](https://www.plex.tv/), A media server, not fully free or open source, but has features like remote access
  - Alternatively, an open source media server [Jellyfin](https://community-scripts.github.io/ProxmoxVE/scripts?id=jellyfin)
  - [Piehole](https://community-scripts.github.io/ProxmoxVE/scripts?id=pihole) a network level (whole home) ad blocker
  - [MySQL](https://community-scripts.github.io/ProxmoxVE/scripts?id=mysql) A very full featured database
  - [Grafana](https://community-scripts.github.io/ProxmoxVE/scripts?id=grafana) Data visualization


