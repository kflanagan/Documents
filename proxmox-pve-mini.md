# Proxmox Configuration Documentation
> Generated on Sat Sep  5 06:58:18 PM EDT 2026

## Virtual Machines

## VM ID: 107

### Status:
 `status: running`

### Configuration:
| Setting | Value |
| --- | --- |
| **agent** | enabled=1 |
| **bios** | ovmf |
| **boot** | order=scsi0 |
| **cores** | 3 |
| **cpu** | kvm64 |
| **description** | <div align='center'><br>  <a href='https://community-scripts.org' target='_blank' rel='noopener noreferrer'><br>    <img src='https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/misc/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/><br>  </a><br><br>  <h2 style='font-size: 24px; margin: 20px 0;'>Homeassistant OS VM</h2><br><br>  <p style='margin: 16px 0;'><br>    <a href='https://ko-fi.com/community_scripts' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/&#x2615;-Buy us a coffee-blue' alt='spend Coffee' /><br>    </a><br>  </p><br><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a><br>  </span><br></div> |
| **efidisk0** | local-lvm:vm-107-disk-1,efitype=4m,size=4M |
| **localtime** | 1 |
| **machine** | q35 |
| **memory** | 8192 |
| **meta** | creation-qemu=11.0.0,ctime=1781971072 |
| **name** | haos-mini |
| **net0** | virtio=02:20:3A:93:FB:5F,bridge=vmbr0 |
| **numa** | 0 |
| **onboot** | 1 |
| **ostype** | l26 |
| **scsi0** | local-lvm:vm-107-disk-0,discard=on,size=40G,ssd=1 |
| **scsihw** | virtio-scsi-pci |
| **serial0** | socket |
| **smbios1** | uuid=318c759b-642c-4f7b-91a7-b27f8dbb29b4 |
| **sockets** | 1 |
| **tablet** | 0 |
| **tags** | community-script |
| **usb0** | host=10c4:ea60 |
| **vmgenid** | e7df6ed9-2ac0-4690-89ec-74feb91ac98a |

### IP Addresses:
- Unable to retrieve IP addresses (guest agent may not be installed)

## Containers

## Container ID: 101

### Status:
`status: running`

### Configuration:
| Setting | Value |
| --- | --- |
| **arch** | amd64 |
| **cores** | 1 |
| **description** | <div align='center'><br>  <a href='https://Helper-Scripts.com' target='_blank' rel='noopener noreferrer'><br>    <img src='https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/misc/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/><br>  </a><br><br>  <h2 style='font-size: 24px; margin: 20px 0;'>Pihole LXC</h2><br><br>  <p style='margin: 16px 0;'><br>    <a href='https://ko-fi.com/community_scripts' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/&#x2615;-Buy us a coffee-blue' alt='spend Coffee' /><br>    </a><br>  </p><br><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a><br>  </span><br></div> |
| **features** | keyctl=1,nesting=1,fuse=1 |
| **hostname** | pihole |
| **memory** | 512 |
| **net0** | name=eth0,bridge=vmbr0,hwaddr=BC:24:11:75:83:EE,ip=dhcp,type=veth |
| **onboot** | 1 |
| **ostype** | debian |
| **rootfs** | local-lvm:vm-101-disk-1,size=5G |
| **startup** | order=6 |
| **swap** | 512 |
| **tags** | adblock;community-script |
| **unprivileged** | 1 |
| **lxc.cgroup2.devices.allow** | c 10:200 rwm |
| **lxc.mount.entry** | /dev/net/tun dev/net/tun none bind,create=file |

### Resources:
| Resource | Value |
| --- | --- |
| Memory | 512MB |
| Swap | 512MB |
| Disk (rootfs) | local-lvm:vm-101-disk-1 |
| Disk Size (rootfs) | size=5G |
| Disk Free percentage (rootfs) | 43.9 percent |
| Startup | order=6 |
| Privilege Mode | Unprivileged |
| Uptime |  19:02:06 up 2 days |

### IP Addresses:
- `192.168.1.248/24`

