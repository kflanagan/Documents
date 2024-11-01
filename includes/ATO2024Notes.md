# All Things Open 2024 - 27-29 Oct 2024 
[ATO 2024](https://2024.allthingsopen.org/)

# Sunday 27-Oct CLS (Community Leadership Summit)

The CLS is a co-located event, that's free for anyone, focused around Open Source community, and those who would lead.
[CLS at ATO 2024](https://2024.allthingsopen.org/community-leadership-summit)

-----------   
**From their site:**

The Community Leadership Summit 2024 brings together community leaders, organizers and managers and the projects and organizations that are interested in growing and empowering a strong community. Leading minds in community management, relations and online collaboration will discuss, debate and continue to refine the art of building an effective and capable community.

------------

The CLS is run as an unconference, and more small sessions that are designed to be conversation rather than presentation.  A good opportunity to consider how things can be approached/thought about differently.

Since these were all conversations, it wasn't really the kind of thing that creates a lot of notes.  


# Monday 28-Oct 

## You're going to need to test that
- Better testing will save time and money.  
Sounds obvious, but it's apparently not since we see a lot of things that aren't tested as well as they could be.
    - How do you write better tests.  
    - Tools based tests
    Be careful of tools based tests incurring extra costs from cloud services
    What about analytics/linters etc built in to the IDEs, where can we leverage them?
    - Manual tests
    Better than no tests, but often challenging, if there's not a written plan it's haphazard at best

## Access Self Hosted services remotely, and securely - Alex Kietzschmer 

This session is really more interesting for people who need to get to things at home when away, and can install the Tailscale client. (Not work systems or phones)
  - Tailscale is the focus of this session
  - See selfhosted.show for ongoing content
  - VM/Containers only limit the damage if you port forward.  
  They don't completely secure anything, but it could mean that only one app is damaged if you have an exposed vulnerability.
  - NAT traversal is how Tailscale gets you access. 
  - Tailscale has a feature referred to as funnels, a way to make an app be "published" to the greater internet without all kinds of work on things like reverse proxies etc.
    - immich - Google Photos like
    - gitea - like a self hosted github
    - Traefik / Caddy - reverse proxy
    - Libation - for audible files
    - Possible to apply blocking rules in DNSMASQ instead of all of the work in pihole. 
## Making OS updates Fast, Easy and Safe 
  - bootc - takes a container and makes something bootable, similar to a full VM.  This may be something to look at for test systems, very stripped down.
  - UniversalBlue - A project to look into
## How You Write Matters
  - Have a voice - Consistency really matters
  - Style guides, pick one, of course at work it's the corporate one, use it, not others
  - Don't expect anyone to read what you write - At least at first
  - Guideposts for things like naming.  Not everything is in the style guide, maybe look at inclusivenaming.org for some help in inclusivity, but get the guideposts and stick to what you pick, consistency matters
  - You audience may be global 
  This may seem obvious to many of us at Met, but a reminder is often helpful. Don't use idoms that won't make sense to someone who grew up in a different place.  "Remember on Mayberry RFD when .....?" that's usually lost on someone who grew up in India.
  - Be clear about who's saying what - "We want XXX" isn't great, who is the we? Not the "royal we"
  - Testing your writing means people, could get messy, but that's what it takes

# Tuesday 29-Oct

## Change is in our bones

- Graceful extensability - How systems strech to handle surprises
- Adaptive Capacity - Not capacity management, but capacity to change
  - These things above cause constant descruction/construction.  Things communicate
- Resilence Engineering - Engineering applied to resielent systems to encourage adaptation
- Queer Theory of Lichens - a paper to look for to read.  Challenge how we percieve the world
- The commonality of the speaker being a trans woman and the practice of resilence engineering is an interesting thought, constantly ready for, or embracing change
  
## How a 60's technlogy evolved and survived

- MUMPS is the technology in question
- App code from the 80s will generally still just run
An evolution of GT M from the 80's which was an evolution of MUMPS from decades before that.



## Balancing transparency and openness in Gov't

- Too many 1 off soltions for projects were the kicker
- Location data was enough to just get people to go elsewhere
- A centralized clearinghouse, but without tracking is the result


## Dependency Management

- deps.dev is a publishedplace to look for info
- They published (internally) their stats and info to get understanding (can/should we?)
- a scan of the greater internet repositories found about  1/4th of a million vulnerabilities
- Effective dependency management is about tradeoffs, which options are scalable and automated?
-----  
Can we visualize things like these to help make the case/motivate folks
- INC to OS mapping.  (What percentage of RHEL 6 systems generate what percentage of the issues, for example)
- What about a dependency graph but not for code, but rather our platforms

## 4 Habits of highly successful infrastructure and ops teams - [Kevin Kline KeKline on LinkedIn](https://www.linkedin.com/in/kekline/)

- [Remember the Capablity Maturity Model?](https://cmmiinstitute.com)
- Rely on data (from systems), not thoughts
- Can we require that we be consulted on this like updates/changes in a certain scope?
- Behaviors become habits, always a decent reminder
- Publicize averages, like "average deployment time" or some other metrics we can back up. 
  - Monitor
  - Leverage the monitoring data to
    - Plan for the future with our customers
    - Build out IT Ops processes


## Other misc notes
- Chef and Elastic had a good presense there.  
    I prodded the Elastic folks at their booth to get on that open ticket, and it seems to have had an impact, Mark was able to get past that issue on Tuesday. 
    
    Chef conversations were a bit tricky, I started with talking about their installation process, the Director of Engineering was motivated.  The sales/support territories are being juggled, the guy from that org that was there was all kinds of wound up, wants to do a presentation for the team in their Morrisville office, and on and on. How to not say that we are migrating off, and not be too focused on fixing more than we have to, but keep engaged so we get the support we need is a challenge.


There is more competition for Elastic than I've seen before, DataDog is just one

[The Linux Foundation has free learning as well as paid](https://linuxfoundation.org)
40% off elearing courses, certifications and bundles with code ``` ATO24 ``` at checkout
  

