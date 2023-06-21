# Begin: Friday 9-Jun - End Tuesday 20-Jun

## Goals
- Currency:
    - Get the UCD infrastructure off of RHEL 6 servers
    - Position for UCD upgrades, as our current version will be going out of support
    - Database server update to current MS SQL server
    - Migrate agent communication from Java to Web (JMS to WSS)
- Re-design
    - A smaller number of hosts
        - 2 Core servers (same as pre-existing)
        - 6 Relay servers (down by 4)
    

## Approach
- Parallel build of infrastructure
- Replicated database and shared filesystem at point in time
- Migrate agent nodes to new infrasructure
- Only migrate agents that have been active in the past 13 months



## infrastructure

Prior to the build we did test installations of the infrastructure parts and learned a few key things.
- A new JDBC driver was needed to connect to the new database server
- A new JDBC driver required a new version of the JRE was needed on the infrastructure servers
- DNS resolution for agent hosts to infrastructure servers is not predictable enough to rely on, IP addresses are used in agent configuration

In the migration there were several things learned
- The JRE on many agents would need to be upgraded from 1.7 to 1.8
- Many agents, especially the older RHEL 6 ones, neeeded to be made consistent
    - Upper case directory names didn't match with the response from the hostname command on the server.  This caused the Chef Cookbook to not be able to stop the running agent in the migration, meaning it could not start it again after updates were made
    - These RHEL 6 systems generally needed the JRE upgrade mentioned above
    - AIX hosts often needed the JRE upgrade as well
- More rigirous migration testing would have revealed most of these problems in advance

- It is probable that we could have changed the approach in the agent work with new relay servers connected to existing infrastructure first. This would have required further testing.
    - Build new relay servers connected to existing core servers
    - Migrate agents to new relay servers live, with no disruption to agent nodes
    - Build new core servers with replicated database and shared filesystem 
        - The shared filesystem might not even need to be duplicated for migration, but mounted on new core servers when built
    - Migrate new relay servers with attached agents to new core servers



# Most common agent issues
- Issue
    - Symptom

            Resolution
- Directory that UCD agent was installed in doesn't match the case of the hostname command on the server.  
    - hostname command returns servername in lower case
    - UCD installation directory "/opt/ibm-ucd/SERVERNAME/....

                - In the Web UI, rename the agent to .old
                - Stop agent 
                    - /opt/ibm-ucd/SERVERNAME/bin/agent stop
                - Check for agent processes 
                    - "ps -ef | grep -i ucd" until none are found
                - mv /opt/ibm-ucd /opt/ibm-ucd-old
                - perform a clean installation via Chef cookbook
                - Validate that the agent shows as online without the .old
                    - Migrate resources from .old to new agent
                    - Copy the description from .old to new agent
                    - Make sure that the new agent shows as licensed and true
- JRE at 1.7 will not connect
    - Agent will not connect, TLS errors in log /opt/ibm-ucd/servername/var/log/agent.out, repeated


                - In the Web UI, rename the agent to .old
                - Stop agent 
                    - /opt/ibm-ucd/SERVERNAME/bin/agent stop
                - Check for agent processes 
                    - "ps -ef | grep -i ucd" until none are found
                - mv /opt/ibm-ucd /opt/ibm-ucd-old
                - perform a clean installation via Chef cookbook
                - Validate that the agent shows as online without the .old
                    - Migrate resources from .old to new agent
                    - Copy the description from .old to new agent
                    - Make sure that the new agent shows as licensed and true
- Config file changes were applied, but agent didn't restart
    -   The agent is showing no change in the Web UI, but a review of the config files show the new server values

            - In the Web UI, rename the agent to .old
            - Stop agent as above
            - Start agent with run command to see results inline
                - /opt/ibm-ucd/servername/bin/agent run
                    - Look for "Connected to server" message, with one of the new relay server IP addresses
                    - Check Web UI for agent to show status of online
                - ^c 
                - start the agent as backround processes
                    "/opt/ibm-ucd/servername/bin/agent start"
            - Validate that the agent shows as online without the .old
                    - Migrate resources from .old to new agent
                    - Copy the description from .old to new agent
                    - Make sure that the new agent shows as licensed and true


### Manual options
- JRE update (Linux and Unix)

        - Login in to a server with the same OS 
        - In /opt/ibm-ucd/opt see the 1.8 java directory
            - tar -cvf "directoryname".tar "directory name"
        - scp .tar to new host (requires the password on the new host)
        - On new host mv tar to /opt/ibm-ucd/opt
        - tar -xvf tarfile.tar
        - Edit config files, update all occurences of old jre directory with new
            - /opt/ibm-ucd/servername/conf/agent/installed.properties
            - /opt/ibm-ucd/servername/bin/agent
            - /opt/ibm-ucd/servername/bin/configure-agent

- Migrate agent

        - Edit config files replacing lines with old servers with new
            - /opt/ibm-ucd/servername/conf/agent/installed.properties



    