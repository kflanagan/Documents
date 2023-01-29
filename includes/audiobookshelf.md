# AudioBookShelf a short project
***Sunday 29-Jan-2023***

I spotted this project on youtube, since I had a collection of audio books, and thought that not being tied to Audible would be best, I thought I'd give it a try.

***Environment at the start***
- Hardware
    - Raspberry Pi 4B 8GB RAM
    - 240GB SSD in external USB-3 case
- Software
    - Ubuntu ARM-64
    - Docker, installed as a snap (more on why that matters in a bit)
    - Plex server installed manually
- Containers
    - Home Assistant
    - Portainer
    - Pi-Hole
    - Dashy
    - Jellyfin

I saw this project and since it ran as a container, the risk of making my Pi unstable was very low, so why not. 

[Audiobookshelf](https://www.audiobookshelf.org/)

As I attempted to start the container I kept getting error messsages that indicated that the volume I was trying to use for the audiobooks was read only.  I tried making the directory world read/write/execute, no dice.  I tried pre-creating the volumes, no dice. I got some help on the community Discord, no dice. 

Then I discovered, with help, the following info, and suddenly it all made sense.

    If you are running Docker as a snap on Linux, this build can only access files in the home directory. 

My solution was as follows:
- Create the user account and home directory (This was not in the documentation)
- Put a 1TB drive that I took out of my laptop in an external USB-3 case
- Partition it so that I have one just for the audio books
- Mount the new partition on the audiobookshelf user home directory 
- Proceed with the installation as usual

I did not make this server visible to the internet, there's no need. I can connect the client when at home, download a book, and listen in offline mode.

There are Andriod and iOS(Beta only) clients that seem to work pretty well. 

I'm pretty happy with the result, it's easy to use and functional. I even forked the github project and added what I discovered to the installation guide. The maintiner said that I'm the only person to have encountered this problem, so if he accepts the PR remains to be seen.