## Container ID: 102

### Status:
`status: stopped`

### Configuration:
| Setting | Value |
| --- | --- |
| **arch** | amd64 |
| **cores** | 2 |
| **description** | <div align='center'><br>  <a href='https://Helper-Scripts.com' target='_blank' rel='noopener noreferrer'><br>    <img src='https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/misc/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/><br>  </a><br><br>  <h2 style='font-size: 24px; margin: 20px 0;'>Excalidraw LXC</h2><br><br>  <p style='margin: 16px 0;'><br>    <a href='https://ko-fi.com/community_scripts' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/&#x2615;-Buy us a coffee-blue' alt='spend Coffee' /><br>    </a><br>  </p><br><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a><br>  </span><br></div> |
| **features** | nesting=1,fuse=1 |
| **hostname** | excalidraw |
| **memory** | 3072 |
| **net0** | name=eth0,bridge=vmbr0,hwaddr=BC:24:11:97:BD:11,ip=dhcp,ip6=auto,type=veth |
| **onboot** | 1 |
| **ostype** | debian |
| **rootfs** | local-lvm:vm-102-disk-0,size=10G |
| **startup** | order=5 |
| **swap** | 768 |
| **tags** | community-script;tailscale |
| **lxc.cgroup2.devices.allow** | a |
| **lxc.cap.drop** |  |
| **lxc.cgroup2.devices.allow** | c 188:* rwm |
| **lxc.cgroup2.devices.allow** | c 189:* rwm |
| **lxc.mount.entry** | /dev/serial/by-id  dev/serial/by-id  none bind,optional,create=dir |
| **lxc.mount.entry** | /dev/ttyUSB0       dev/ttyUSB0       none bind,optional,create=file |
| **lxc.mount.entry** | /dev/ttyUSB1       dev/ttyUSB1       none bind,optional,create=file |
| **lxc.mount.entry** | /dev/ttyACM0       dev/ttyACM0       none bind,optional,create=file |
| **lxc.mount.entry** | /dev/ttyACM1       dev/ttyACM1       none bind,optional,create=file |
| **lxc.cgroup2.devices.allow** | c 226:128 rwm |
| **lxc.mount.entry** | /dev/dri/renderD128 dev/dri/renderD128 none bind,optional,create=file |
| **lxc.cgroup2.devices.allow** | c 29:0 rwm |
| **lxc.mount.entry** | /dev/fb0 dev/fb0 none bind,optional,create=file |
| **lxc.mount.entry** | /dev/dri dev/dri none bind,optional,create=dir |
| **lxc.cgroup2.devices.allow** | c 10:200 rwm |
| **lxc.mount.entry** | /dev/net/tun dev/net/tun none bind,create=file |

### Resources:
| Resource | Value |
| --- | --- |
| Memory | 3072MB |
| Swap | 768MB |
| Disk (rootfs) | local-lvm:vm-102-disk-0 |
| Disk Size (rootfs) | size=10G |
| Disk Free percentage (rootfs) | 72.9 percent |
| Startup | order=5 |
| Privilege Mode | Privileged |
| Uptime |  |

### IP Addresses:
- Container not running

## Container ID: 103

### Status:
`status: running`

