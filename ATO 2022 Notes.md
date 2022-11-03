#  Session Notes
## Tuesday
### Building and running a support department
- Rewards for participation, not just the heroes, that gets the work spread around
- Create a better triage process for issues/bugs where the work is done by rotating team members, gets everyone engaged in them
- Scheduled times for each developer to work the queue, not just block out some time that gets ignored
- Maybe we can have an event like a hack-a-thon for the teams that own their own work, each pitch in to help them

### What we learned from dissecting the most popular containers
- The number of vulnerabilities is staggering
- slim.ai is something to look at

### Say Vulnerability One More Time
- ****  We need as-built docs, that get updated with every fix
- OpenSSL just announced a couple of BAD CVEs, take a look for our exposure with IPSoft
- Probably worth metrics for things like how long a bug is open, both from us and vendor
- Don't forget, "Better Done Than Perfect"
- The faster and more efficient the pipeline is, the more secure you will be.  Get fixes out there, then fix the next thing
- Avoid the "all hands on deck" situations, Prioritize then mitigate, then remediate as BAU work

###  Developing on WSL 
- Set default console to Terminal, much faster
- WSLG gives you full Linux GUI apps
- HanselMinutes is Scott Hanselman's podcast
- In a browser, when hanging up, F12 then Right Click on the reload icon in the bar, new options

###  Learning infrastructure with your own computer cluster
- Turing Pi board, with 4 computer modules, a great cluster for not that much $

##  Wednesday
### The future of service mesh
- Solo.io looks interesting
- istio, see books. They provide a way to do things like dynamic failover
- Ambient mesh
- Look for GraphQL, a way to get data from many sources, APIs, and DBs

###  How content creation took my career to the next level
- James Q Quick is the speaker, he has a lot of content on youtube
- You need to learn a lot of new skills to do that
- Communication can be your Super Power, A way of leading is by being a great communicator
- Can github be my own personal repo for writing?  Yes, but I'll need to learn markdown a lot better, good for work stuff too
- https://dev.to/monisnap/bye-bye-postman-let-s-share-your-rest-api-calls-in-team-easily-h6l 
     Rest Client - an extension for VS Code, you can use in place of postman
- learnbuildteach.com takes you to a Discord server, where James shares a lot 

###   Verbs not Nouns - writing documentation that users will want to read
- Sidebars for navigation are a good idea where possible
- A tutorial tells a story/journey, they smooth the path
- Verbs that imply a change of state are more helpful
       Install, configure, etc
        gerends can be OK (end in ing, installing), but use intentionally
- Make an outline where you just lay out the steps quickly, and look for steps within steps
- prioritize cases
- After the brain dump, look for verbs, those are the actions that should probably start your steps
- Categorize steps - Beginner, intermediate, advanced, that will help make the doc useful, and trim things out, or move to another doc
- Dont assume any knowledge
- At the end of a step, summarize.  "Now that you have X, let's go to Y"
- Each step should do one thing
- Active voice, start each step with a verb.  Read the step till you hit a verb, you can probably drop everything before that.
- Semicolons can usually be replaced by periods
- If you write for everybody , you will please nobody, focus on the audience
- Avoid marketing copy  
