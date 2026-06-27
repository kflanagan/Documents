# Proxmox Configuration Documentation
Generated on Sat Jun 27 08:31:30 AM EDT 2026

## Virtual Machines

## VM ID: 107

### Configuration:
- **agent**: enabled=1
- **bios**: ovmf
- **boot**: order=scsi0
- **cores**: 2
- **description**: <div align='center'>
  <a href='https://community-scripts.org' target='_blank' rel='noopener noreferrer'>
    <img src='https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/misc/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/>
  </a>

  <h2 style='font-size: 24px; margin: 20px 0;'>Homeassistant OS VM</h2>

  <p style='margin: 16px 0;'>
    <a href='https://ko-fi.com/community_scripts' target='_blank' rel='noopener noreferrer'>
      <img src='https://img.shields.io/badge/&#x2615;-Buy us a coffee-blue' alt='spend Coffee' />
    </a>
  </p>

  <span style='margin: 0 10px;'>
    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a>
  </span>
  <span style='margin: 0 10px;'>
    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a>
  </span>
  <span style='margin: 0 10px;'>
    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a>
  </span>
</div>
- **efidisk0**: local-lvm:vm-107-disk-1,efitype=4m,size=4M
- **localtime**: 1
- **machine**: q35
- **memory**: 8192
- **meta**: creation-qemu=11.0.0,ctime=1781971072
- **name**: haos-mini
- **net0**: virtio=02:20:3A:93:FB:5F,bridge=vmbr0
- **onboot**: 1
- **ostype**: l26
- **scsi0**: local-lvm:vm-107-disk-0,discard=on,size=40G,ssd=1
- **scsihw**: virtio-scsi-pci
- **serial0**: socket
- **smbios1**: uuid=318c759b-642c-4f7b-91a7-b27f8dbb29b4
- **tablet**: 0
- **tags**: community-script
- **vmgenid**: e7df6ed9-2ac0-4690-89ec-74feb91ac98a

### Status:
status: running

### IP Addresses:
- Unable to retrieve IP addresses (guest agent may not be installed)

## Containers

## Container ID: 101

### Configuration:
- **arch**: amd64
- **cores**: 1
- **description**: <div align='center'>
  <a href='https://Helper-Scripts.com' target='_blank' rel='noopener noreferrer'>
    <img src='https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/misc/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/>
  </a>

  <h2 style='font-size: 24px; margin: 20px 0;'>Pihole LXC</h2>

  <p style='margin: 16px 0;'>
    <a href='https://ko-fi.com/community_scripts' target='_blank' rel='noopener noreferrer'>
      <img src='https://img.shields.io/badge/&#x2615;-Buy us a coffee-blue' alt='spend Coffee' />
    </a>
  </p>

  <span style='margin: 0 10px;'>
    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a>
  </span>
  <span style='margin: 0 10px;'>
    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a>
  </span>
  <span style='margin: 0 10px;'>
    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a>
  </span>
</div>
- **features**: keyctl=1,nesting=1,fuse=1
- **hostname**: pihole
- **memory**: 512
- **net0**: name=eth0,bridge=vmbr0,hwaddr=BC:24:11:75:83:EE,ip=dhcp,type=veth
- **onboot**: 1
- **ostype**: debian
- **rootfs**: local-lvm:vm-101-disk-0,size=5G
- **startup**: order=6
- **swap**: 512
- **tags**: adblock;community-script
- **unprivileged**: 1
- **lxc.cgroup2.devices.allow**: c 10:200 rwm
- **lxc.mount.entry**: /dev/net/tun dev/net/tun none bind,create=file

### Resources:
- **Memory**: 512MB
- **Swap**: 512MB
- **Disk (rootfs)**: local-lvm:vm-101-disk-0
- **Disk Size (rootfs)**: size=5G
- **Disk Free percentage (rootfs)**: 40.1 percent
- **Startup**: order=6
- **Privilege Mode**: Unprivileged
- **Uptime**:  08:31:42 up 3 days

### Status:
status: running

### IP Addresses:
- 192.168.1.248/24

## Container ID: 102

