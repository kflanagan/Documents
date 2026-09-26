# Proxmox Configuration Documentation
> Generated on Sat Sep 26 04:13:08 PM EDT 2026

## Virtual Machines

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
| Disk Free percentage (rootfs) | 44.0 percent |
| Startup | order=6 |
| Privilege Mode | Unprivileged |
| Uptime |  16:13:28 up 6 days |

### IP Addresses:
- `192.168.1.248/24`

## Container ID: 102

### Status:
`status: running`

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
| **rootfs** | local-lvm:vm-102-disk-1,size=10G |
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
| Disk (rootfs) | local-lvm:vm-102-disk-1 |
| Disk Size (rootfs) | size=10G |
| Disk Free percentage (rootfs) | 73.3 percent |
| Startup | order=5 |
| Privilege Mode | Privileged |
| Uptime |  16:13:47 up 6 days |

### IP Addresses:
- `192.168.1.74/24`

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
| **mp0** | /data,mp=/data |
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
| Disk Free percentage (rootfs) | 51.5 percent |
| Startup | order=4,up=20 |
| Privilege Mode | Privileged |
| Uptime |  16:14:06 up 6 days |

### IP Addresses:
- `192.168.1.180/24`
- `100.67.39.60/32`

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
| **mp0** | /data,mp=/data |
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
| Disk Free percentage (rootfs) | 46.2 percent |
| Startup | order=3,up=30 |
| Privilege Mode | Privileged |
| Uptime |  16:14:25 up 6 days |

### IP Addresses:
- `192.168.1.203/24`
- `100.69.151.40/32`

## Container ID: 106

### Status:
`status: running`

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
| Disk Free percentage (rootfs) | 82.8 percent |
| Startup |  |
| Privilege Mode | Privileged |
| Uptime |  16:14:44 up 6 days |

### IP Addresses:
- `192.168.1.186/24`
- `100.80.57.104/32`

## Container ID: 109

### Status:
`status: running`

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
| Uptime |  16:15:02 up 6 days |

### IP Addresses:
- `192.168.1.45/24`

## Container ID: 111

### Status:
`status: running`

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
| Uptime |  16:15:21 up 6 days |

### IP Addresses:
- `192.168.1.34/24`

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
| **mp0** | /data,mp=/data |
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
| Disk Free percentage (rootfs) | 32.8 percent |
| Startup |  |
| Privilege Mode | Unprivileged |
| Uptime |  16:15:40 up 19:19 |

### IP Addresses:
- `192.168.1.247/24`

## Container ID: 113

### Status:
`status: running`

### Configuration:
| Setting | Value |
| --- | --- |
| **arch** | amd64 |
| **cores** | 3 |
| **description** | <br><div align='center'><br>  <a href='https://community-scripts.org' target='_blank' rel='noopener noreferrer'><br>    <img src='https://raw.githubusercontent.com/community-scripts/core/main/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/><br>  </a><br><br>  <h2 style='font-size: 24px; margin: 20px 0;'>Fedora LXC</h2><br><br>  <p style='margin: 16px 0;'><br>    <a href='https://community-scripts.org/donate' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/%E2%9D%A4%EF%B8%8F-Sponsoring%20%26%20Donations-FF5E5B' alt='Sponsoring and donations' /><br>    </a><br>  </p><br><br>  <p style='margin: 12px 0;'><br>    <a href='https://community-scripts.org/scripts/fedora' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/%F0%9F%93%A6-Open%20Script%20Page-00617f' alt='Open script page' /><br>    </a><br>  </p><br><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a><br>  </span><br></div> |
| **features** | nesting=1,keyctl=1,fuse=1,mount=nfs |
| **hostname** | ansible |
| **memory** | 1024 |
| **mp0** | /data,mp=/data |
| **net0** | name=eth0,bridge=vmbr0,hwaddr=BC:24:11:88:5C:65,ip=dhcp,ip6=auto,type=veth |
| **onboot** | 1 |
| **ostype** | fedora |
| **rootfs** | local-lvm:vm-113-disk-0,size=8G |
| **swap** | 512 |
| **tags** | community-script;os |
| **timezone** | America/New_York |
| **unprivileged** | 1 |