### Configuration:
| Setting | Value |
| --- | --- |
| **arch** | amd64 |
| **cores** | 2 |
| **description** | <div align='center'><br>  <a href='https://Helper-Scripts.com' target='_blank' rel='noopener noreferrer'><br>    <img src='https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/misc/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/><br>  </a><br><br>  <h2 style='font-size: 24px; margin: 20px 0;'>audiobookshelf LXC</h2><br><br>  <p style='margin: 16px 0;'><br>    <a href='https://ko-fi.com/community_scripts' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/&#x2615;-Buy us a coffee-blue' alt='spend Coffee' /><br>    </a><br>  </p><br><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a><br>  </span><br></div> |
| **features** | nesting=1 |
| **hostname** | audiobookshelf |
| **memory** | 2048 |
| **net0** | name=eth0,bridge=vmbr0,hwaddr=BC:24:11:4D:D9:51,ip=dhcp,ip6=auto,type=veth |
| **onboot** | 1 |
| **ostype** | debian |
| **rootfs** | local-lvm:vm-103-disk-1,size=4G |
| **startup** | order=4,up=20 |
| **swap** | 512 |
| **tags** | audiobook;community-script;podcast;tailscale |
| **lxc.cgroup2.devices.allow** | a |
| **lxc.cap.drop** |  |
| **lxc.cgroup2.devices.allow** | c 188:* rwm |
| **lxc.cgroup2.devices.allow** | c 189:* rwm |
| **lxc.mount.entry** | /dev/serial/by-id  dev/serial/by-id  none bind,optional,create=dir |
| **lxc.mount.entry** | /dev/ttyUSB0       dev/ttyUSB0       none bind,optional,create=file |
| **lxc.mount.entry** | /dev/ttyUSB1       dev/ttyUSB1       none bind,optional,create=file |
| **lxc.mount.entry** | /dev/ttyACM0       dev/ttyACM0       none bind,optional,create=file |
| **lxc.mount.entry** | /dev/ttyACM1       dev/ttyACM1       none bind,optional,create=file |
| **lxc.cgroup2.devices.allow** | c 226:128 rwm |
| **lxc.mount.entry** | /dev/dri/renderD128 dev/dri/renderD128 none bind,optional,create=file |
| **lxc.cgroup2.devices.allow** | c 29:0 rwm |
| **lxc.mount.entry** | /dev/fb0 dev/fb0 none bind,optional,create=file |
| **lxc.mount.entry** | /dev/dri dev/dri none bind,optional,create=dir |
| **lxc.cgroup2.devices.allow** | c 10:200 rwm |
| **lxc.mount.entry** | /dev/net/tun dev/net/tun none bind,create=file |

### Resources:
| Resource | Value |
| --- | --- |
| Memory | 2048MB |
| Swap | 512MB |
| Disk (rootfs) | local-lvm:vm-103-disk-1 |
| Disk Size (rootfs) | size=4G |
| Disk Free percentage (rootfs) | 51.3 percent |
| Startup | order=4,up=20 |
| Privilege Mode | Privileged |
| Uptime |  19:07:29 up 2 days |

### IP Addresses:
- `192.168.1.180/24`

## Container ID: 104

### Status:
`status: running`

### Configuration:
| Setting | Value |
| --- | --- |
| **arch** | amd64 |
| **cores** | 4 |
| **description** | <div align='center'><br>  <a href='https://Helper-Scripts.com' target='_blank' rel='noopener noreferrer'><br>    <img src='https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/misc/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/><br>  </a><br><br>  <h2 style='font-size: 24px; margin: 20px 0;'>Jellyfin LXC</h2><br><br>  <p style='margin: 16px 0;'><br>    <a href='https://ko-fi.com/community_scripts' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/&#x2615;-Buy us a coffee-blue' alt='spend Coffee' /><br>    </a><br>  </p><br><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a><br>  </span><br></div> |
| **features** | nesting=1,fuse=1 |
| **hostname** | jellyfin |
| **memory** | 2048 |
| **net0** | name=eth0,bridge=vmbr0,hwaddr=BC:24:11:30:2D:33,ip=dhcp,ip6=auto,type=veth |
| **onboot** | 1 |
| **ostype** | ubuntu |
| **rootfs** | local-lvm:vm-104-disk-0,size=8G |
| **startup** | order=3,up=30 |
| **swap** | 512 |
| **tags** | community-script;media;tailscale |
| **lxc.cgroup2.devices.allow** | a |
| **lxc.cap.drop** |  |
| **lxc.cgroup2.devices.allow** | c 188:* rwm |
| **lxc.cgroup2.devices.allow** | c 189:* rwm |
| **lxc.mount.entry** | /dev/serial/by-id  dev/serial/by-id  none bind,optional,create=dir |
| **lxc.mount.entry** | /dev/ttyUSB0       dev/ttyUSB0       none bind,optional,create=file |
| **lxc.mount.entry** | /dev/ttyUSB1       dev/ttyUSB1       none bind,optional,create=file |
| **lxc.mount.entry** | /dev/ttyACM0       dev/ttyACM0       none bind,optional,create=file |
| **lxc.mount.entry** | /dev/ttyACM1       dev/ttyACM1       none bind,optional,create=file |
| **lxc.cgroup2.devices.allow** | c 226:128 rwm |
| **lxc.mount.entry** | /dev/dri/renderD128 dev/dri/renderD128 none bind,optional,create=file |
| **lxc.cgroup2.devices.allow** | c 29:0 rwm |
| **lxc.mount.entry** | /dev/fb0 dev/fb0 none bind,optional,create=file |
| **lxc.mount.entry** | /dev/dri dev/dri none bind,optional,create=dir |
| **lxc.cgroup2.devices.allow** | c 10:200 rwm |
| **lxc.mount.entry** | /dev/net/tun dev/net/tun none bind,create=file |

