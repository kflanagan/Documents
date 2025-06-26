# All Things Open 2023 notes


## Why I like ATO
  A real diverse collection of topics, some are directly related to work things, some tangentially, some not at all, but from all of them you learn something.
  
  A chance to get familiar with other companies/products

  A chance to grill a vendor or three

  There are alot of companies out there doing a business by wrapping services around Open Source Sofware, many more than you would think.  Sure a lot of them aren't going to offer the stability that a large company requires, but maybe in the future they will, it's helpful to know the history.

##  A key takeaway from booth row
  I spoke with the Cisco AppD folks a good bit, let them know that they would really do a service to the customers if they had a set of white papers on how to install the agent with each of the commonly used software distribution tools.  For example:  For Tanium, the best detection method would be really handy to know.


## Day one - Monday

### How to Design a Data Driven Culture

- If you aren't presenting the right data to people at the right time in the right format, you will fail
- A Data Mesh 
  - Domain driven design
  - Automonious domain teams
  - A mesh catalog connects all, live, via API
- Standards, with Federated data governance, the domain teams handle that
- A chief data officer is a must, to drive this
- Steps
  - Answer, What is the company mission?
  - How is data used to fulfill that mission? 
  - Define the data domains
  - Appoint stewards for each
  - Define data quality for each
  - co-create a culture of data ownership




### Using Open Shift as a Sandbox

- [Developer Sandbox](https://developers.redhat.com/developer-sandbox), sign up for developer sandbox, you get 30 days free
- Openshift as a service, this is a way to see more of Ansible Automation Platform
- slides  
- This will wipe itself every 30 days, but you can export your config to JSON, and re-import it, so you can get back where you were quickly

### Open Source Forests

    Amanda Casari amcasari at all the socials

- Funding
  - Keep orginizational calendars in mind
  - Measure impact in ways that leaders want
    - Objectives
    - Observable Aspects
    - Baseline 
    - Define the desired trend
    - Determine signal phenomena
      - Leading or lagging
- Resilient systems do not have one point of failure
- Ecosystems have no single points 
- Understand and grow things that are going well

### DevSecOps - A love triangle

  Burr Sutter - Redhat

- Slides are on Google Drive, couldn't get to from work phone, or even validate
- DevSecOps must have shared goals
  - The goals must be compelling, for who is the quesiton.  If you know this, you know who to seek to serve
- Think of making a new developer want to use it.
- Generally speaking, you are building for horses, not unicorns. Make the thing work for the most people/circumstances, not the edge case 
- Focus on the storm
  - Repeating the desired outcomes is powerful
- Self serve processes shorten the time to deliver valie


### Break Glass, Repair fast, Reconcile, Automate 

Rosemary Wang  - joatmon08.github.io

[Slides](https://speakerdeck.com/joatmon08/break-glass-repair-fast-reconcile-automation)

- Often automaiton adds complexity if you have to manually retrofit in emergency
- Who can breakglass? 
  - The access lifecycle, better than the binary model that most have
    - Making the access a part of the work, when the work is complete, the access is revoked. That can make it easier to get access
  - To provision access on demand
    - Define breakglass role
    - Define how to provision 
- Drift is the devil
- The slides are good, see them for a lot more detail


## Day two - Tuesday

### Know your data: The stats behind the alerts

- Mean/Median/Mode
- For the data to be useful, visualize it
- Rate change over time - How to do that?
- Approximate definitions
  - Mean = Average
  - Median = Middle
  - Mode = That which appears most frequently
- Mean can help you spot outliers
- Mode can help you spot the most common events/errors
- Samling really matters, when you can't deal with the volume
  - Head based - Random but selected in advance
  - Tail based - "Look for transactions over X size"
- LOTS more math than I'm prepared for.....
- Pitfalls
  - Fail to consider scale
  - Wrong central measure
  - Fail to see the biases
  - Getting correleation/causation backwards
  - Don't see causation because of correlation


### Empower efficency with full stack observability

- A War Room is often really "mean time to innocence", rather than finding the problems and solutions.  Meanwhile customers.......
- Full Stack observability
  - 68% of companies have too many tools
    - Consolidate
  - Timeley events in one place are what's useful
  - Fines for failures in tools/processes, as a means to accountability.  Could we have something like that?
- Allways remember that "Maybe it's not one failure, but multiple small ones"

###  Open infrastructure - What, Why, How

ildiko Vansca is Director of Community - ildiko@openinfra.dev

- Open infrastructure foundation supports openstack
- "95% of IT entities are using FOSS in mission critical places, wether they are aware of it or not"
- EU Cyber Resilency Act
  - Seems to be in conflict with Open Source practices
- Open Infrastructure is just infrastructure built with open source products/practices
  - Delivered as an ISO image
    - OpenStack
    - kubernetes
    - Ceph
    - QEMU
  - Example:
  - [StarlingX project](www.starlingx.io/blog)
- Openinfra.live on Thursdays

### Beyond passwords - Secure Authentication with PassKeys

- Passkeys are public/private key pairs
- Many of the slides couldn't be read in the room, too much small print.  Look for slides
- Google Password Manager can be the authenticator on a Mac where you might not want to use Safari.  Look in settings/passwords 
  

### Talking with Management about Open Source

- Ask yourself, Why do you do open source?
- Lead with the things the leadership cares about
  - Money
  - Results
- Can you look at the org's mission statement to see similarities to Open Source ethos
- Be sure to include giving back, to ensure that the projects you start using stick around
- There was a fix for Log4J in 4 days, even though it took a long time to roll out
- Can you show an Open Source project that's used in a corp product and how long it would take to replace it?  
- Companies are interested in driving things, not being popular. There's some challenge there with Open Source projects
- Think about the Open Source Engagement as a recruiting advantage
- Remember, it's "Free as in kittens", it's an investment, focus on the value

**Remember that it really is like this a lot of the time**
![Always remember](includes/../Real%20infrastructure.jpg)