### Resources:
| Resource | Value |
| --- | --- |
| Memory | 1024MB |
| Swap | 512MB |
| Disk (rootfs) | local-lvm:vm-113-disk-0 |
| Disk Size (rootfs) | size=8G |
| Disk Free percentage (rootfs) | 15.9 percent |
| Startup |  |
| Privilege Mode | Unprivileged |
| Uptime |  16:15:59 up 6 days |

### IP Addresses:
- `192.168.1.91/24`

## Container ID: 114

### Status:
`status: running`

### Configuration:
| Setting | Value |
| --- | --- |
| **arch** | amd64 |
| **cores** | 2 |
| **description** | <br><div align='center'><br>  <a href='https://community-scripts.org' target='_blank' rel='noopener noreferrer'><br>    <img src='https://raw.githubusercontent.com/community-scripts/core/main/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/><br>  </a><br><br>  <h2 style='font-size: 24px; margin: 20px 0;'>Semaphore LXC</h2><br><br>  <p style='margin: 16px 0;'><br>    <a href='https://community-scripts.org/donate' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/%E2%9D%A4%EF%B8%8F-Sponsoring%20%26%20Donations-FF5E5B' alt='Sponsoring and donations' /><br>    </a><br>  </p><br><br>  <p style='margin: 12px 0;'><br>    <a href='https://community-scripts.org/scripts/semaphore' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/%F0%9F%93%A6-Open%20Script%20Page-00617f' alt='Open script page' /><br>    </a><br>  </p><br><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a><br>  </span><br></div> |
| **features** | nesting=1,keyctl=1 |
| **hostname** | semaphore |
| **memory** | 2048 |
| **net0** | name=eth0,bridge=vmbr0,hwaddr=BC:24:11:B7:FF:82,ip=dhcp,type=veth |
| **onboot** | 1 |
| **ostype** | ubuntu |
| **rootfs** | local-lvm:vm-114-disk-0,size=4G |
| **swap** | 512 |
| **tags** | community-script;dev_ops |
| **timezone** | America/New_York |
| **unprivileged** | 1 |

### Resources:
| Resource | Value |
| --- | --- |
| Memory | 2048MB |
| Swap | 512MB |
| Disk (rootfs) | local-lvm:vm-114-disk-0 |
| Disk Size (rootfs) | size=4G |
| Disk Free percentage (rootfs) | 44.9 percent |
| Startup |  |
| Privilege Mode | Unprivileged |
| Uptime |  16:16:18 up 6 days |

### IP Addresses:
- `192.168.1.12/24`

## Container ID: 115

### Status:
`status: running`

### Configuration:
| Setting | Value |
| --- | --- |
| **arch** | amd64 |
| **cores** | 2 |
| **description** | <br><div align='center'><br>  <a href='https://community-scripts.org' target='_blank' rel='noopener noreferrer'><br>    <img src='https://raw.githubusercontent.com/community-scripts/core/main/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/><br>  </a><br><br>  <h2 style='font-size: 24px; margin: 20px 0;'>n8n LXC</h2><br><br>  <p style='margin: 16px 0;'><br>    <a href='https://community-scripts.org/donate' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/%E2%9D%A4%EF%B8%8F-Sponsoring%20%26%20Donations-FF5E5B' alt='Sponsoring and donations' /><br>    </a><br>  </p><br><br>  <p style='margin: 12px 0;'><br>    <a href='https://community-scripts.org/scripts/n8n' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/%F0%9F%93%A6-Open%20Script%20Page-00617f' alt='Open script page' /><br>    </a><br>  </p><br><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a><br>  </span><br></div> |
| **features** | nesting=1,keyctl=1 |
| **hostname** | n8n |
| **memory** | 2048 |
| **net0** | name=eth0,bridge=vmbr0,hwaddr=BC:24:11:D3:52:13,ip=dhcp,type=veth |
| **onboot** | 1 |
| **ostype** | debian |
| **rootfs** | local-lvm:vm-115-disk-0,size=10G |
| **swap** | 512 |
| **tags** | automation;community-script |
| **timezone** | America/New_York |
| **unprivileged** | 1 |

