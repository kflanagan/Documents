# Metrics to measure the effectiveness of automaition

How do you know if the time you spend automating things is really paying off?  You need to track it, you can't quantify what you don't track. To track things you need clear definitions of what it is that you are measuring. 

- Determine the average time to repair, of dedicated work time for each alert type.  (This becomes BME below)
- Name each automation to reflect the work
- Create a database to store this metadata
- Each automation should have a section that writes a row to a database, that would contain
  - Automation name
  - BME = Baseline Manual Effort (The time it takes to do things manually)
- Other informaiton is derived in your reporting
  - AVA = Automation Value Added (Added work that was not done by hand, but is now done by automation)
  - EME = Eliminitated Manual Effort (The number of times an automation runs multiplied by the BME)

Now you can say that you saved X number of hours per week, and did Y hours of additional work that hadn't been done in the past. 

  - OIA (Operator Interactions Avoided).  This is to show that there's lost time every time one of your people has to drop their project and react to an incident. Each transition is a number of minutes before that person is actively working. That is additional time saved in work to repair, but the restoration of service happens much faster if one machine does something that 3 different people did a part.