### Configuration:
- **arch**: amd64
- **cores**: 2
- **description**: <div align='center'>
  <a href='https://Helper-Scripts.com' target='_blank' rel='noopener noreferrer'>
    <img src='https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/misc/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/>
  </a>

  <h2 style='font-size: 24px; margin: 20px 0;'>Excalidraw LXC</h2>

  <p style='margin: 16px 0;'>
    <a href='https://ko-fi.com/community_scripts' target='_blank' rel='noopener noreferrer'>
      <img src='https://img.shields.io/badge/&#x2615;-Buy us a coffee-blue' alt='spend Coffee' />
    </a>
  </p>

  <span style='margin: 0 10px;'>
    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a>
  </span>
  <span style='margin: 0 10px;'>
    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a>
  </span>
  <span style='margin: 0 10px;'>
    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a>
  </span>
</div>
- **features**: nesting=1,fuse=1
- **hostname**: excalidraw
- **memory**: 3072
- **net0**: name=eth0,bridge=vmbr0,hwaddr=BC:24:11:97:BD:11,ip=dhcp,ip6=auto,type=veth
- **onboot**: 1
- **ostype**: debian
- **rootfs**: local-lvm:vm-102-disk-1,size=10G
- **startup**: order=5
- **swap**: 768
- **tags**: community-script;tailscale
- **lxc.cgroup2.devices.allow**: a
- **lxc.cap.drop**: 
- **lxc.cgroup2.devices.allow**: c 188:* rwm
- **lxc.cgroup2.devices.allow**: c 189:* rwm
- **lxc.mount.entry**: /dev/serial/by-id  dev/serial/by-id  none bind,optional,create=dir
- **lxc.mount.entry**: /dev/ttyUSB0       dev/ttyUSB0       none bind,optional,create=file
- **lxc.mount.entry**: /dev/ttyUSB1       dev/ttyUSB1       none bind,optional,create=file
- **lxc.mount.entry**: /dev/ttyACM0       dev/ttyACM0       none bind,optional,create=file
- **lxc.mount.entry**: /dev/ttyACM1       dev/ttyACM1       none bind,optional,create=file
- **lxc.cgroup2.devices.allow**: c 226:128 rwm
- **lxc.mount.entry**: /dev/dri/renderD128 dev/dri/renderD128 none bind,optional,create=file
- **lxc.cgroup2.devices.allow**: c 29:0 rwm
- **lxc.mount.entry**: /dev/fb0 dev/fb0 none bind,optional,create=file
- **lxc.mount.entry**: /dev/dri dev/dri none bind,optional,create=dir
- **lxc.cgroup2.devices.allow**: c 10:200 rwm
- **lxc.mount.entry**: /dev/net/tun dev/net/tun none bind,create=file

### Resources:
- **Memory**: 3072MB
- **Swap**: 768MB
- **Disk (rootfs)**: local-lvm:vm-102-disk-1
- **Disk Size (rootfs)**: size=10G
- **Disk Free percentage (rootfs)**: 65.8 percent
- **Startup**: order=5
- **Privilege Mode**: Privileged
- **Uptime**:  08:31:51 up 3 days

### Status:
status: running

### IP Addresses:
- 192.168.1.154/24

## Container ID: 103

### Configuration:
- **arch**: amd64
- **cores**: 2
- **description**: <div align='center'>
  <a href='https://Helper-Scripts.com' target='_blank' rel='noopener noreferrer'>
    <img src='https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/misc/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/>
  </a>

  <h2 style='font-size: 24px; margin: 20px 0;'>audiobookshelf LXC</h2>

  <p style='margin: 16px 0;'>
    <a href='https://ko-fi.com/community_scripts' target='_blank' rel='noopener noreferrer'>
      <img src='https://img.shields.io/badge/&#x2615;-Buy us a coffee-blue' alt='spend Coffee' />
    </a>
  </p>

  <span style='margin: 0 10px;'>
    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a>
  </span>
  <span style='margin: 0 10px;'>
    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a>
  </span>
  <span style='margin: 0 10px;'>
    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a>
  </span>
