## Scheduled Reports
- a report that runs on a scheduled interval
- can trigger an action each time it runs
- scheduled report doesn't need time range picker
- how to create scheduled report is creating report first and then add schedule on the report
## create scheduled reports
- running concurrent reports, and the searches behind them, can put a big demand on your system hardware even if everything is configured to the recommended specs
- only admin user can set up schedule priority 
- include a schedule window only if the report doesn't have to start at a specific time and you're ok with the delay
## manage scheduled reports
- creating embedded report means anyone with access to the web page will be able to see the report
- an embedded report will not show data until the scheduled search is run
## alert 
- based on searches that run on scheduled intervals or in real-time
- notify you when the results of a search meet defined conditions
- triggered when search is completed
- alerts can be
    1. list in interface
    2. log events
    3. output to lookup
    4. send to a telemetry endpoint
    5. trigger scripts
    6. send emails
    7. use a webhook
    8. run a custom alert
## create alert
- alert can be defined by search result
- by default, everyone has read access and power users have write access to the alert
- scheduled alert type
    - allows you to set a schedule and time range for the search to be run
- real-time alert type
    - will run the search continuously in the background as soon as alert conditions are satisfied an action is triggered
    - this run continuously and can place more overhead on system performance
- trigger options means how often alert will sent during interval time
- admin users can find prebuilt alert actions by clicking the manage alert actions link