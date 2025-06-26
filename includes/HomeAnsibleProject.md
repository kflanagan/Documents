# 14-Jan-2024 - Ansible vault

Another long time since the last update.  
Ansible Vault is how you can save a password and refer to it in playbooks.

I do not have all of the features at home that corporate environments would have, but this is a great one to not worry about that password in clear text anywhere.

[Ansible Vault docs](https://docs.ansible.com/ansible/2.9/user_guide/vault.html)

The idea is that you secure the password for sudo escalation in the vault and give the vault password at run time. 

To leverage this, I just wrote a 1 line shell script that takes one parameter. 

        #!/bin/bash
        # A wrapper for a playbook, so I don't have to remember the syntax
        # Takes one parameter, the full path of the playbook to run

        # The passwd.yaml vault is created in the current directory
        # ansible-vault create passwd.yaml

        # See /etc/ansible/hosts for the variables syntax and see the line below to call the vault
        ansible-playbook   --ask-vault-pass --extra-vars '@passwd.yaml' $1 

# 4-July-2023 - Ansible Semaphore
It's been a while since I updated this page, today I installed Ansible Semaphonre, a web based GUI for ansible. It requires a database, so a quick MariaDB installation first, then just download, install and configure.
[Semaphore](https://docs.ansible-semaphore.com/administration-guide/installation)
It works just fine, given that I just charged forward, not really reading the docs, but looking things up in them when it wasn't obvious it went pretty well.
I do now need to go back and make the installation more "proper" not use root for the DB, and make Semaphore auto start should be about all, but since they are on a VM that's usually not running, it's not critical that I do it this morning. 
# 16-Jan-2023
OK, I have my Ansible stuff in "good enough" state.  I learned quite a bit. I'll start something new next, maybe Chef, but that seems to require a good bit more infrastructure to build, where Ansible was about 30 minutes to functional.
## Linux
- I have the bare bones "configure a Linux machine like the others for NFS and SMB sharing"
- Apply all updates
- Display basic info, disk space etc.
## Windows
- Check drive space and show a message if c: has less than 3GB free
- Apply all updates, and log results to a file
- Windows is a pain in the ass with the \ vs /.  

# 8-Jan-2023
I've done some inventory work today, now I have a short yaml that will get system info and display it, then check to make sure that / has 3GB free.   I think that the next thing to try, probably next weekend is handling the failure states to conditionally do things on a host.



# 2-Jan-2023
Since github doesn't do includes, I'll have to work with the links.

## Current projects at home
I recently set up an ansible server on a Virtual machine, mostly so I could learn some Ansible things, as it may come in handy at work.  I work best when I have a thing to do that I'll want to keep around, so I decided that I was going to set this up in a way that will make setup of new Virtual machines easy to be consistent in the following ways.
- File sharing between physical and virtual systems
- All pointing at one the physical desktop computer, in a directory that I have cloned my Testing github repo
- Exporting the same directory on all of the physical and virtual machines
- Auto mounting of some of these directories on demand on other systems

I have a mix of things at home.
- Physical Windows, Linux, ChromeOS, Android and iOS devices
- Virtual Linux, and soon Windows machines 

I run virtual machnies on a physical Desktop computer with Ubuntu Linux on it.  Native virtualization, qemu/KVM, with Virtual Machine Manager as the user interface.

Because Ansible is a thing that I have very little exposure to, and it can be installed on a virtual Linux machine in under 10 minutes, that looked like a good thing to try to get familiar with. 
https://github.com/kflanagan/Documents/blob/main/includes/Ansible.md


To do this, I have a few ansible playbooks, I have commented them with each function, maybe it could be better, but it's a start.

https://github.com/kflanagan/Testing/blob/master/ubuntu-setup.yaml

https://github.com/kflanagan/Testing/blob/master/ansible/Fedora-setup.yaml

There are a small number of other files there, mostly ones I got working, but are now inclded in the other playbooks.  Notice that there are zero windows commands in here, that's coming up, but it's different enough that I'm not ready to start that yet.

## Projects at work
As responsiblities shift a bit in the new year, I need to get more familiar with the following tools.
- Tanium
- UCD
- Chef

This is to support the new team that I'm part of, take some responsiblities off of the shoulders of folks who are there, and tie some things together. 