### Resources:
| Resource | Value |
| --- | --- |
| Memory | 2048MB |
| Swap | 512MB |
| Disk (rootfs) | local-lvm:vm-104-disk-0 |
| Disk Size (rootfs) | size=8G |
| Disk Free percentage (rootfs) | 44.5 percent |
| Startup | order=3,up=30 |
| Privilege Mode | Privileged |
| Uptime |  19:10:15 up 2 days |

### IP Addresses:
- `192.168.1.203/24`
- `100.69.151.40/32`

## Container ID: 106

### Status:
`status: stopped`

### Configuration:
| Setting | Value |
| --- | --- |
| **arch** | amd64 |
| **cores** | 2 |
| **description** | <div align='center'><br>  <a href='https://Helper-Scripts.com' target='_blank' rel='noopener noreferrer'><br>    <img src='https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/misc/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/><br>  </a><br><br>  <h2 style='font-size: 24px; margin: 20px 0;'>Stirling-PDF LXC</h2><br><br>  <p style='margin: 16px 0;'><br>    <a href='https://ko-fi.com/community_scripts' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/&#x2615;-Buy us a coffee-blue' alt='spend Coffee' /><br>    </a><br>  </p><br><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a><br>  </span><br></div> |
| **features** | nesting=1 |
| **hostname** | stirling-pdf |
| **memory** | 2048 |
| **net0** | name=eth0,bridge=vmbr0,hwaddr=BC:24:11:4D:0E:09,ip=dhcp,ip6=auto,type=veth |
| **onboot** | 1 |
| **ostype** | debian |
| **rootfs** | local-lvm:vm-106-disk-0,size=8G |
| **swap** | 512 |
| **tags** | community-script;pdf-editor;tailscale |
| **lxc.cgroup2.devices.allow** | a |
| **lxc.cap.drop** |  |
| **lxc.cgroup2.devices.allow** | c 188:* rwm |
| **lxc.cgroup2.devices.allow** | c 189:* rwm |
| **lxc.mount.entry** | /dev/serial/by-id  dev/serial/by-id  none bind,optional,create=dir |
| **lxc.mount.entry** | /dev/ttyUSB0       dev/ttyUSB0       none bind,optional,create=file |
| **lxc.mount.entry** | /dev/ttyUSB1       dev/ttyUSB1       none bind,optional,create=file |
| **lxc.mount.entry** | /dev/ttyACM0       dev/ttyACM0       none bind,optional,create=file |
| **lxc.mount.entry** | /dev/ttyACM1       dev/ttyACM1       none bind,optional,create=file |
| **lxc.cgroup2.devices.allow** | c 226:128 rwm |
| **lxc.mount.entry** | /dev/dri/renderD128 dev/dri/renderD128 none bind,optional,create=file |
| **lxc.cgroup2.devices.allow** | c 29:0 rwm |
| **lxc.mount.entry** | /dev/fb0 dev/fb0 none bind,optional,create=file |
| **lxc.mount.entry** | /dev/dri dev/dri none bind,optional,create=dir |
| **lxc.cgroup2.devices.allow** | c 10:200 rwm |
| **lxc.mount.entry** | /dev/net/tun dev/net/tun none bind,create=file |