</div>
- **features**: nesting=1
- **hostname**: audiobookshelf
- **memory**: 2048
- **net0**: name=eth0,bridge=vmbr0,hwaddr=BC:24:11:4D:D9:51,ip=dhcp,ip6=auto,type=veth
- **onboot**: 1
- **ostype**: debian
- **rootfs**: local-lvm:vm-103-disk-0,size=4G
- **startup**: order=4,up=20
- **swap**: 512
- **tags**: audiobook;community-script;podcast;tailscale
- **lxc.cgroup2.devices.allow**: a
- **lxc.cap.drop**: 
- **lxc.cgroup2.devices.allow**: c 188:* rwm
- **lxc.cgroup2.devices.allow**: c 189:* rwm
- **lxc.mount.entry**: /dev/serial/by-id  dev/serial/by-id  none bind,optional,create=dir
- **lxc.mount.entry**: /dev/ttyUSB0       dev/ttyUSB0       none bind,optional,create=file
- **lxc.mount.entry**: /dev/ttyUSB1       dev/ttyUSB1       none bind,optional,create=file
- **lxc.mount.entry**: /dev/ttyACM0       dev/ttyACM0       none bind,optional,create=file
- **lxc.mount.entry**: /dev/ttyACM1       dev/ttyACM1       none bind,optional,create=file
- **lxc.cgroup2.devices.allow**: c 226:128 rwm
- **lxc.mount.entry**: /dev/dri/renderD128 dev/dri/renderD128 none bind,optional,create=file
- **lxc.cgroup2.devices.allow**: c 29:0 rwm
- **lxc.mount.entry**: /dev/fb0 dev/fb0 none bind,optional,create=file
- **lxc.mount.entry**: /dev/dri dev/dri none bind,optional,create=dir
- **lxc.cgroup2.devices.allow**: c 10:200 rwm
- **lxc.mount.entry**: /dev/net/tun dev/net/tun none bind,create=file

### Resources:
- **Memory**: 2048MB
- **Swap**: 512MB
- **Disk (rootfs)**: local-lvm:vm-103-disk-0
- **Disk Size (rootfs)**: size=4G
- **Disk Free percentage (rootfs)**: 46.3 percent
- **Startup**: order=4,up=20
- **Privilege Mode**: Privileged
- **Uptime**:  08:32:00 up 3 days

### Status:
status: running

### IP Addresses:
- 192.168.1.180/24

## Container ID: 104

### Configuration:
- **arch**: amd64
- **cores**: 4
- **description**: <div align='center'>
  <a href='https://Helper-Scripts.com' target='_blank' rel='noopener noreferrer'>
    <img src='https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/misc/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/>
  </a>

  <h2 style='font-size: 24px; margin: 20px 0;'>Jellyfin LXC</h2>

  <p style='margin: 16px 0;'>
    <a href='https://ko-fi.com/community_scripts' target='_blank' rel='noopener noreferrer'>
      <img src='https://img.shields.io/badge/&#x2615;-Buy us a coffee-blue' alt='spend Coffee' />
    </a>
  </p>

  <span style='margin: 0 10px;'>
    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a>
  </span>
  <span style='margin: 0 10px;'>
    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a>
  </span>
  <span style='margin: 0 10px;'>
    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a>
  </span>
</div>
- **features**: nesting=1,fuse=1
- **hostname**: jellyfin
- **memory**: 2048
- **net0**: name=eth0,bridge=vmbr0,hwaddr=BC:24:11:30:2D:33,ip=dhcp,ip6=auto,type=veth
- **onboot**: 1
- **ostype**: ubuntu
- **rootfs**: local-lvm:vm-104-disk-0,size=8G
- **startup**: order=3,up=30
- **swap**: 512
- **tags**: community-script;media;tailscale
- **lxc.cgroup2.devices.allow**: a
- **lxc.cap.drop**: 
- **lxc.cgroup2.devices.allow**: c 188:* rwm
- **lxc.cgroup2.devices.allow**: c 189:* rwm
- **lxc.mount.entry**: /dev/serial/by-id  dev/serial/by-id  none bind,optional,create=dir
- **lxc.mount.entry**: /dev/ttyUSB0       dev/ttyUSB0       none bind,optional,create=file
- **lxc.mount.entry**: /dev/ttyUSB1       dev/ttyUSB1       none bind,optional,create=file
- **lxc.mount.entry**: /dev/ttyACM0       dev/ttyACM0       none bind,optional,create=file
- **lxc.mount.entry**: /dev/ttyACM1       dev/ttyACM1       none bind,optional,create=file
- **lxc.cgroup2.devices.allow**: c 226:128 rwm
- **lxc.mount.entry**: /dev/dri/renderD128 dev/dri/renderD128 none bind,optional,create=file
- **lxc.cgroup2.devices.allow**: c 29:0 rwm
- **lxc.mount.entry**: /dev/fb0 dev/fb0 none bind,optional,create=file
- **lxc.mount.entry**: /dev/dri dev/dri none bind,optional,create=dir
- **lxc.cgroup2.devices.allow**: c 10:200 rwm
- **lxc.mount.entry**: /dev/net/tun dev/net/tun none bind,create=file

