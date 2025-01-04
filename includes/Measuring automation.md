# Metrics to measure the effectiveness of automaition

How do you know if the time you spend automating things is really paying off?

- Determine the average time to repair, of dedicated work time for each alert type.  (This becomes BME below)
- Name each automation to reflect the work
- Create a database to store this metadata
- Each automation should have a section that writes a row to a database, that would contain
  - Automation name
  - BME = Baseline Manual Effort
- Other informaiton is derived in your reporting
  - EME = Eliminitate Manual Effort (The number of times an automation runs multiplied by the BME)

Now you can say that you saved X number of hours per week. 

Another thing you might measure we call OIA (Operator Interactions Avoided).  This is to show that there's lost time every time one of your people has to drop their project and react to an incident. Each transition is a number of minutes before that person is actively working. That is additional time saved in work to repair, but the restoration of service happens much faster if one machine does something that 3 different people did a part.