### Resources:
| Resource | Value |
| --- | --- |
| Memory | 2048MB |
| Swap | 512MB |
| Disk (rootfs) | local-lvm:vm-106-disk-0 |
| Disk Size (rootfs) | size=8G |
| Disk Free percentage (rootfs) | 80.8 percent |
| Startup |  |
| Privilege Mode | Privileged |
| Uptime |  |

### IP Addresses:
- Container not running

## Container ID: 109

### Status:
`status: stopped`

### Configuration:
| Setting | Value |
| --- | --- |
| **arch** | amd64 |
| **cores** | 2 |
| **description** | <div align='center'><br>  <a href='https://community-scripts.org' target='_blank' rel='noopener noreferrer'><br>    <img src='https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/misc/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/><br>  </a><br><br>  <h2 style='font-size: 24px; margin: 20px 0;'>qBittorrent LXC</h2><br><br>  <p style='margin: 16px 0;'><br>    <a href='https://community-scripts.org/donate' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/%E2%9D%A4%EF%B8%8F-Sponsoring%20%26%20Donations-FF5E5B' alt='Sponsoring and donations' /><br>    </a><br>  </p><br><br>  <p style='margin: 12px 0;'><br>    <a href='https://community-scripts.org/scripts/qbittorrent' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/%F0%9F%93%A6-Open%20Script%20Page-00617f' alt='Open script page' /><br>    </a><br>  </p><br><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a><br>  </span><br></div> |
| **features** | nesting=1,keyctl=1 |
| **hostname** | qbittorrent |
| **memory** | 2048 |
| **net0** | name=eth0,bridge=vmbr0,hwaddr=BC:24:11:20:01:5D,ip=dhcp,type=veth |
| **onboot** | 1 |
| **ostype** | debian |
| **rootfs** | local-lvm:vm-109-disk-0,size=8G |
| **swap** | 512 |
| **tags** | community-script;torrent |
| **timezone** | America/New_York |
| **unprivileged** | 1 |

### Resources:
| Resource | Value |
| --- | --- |
| Memory | 2048MB |
| Swap | 512MB |
| Disk (rootfs) | local-lvm:vm-109-disk-0 |
| Disk Size (rootfs) | size=8G |
| Disk Free percentage (rootfs) | 10.2 percent |
| Startup |  |
| Privilege Mode | Unprivileged |
| Uptime |  |

### IP Addresses:
- Container not running

## Container ID: 111

### Status:
`status: stopped`

### Configuration:
| Setting | Value |
| --- | --- |
| **arch** | amd64 |
| **cores** | 1 |
| **description** | <div align='center'><br>  <a href='https://community-scripts.org' target='_blank' rel='noopener noreferrer'><br>    <img src='https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/misc/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/><br>  </a><br><br>  <h2 style='font-size: 24px; margin: 20px 0;'>ESPConnect LXC</h2><br><br>  <p style='margin: 16px 0;'><br>    <a href='https://community-scripts.org/donate' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/%E2%9D%A4%EF%B8%8F-Sponsoring%20%26%20Donations-FF5E5B' alt='Sponsoring and donations' /><br>    </a><br>  </p><br><br>  <p style='margin: 12px 0;'><br>    <a href='https://community-scripts.org/scripts/espconnect' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/%F0%9F%93%A6-Open%20Script%20Page-00617f' alt='Open script page' /><br>    </a><br>  </p><br><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a><br>  </span><br></div> |
| **features** | nesting=1,keyctl=1 |
| **hostname** | espconnect |
| **memory** | 512 |
| **net0** | name=eth0,bridge=vmbr0,hwaddr=BC:24:11:1C:33:7B,ip=dhcp,type=veth |
| **onboot** | 1 |
| **ostype** | debian |
| **rootfs** | local-lvm:vm-111-disk-0,size=4G |
| **swap** | 512 |
| **tags** | community-script;esp32;flash;iot |
| **timezone** | America/New_York |
| **unprivileged** | 1 |

