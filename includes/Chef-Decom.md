I initially wrote this reently approximately 12/18/2025, updates done in place.


**FML** Because my employer has opted to get away from Chef as an automation platform we sent the vendor notice recently.  

The company (as usually happens) waited until the other day so that if we needed support in November they would answer the phone. 

Tuesday we got a note from the vendor that wanted me to run a program that would scan the infrastructure servers for their software to validate that we removed it.  I responded to the email informing them that I couldn't because we have already decommissioned the infrastructure servers. 

When they got that they were good with that, but sent us a PDF to get a signature on.  Of course I was thinking that it was the infrastructure servers, about 25 of them that are have in the process being deleted. I forwarded that to my director, knowing that it would be at least her level that needed to sign, it turns out that it has to go to the global CIO, that part isn't my problem.
Here's the twist.  The letter said that we have to uninstall the client for _ALL_ of the servers in the enterprise.  **By the end of the year**, this year. 

I got to work on what I can do.
- Generated the list of servers that have the client installaed before the last of the infrastructure servers got turned off. 
- Went to the CMDB and got the environment and Operating System info
- Organized our list of targets using that CMDB data so we can work on the non-prod hosts first (we are in the end of year change freeze)
- Ceated Ansible templates that run the scripts we have 
- Tested another tool to run the scripts, but Ansible was the only automation that worked. 

We have the client on just over 9100 servers.  Windows, Linux and AIX hosts, even about 10 Solaris ones. (we have no automation for Solaris hosts, or access so I don't now how it'll happen).

The next day was Friday I was scheduled to be off, but worked the until about 2:30 PM. 

A few other folks did some good work. 
- Update the Ansible Playbooks to add logging so we have the audit trail for the work
- Made the output clearer to read from that logging, that will help our team

I think that we are ready to go after the first of the year to create changes for the work, schedule it out and go. We will do change requests for non-prod even though we aren't required to, that way we will have a much easier time with approvals for the production hosts having done the work on thousands of non-prod hosts.