### Resources:
- **Memory**: 2048MB
- **Swap**: 512MB
- **Disk (rootfs)**: local-lvm:vm-104-disk-0
- **Disk Size (rootfs)**: size=8G
- **Disk Free percentage (rootfs)**: 48.0 percent
- **Startup**: order=3,up=30
- **Privilege Mode**: Privileged
- **Uptime**:  08:32:09 up 3 days

### Status:
status: running

### IP Addresses:
- 192.168.1.203/24

## Container ID: 106

### Configuration:
- **arch**: amd64
- **cores**: 2
- **description**: <div align='center'>
  <a href='https://Helper-Scripts.com' target='_blank' rel='noopener noreferrer'>
    <img src='https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/misc/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/>
  </a>

  <h2 style='font-size: 24px; margin: 20px 0;'>Stirling-PDF LXC</h2>

  <p style='margin: 16px 0;'>
    <a href='https://ko-fi.com/community_scripts' target='_blank' rel='noopener noreferrer'>
      <img src='https://img.shields.io/badge/&#x2615;-Buy us a coffee-blue' alt='spend Coffee' />
    </a>
  </p>

  <span style='margin: 0 10px;'>
    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a>
  </span>
  <span style='margin: 0 10px;'>
    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a>
  </span>
  <span style='margin: 0 10px;'>
    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a>
  </span>
</div>
- **features**: nesting=1
- **hostname**: stirling-pdf
- **memory**: 2048
- **net0**: name=eth0,bridge=vmbr0,hwaddr=BC:24:11:4D:0E:09,ip=dhcp,ip6=auto,type=veth
- **onboot**: 1
- **ostype**: debian
- **rootfs**: local-lvm:vm-106-disk-0,size=8G
- **swap**: 512
- **tags**: community-script;pdf-editor;tailscale
- **lxc.cgroup2.devices.allow**: a
- **lxc.cap.drop**: 
- **lxc.cgroup2.devices.allow**: c 188:* rwm
- **lxc.cgroup2.devices.allow**: c 189:* rwm
- **lxc.mount.entry**: /dev/serial/by-id  dev/serial/by-id  none bind,optional,create=dir
- **lxc.mount.entry**: /dev/ttyUSB0       dev/ttyUSB0       none bind,optional,create=file
- **lxc.mount.entry**: /dev/ttyUSB1       dev/ttyUSB1       none bind,optional,create=file
- **lxc.mount.entry**: /dev/ttyACM0       dev/ttyACM0       none bind,optional,create=file
- **lxc.mount.entry**: /dev/ttyACM1       dev/ttyACM1       none bind,optional,create=file
- **lxc.cgroup2.devices.allow**: c 226:128 rwm
- **lxc.mount.entry**: /dev/dri/renderD128 dev/dri/renderD128 none bind,optional,create=file
- **lxc.cgroup2.devices.allow**: c 29:0 rwm
- **lxc.mount.entry**: /dev/fb0 dev/fb0 none bind,optional,create=file
- **lxc.mount.entry**: /dev/dri dev/dri none bind,optional,create=dir
- **lxc.cgroup2.devices.allow**: c 10:200 rwm
- **lxc.mount.entry**: /dev/net/tun dev/net/tun none bind,create=file