### Resources:
| Resource | Value |
| --- | --- |
| Memory | 512MB |
| Swap | 512MB |
| Disk (rootfs) | local-lvm:vm-111-disk-0 |
| Disk Size (rootfs) | size=4G |
| Disk Free percentage (rootfs) | 19.7 percent |
| Startup |  |
| Privilege Mode | Unprivileged |
| Uptime |  |

### IP Addresses:
- Container not running

## Container ID: 112

### Status:
`status: running`

### Configuration:
| Setting | Value |
| --- | --- |
| **arch** | amd64 |
| **cores** | 1 |
| **description** | <div align='center'><br>  <a href='https://community-scripts.org' target='_blank' rel='noopener noreferrer'><br>    <img src='https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/misc/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/><br>  </a><br><br>  <h2 style='font-size: 24px; margin: 20px 0;'>MeTube LXC</h2><br><br>  <p style='margin: 16px 0;'><br>    <a href='https://community-scripts.org/donate' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/%E2%9D%A4%EF%B8%8F-Sponsoring%20%26%20Donations-FF5E5B' alt='Sponsoring and donations' /><br>    </a><br>  </p><br><br>  <p style='margin: 12px 0;'><br>    <a href='https://community-scripts.org/scripts/metube' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/%F0%9F%93%A6-Open%20Script%20Page-00617f' alt='Open script page' /><br>    </a><br>  </p><br><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a><br>  </span><br></div> |
| **features** | nesting=1,keyctl=1 |
| **hostname** | metube |
| **memory** | 2048 |
| **mp0** | /data/plex,mp=/media/downloads |
| **net0** | name=eth0,bridge=vmbr0,hwaddr=BC:24:11:C7:AA:72,ip=dhcp,type=veth |
| **onboot** | 1 |
| **ostype** | debian |
| **rootfs** | local-lvm:vm-112-disk-0,size=10G |
| **swap** | 512 |
| **tags** | community-script;media;youtube |
| **timezone** | America/New_York |
| **unprivileged** | 1 |

### Resources:
| Resource | Value |
| --- | --- |
| Memory | 2048MB |
| Swap | 512MB |
| Disk (rootfs) | local-lvm:vm-112-disk-0 |
| Disk Size (rootfs) | size=10G |
| Disk Free percentage (rootfs) | 32.7 percent |
| Startup |  |
| Privilege Mode | Unprivileged |
| Uptime |  19:20:24 up 2 days |

### IP Addresses:
- `192.168.1.247/24`

## Host Disk Space Summary

| Filesystem | Size | Used | Available | Use | Mounted on |
| --- | ---: | ---: | ---: | ---: | --- |
| udev | 6.8G | 0 | 6.8G | 0% | /dev |
| tmpfs | 1.6G | 3.1M | 1.6G | 1% | /run |
| /dev/mapper/pve-root | 94G | 33G | 58G | 36% | / |
| tmpfs | 7.8G | 66M | 7.7G | 1% | /dev/shm |
| efivarfs | 192K | 101K | 87K | 54% | /sys/firmware/efi/efivars |
| tmpfs | 5.0M | 0 | 5.0M | 0% | /run/lock |
| tmpfs | 1.0M | 0 | 1.0M | 0% | /run/credentials/systemd-journald.service |
| tmpfs | 7.8G | 0 | 7.8G | 0% | /tmp |
| /dev/sda2 | 1022M | 9.1M | 1013M | 1% | /boot/efi |
| data | 900G | 502G | 398G | 56% | /data |
| /dev/fuse | 128M | 56K | 128M | 1% | /etc/pve |
| tmpfs | 1.0M | 0 | 1.0M | 0% | /run/credentials/getty@tty1.service |
| tmpfs | 1.6G | 4.0K | 1.6G | 1% | /run/user/0 |

