# Proxmox Configuration Documentation
Generated on Sat May 30 07:32:07 PM EDT 2026

## Virtual Machines

## VM ID: 100

### Configuration:
- **agent**: 1
- **bios**: ovmf
- **boot**: order=scsi0
- **cipassword**: **********
- **ciupgrade**: 0
- **ciuser**: root
- **cores**: 2
- **description**: <div align='center'>
  <a href='https://Helper-Scripts.com' target='_blank' rel='noopener noreferrer'>
    <img src='https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/misc/images/logo-81x112.png' alt='Logo' style='width:81px;height:112px;'/>
  </a>

  <h2 style='font-size: 24px; margin: 20px 0;'>ubuntu VM</h2>

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
- **efidisk0**: local-lvm:vm-100-disk-0,efitype=4m,size=4M
- **ide2**: local-lvm:vm-100-cloudinit,media=cdrom
- **ipconfig0**: ip=dhcp,ip6=dhcp
- **localtime**: 1
- **memory**: 7168
- **meta**: creation-qemu=10.0.2,ctime=1754615694
- **name**: ubuntu-vm
- **net0**: virtio=02:A8:4F:D2:5C:FF,bridge=vmbr0
- **onboot**: 1
- **ostype**: l26
- **scsi0**: local-lvm:vm-100-disk-1,discard=on,size=30G,ssd=1
- **scsihw**: virtio-scsi-pci
- **serial0**: socket
- **smbios1**: uuid=836c7e9c-d0e0-41ad-9193-7a395fd1492c
- **startup**: order=1
- **tablet**: 0
- **tags**: community-script
- **usb0**: host=174c:55aa
- **virtio2**: /dev/disk/by-id/ata-TEAM_T2532TB_TPBF2412230030200230,backup=0,discard=on,size=2000398680K
- **vmgenid**: 195d7992-f916-4f36-bfef-8ba336cb1f7e

### Status:
status: running

### IP Addresses:
