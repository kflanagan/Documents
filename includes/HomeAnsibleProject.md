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