### Resources:
| Resource | Value |
| --- | --- |
| Memory | 2048MB |
| Swap | 512MB |
| Disk (rootfs) | local-lvm:vm-115-disk-0 |
| Disk Size (rootfs) | size=10G |
| Disk Free percentage (rootfs) | 57.3 percent |
| Startup |  |
| Privilege Mode | Unprivileged |
| Uptime |  16:16:36 up 6 days |

### IP Addresses:
- `192.168.1.163/24`

## Container ID: 116

### Status:
`status: running`

### Configuration:
| Setting | Value |
| --- | --- |
| **arch** | amd64 |
| **cores** | 2 |
| **description** | <br><div align='center'><br>  <a href='https://community-scripts.org' target='_blank' rel='noopener noreferrer'><br>    <img src='https://raw.githubusercontent.com/community-scripts/core/main/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/><br>  </a><br><br>  <h2 style='font-size: 24px; margin: 20px 0;'>ConvertX LXC</h2><br><br>  <p style='margin: 16px 0;'><br>    <a href='https://community-scripts.org/donate' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/%E2%9D%A4%EF%B8%8F-Sponsoring%20%26%20Donations-FF5E5B' alt='Sponsoring and donations' /><br>    </a><br>  </p><br><br>  <p style='margin: 12px 0;'><br>    <a href='https://community-scripts.org/scripts/convertx' target='_blank' rel='noopener noreferrer'><br>      <img src='https://img.shields.io/badge/%F0%9F%93%A6-Open%20Script%20Page-00617f' alt='Open script page' /><br>    </a><br>  </p><br><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a><br>  </span><br>  <span style='margin: 0 10px;'><br>    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i><br>    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a><br>  </span><br></div> |
| **features** | nesting=1,keyctl=1 |
| **hostname** | convertx |
| **memory** | 4096 |
| **net0** | name=eth0,bridge=vmbr0,hwaddr=BC:24:11:10:FB:5C,ip=dhcp,type=veth |
| **onboot** | 1 |
| **ostype** | debian |
| **rootfs** | local-lvm:vm-116-disk-0,size=20G |
| **swap** | 512 |
| **tags** | community-script;converter |
| **timezone** | America/New_York |
| **unprivileged** | 1 |

### Resources:
| Resource | Value |
| --- | --- |
| Memory | 4096MB |
| Swap | 512MB |
| Disk (rootfs) | local-lvm:vm-116-disk-0 |
| Disk Size (rootfs) | size=20G |
| Disk Free percentage (rootfs) | 29.5 percent |
| Startup |  |
| Privilege Mode | Unprivileged |
| Uptime |  16:16:55 up 6 days |

### IP Addresses:
- `192.168.1.18/24`

## Host Disk Space Summary

| Filesystem | Size | Used | Available | Use | Mounted on |
| --- | ---: | ---: | ---: | ---: | --- |
| udev | 14G | 0 | 14G | 0% | /dev |
| tmpfs | 3.1G | 3.0M | 3.1G | 1% | /run |
| /dev/mapper/pve-root | 65G | 8.3G | 53G | 14% | / |
| tmpfs | 16G | 68M | 16G | 1% | /dev/shm |
| efivarfs | 128K | 52K | 72K | 42% | /sys/firmware/efi/efivars |
| tmpfs | 5.0M | 0 | 5.0M | 0% | /run/lock |
| tmpfs | 1.0M | 0 | 1.0M | 0% | /run/credentials/systemd-journald.service |
| tmpfs | 16G | 404K | 16G | 1% | /tmp |
| /dev/sdb2 | 1022M | 9.1M | 1013M | 1% | /boot/efi |
| data | 1.9T | 503G | 1.4T | 28% | /data |
| /dev/fuse | 128M | 68K | 128M | 1% | /etc/pve |
| tmpfs | 1.0M | 0 | 1.0M | 0% | /run/credentials/getty@tty1.service |
| tmpfs | 3.1G | 4.0K | 3.1G | 1% | /run/user/0 |

