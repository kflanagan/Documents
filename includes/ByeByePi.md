# The end of the Pi, for now at least

Over the last few weeks I was noticing that my Pi was freezing up.  My suspicion is that it was the cheap 240GB SSD that I was using as the boot device.

I also came to the conclusion that my laptop just wasn't much for the lap anymore.  I have replaced the battery and the drive in it recently, it's still a lot more powerful than the Pi, so I decided to move the workloads over to that.

The laptop was already running Ubuntu Linux so it was fairly easy. 
- Install Docker on the laptop
- Copy the data and config directory trees from the Pi disk to the laptop
- Install Portainer, using the same directory on disk for the volume that it stores the config info in
- Install the Home Assistant Docker container, pointing at that directory for all config etc.
- Copy all of the data to the other external drive on the laptop.  AudioBookShelf, and Plex serve that up.
- Install AudioBookshelf, using the new copy of the data directory, and the copied config from the Pi
- Install Plex locall, no container, there are some limitations that I wanted to avoid.
- Set up Plex libraries
- Install Jellyfin Docker container, also pointing to the config and data directories that I migrated
- Export via NFS and Samba a few directories on the laptop

A really remarkable amount of things just worked the same, in spite of different hardware architectures and all of the moving. 

I now have a pretty good home server, that has plenty of horsepower, and enough disk space for just me. 

I think that I need to look into how to selectively sync directories on the server (formerly laptop) to OneDrive, we get a TB of storage there each as part of the family Microsoft 365 subscription, might as well use it.