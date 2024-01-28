# Platform modernization

I joined a team at work that was doing the job, but had a mountain of technical debt in the platform that they supported, [UCD](https://www.ibm.com/docs/en/urbancode-deploy/7.1.1?topic=overview-urbancode-deploy)  

In early 2023 we began an effort to bring the platform up to date, and back into support, with a goal of being 1 release behind the most recent. 


In writing out the steps it strikes me just how much work it really was.  **Phew**

It was worth ***every*** step of preparation for the upgrade, even if at the time it might have seemed excessive.

 
We were told by more than one vendor resource that they had never seen that many versions jumped at once.

 

 

## Summer of 2023

We began an effort to modernize the infrastructure that would take nearly a year, while continuing to provide service to the developers within the company who had software to deploy.  That is the point of the UCD infrastructure after all. 

- Simplified design to have only 5 servers
  - 2 core servers
  - 3 relay servers
- Migrate from 2 core and MANY relay servers to new virtualized servers
- Simplified Firewall rule set
- All server networks, on specified ports, to new UCD infrastructure
- Same version of UCD, but different VMs
  - Old servers were RHEL 6, new are RHEL 8

All agents had to be touched to communicate with the new servers. 
That clearly could have gone much better, but was a crucial step to prepare for the UCD infrastructure upgrade

 

 

## Infrastructure upgrade 6-Jan-2024

 

- Constant engagement with a key resource from the vendor, our advocate gave us a lot of time. His ability to find answers to things on IBM’s site very quickly was a huge help
- Engagement with additional IBM resources to have people standing by at every step
- Created tickets in advance every time we upgraded, letting IBM UCD support know what we were up to, so any need for support would be clear and move fast
- Communicated regularly to our customer base, plans and dates
  - Created a document for one of those communications that outlined the most apparent differences in the User Interface
- Move all JMS agents to WMS, this is a protocol, Java vs Web communication.  There were about 100 left.
- Build DEV environment
  - 3 servers
  - 2 core
  - 1 Relay
- On Core server #1 we installed UCD 7.0.3 as configured in production, but without data
  - MS SQL DB
  - NFS shared filesystem
- During the installation we kept notes of all of the details that were worked out as we went, and pre-requisites.
- Java 8 to Java 11 upgrade, and switch to OpenLogic, the MetLife standard
- Start UCD 7.0.3 with the new Java
- Modified 2 things in the installer
  - 1 because we are no longer using IBM Java, but the MetLife standard
  - 1 because we were making so many jumps at once, disabling a check for JMS agents, since we had moved all to WMS agents in advance
- On DEV Core server #2 we installed UCD 7.0.3 as configured in production, but without data
- On DEV Core server #1 we upgraded from UCD 7.0.3  UCD 7.3.2 as HA peer
- Upgrade 1 relay server from UCD 7.0.3  UCD 7.3.2
- Remove UCD from DEV core server #2
- Rebuild UCD on DEV core server #2 with UCD 7.0.3 as configured in production, but without data
- On DEV Core server #1 we upgraded from UCD 7.0.3  UCD 7.3.2 using notes from above, and vendor documentation
- Rebuild UCD on DEV relay server with UCD 7.0.3 as configured in production
- Upgrade DEV relay server from UCD 7.0.3  UCD 7.3.2
- Testing of agents
  - Abitha coordinated a great test cycle that leveraged our offshore team
    - Every plugin that exists in prod was installed in DEV
    - Every plugin was tested using DEV UCD clients from the AD teams
    - Move the agent to use the DEV infrastructure
    - Perform at least one, test deployment, making sure to use those plugins
    - Move the agent back to production for them
    We had a few known things from plugin version updates that happen automatically when you upgrade, but with them known Abitha had fixes or work-arounds ready
### Ready for Production upgrade!
- Scheduled change!
  - Shut down UCD
  - Database snapshot in case of need to roll back
  - Shared storage snapshot in case of need to roll back
- Begin the upgrade at 9AM
- Follow the directions on the first prod server, just as we had for the second DEV upgrade
- The only real difference was that it took longer for the upgrade because we had shared storage of 14TB, and a large Database, approx. 2TB that get auto updated in the upgrade
- Follow the directions on the second prod server (HA peer), only differences were for the fact that it was second, so some additional info needed
- Upgrade the 3 relay servers
- Java 8 to 11 as above
- UCD 7.0.3 to 7.3.2
- Check that agents were communicating, getting licenses and we could do a test deployment (thanks again to Abitha!)
- Take UCD out of maintenance mode so customers can start using it
- Close change at approx. 14:30
- Communicate to all customers
- Monitor for a few hours
 


Monday after a big upgrade like that you generally expect to have a good number of incidents.  We have seen somewhere in the neighborhood of 10 from the upgrade!

 

A member of our sister team resolved one issue centrally post upgrade, but before any customers hit it.

 

The most common incident has been that some bad practices worked with the old version of UCD, but no longer do. 

Hard coding a particular plugin version in the deployment scripts used to just run with whatever was the new version, it no longer does.  The fix is to call the plugin but not by version in their deployment scripts. 