### Resources:
- **Memory**: 2048MB
- **Swap**: 512MB
- **Disk (rootfs)**: local-lvm:vm-106-disk-0
- **Disk Size (rootfs)**: size=8G
- **Disk Free percentage (rootfs)**: 75.7 percent
- **Startup**: 
- **Privilege Mode**: Privileged
- **Uptime**:  08:32:19 up 3 days

### Status:
status: running

### IP Addresses:
- 192.168.1.186/24

## Container ID: 112

### Configuration:
- **arch**: amd64
- **cores**: 1
- **description**: <div align='center'>
  <a href='https://community-scripts.org' target='_blank' rel='noopener noreferrer'>
    <img src='https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/misc/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/>
  </a>

  <h2 style='font-size: 24px; margin: 20px 0;'>MeTube LXC</h2>

  <p style='margin: 16px 0;'>
    <a href='https://community-scripts.org/donate' target='_blank' rel='noopener noreferrer'>
      <img src='https://img.shields.io/badge/%E2%9D%A4%EF%B8%8F-Sponsoring%20%26%20Donations-FF5E5B' alt='Sponsoring and donations' />
    </a>
  </p>

  <p style='margin: 12px 0;'>
    <a href='https://community-scripts.org/scripts/metube' target='_blank' rel='noopener noreferrer'>
      <img src='https://img.shields.io/badge/%F0%9F%93%A6-Open%20Script%20Page-00617f' alt='Open script page' />
    </a>
  </p>

  <span style='margin: 0 10px;'>
    <i class="fa fa-github fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>GitHub</a>
  </span>
  <span style='margin: 0 10px;'>
    <i class="fa fa-comments fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE/discussions' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Discussions</a>
  </span>
  <span style='margin: 0 10px;'>
    <i class="fa fa-exclamation-circle fa-fw" style="color: #f5f5f5;"></i>
    <a href='https://github.com/community-scripts/ProxmoxVE/issues' target='_blank' rel='noopener noreferrer' style='text-decoration: none; color: #00617f;'>Issues</a>
  </span>
</div>
- **features**: nesting=1,keyctl=1
- **hostname**: metube
- **memory**: 2048
- **net0**: name=eth0,bridge=vmbr0,hwaddr=BC:24:11:C7:AA:72,ip=dhcp,type=veth
- **onboot**: 1
- **ostype**: debian
- **rootfs**: local-lvm:vm-112-disk-0,size=10G
- **swap**: 512
- **tags**: community-script;media;youtube
- **timezone**: America/New_York
- **unprivileged**: 1

### Resources:
- **Memory**: 2048MB
- **Swap**: 512MB
- **Disk (rootfs)**: local-lvm:vm-112-disk-0
- **Disk Size (rootfs)**: size=10G
- **Disk Free percentage (rootfs)**: 28.4 percent
- **Startup**: 
- **Privilege Mode**: Unprivileged
- **Uptime**:  08:32:28 up 3 days

### Status:
status: running

### IP Addresses:
- 192.168.1.247/24

## Host Disk Space Summary

- Filesystem            Size  Used Avail Use% Mounted on
- udev                  6.8G     0  6.8G   0% /dev
- tmpfs                 1.6G  3.1M  1.6G   1% /run
- /dev/mapper/pve-root   94G  6.8G   83G   8% /
- tmpfs                 7.8G   63M  7.7G   1% /dev/shm
- efivarfs              192K  101K   87K  54% /sys/firmware/efi/efivars
- tmpfs                 5.0M     0  5.0M   0% /run/lock
- tmpfs                 1.0M     0  1.0M   0% /run/credentials/systemd-journald.service
- tmpfs                 7.8G     0  7.8G   0% /tmp
- /dev/sda2            1022M  9.1M 1013M   1% /boot/efi
- data                  900G  489G  412G  55% /data
- /dev/fuse             128M   52K  128M   1% /etc/pve
- tmpfs                 1.0M     0  1.0M   0% /run/credentials/getty@tty1.service
- tmpfs                 1.6G  4.0K  1.6G   1% /run/user/0

