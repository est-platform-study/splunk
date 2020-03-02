# core test
- what is the function to count unique value
```
dc(field)
```

- what is the function to get unique value list
```
values(field)
```

- what is the color of command in search bar
```
blue
```

- How do you add or remove fields from search results?
```
A. Use fields +to add and fields -to remove. (answer)
B. Use field +to add and field -to remove.
C. Use table +to add and table -to remove.
D. Use fields Plus to add and fields Minus to remove
```
  
- In production environment, what is installed in client?
```
forwarder
```

- what can do in report edit panel

- how to add if field is not exist in interesting field

- what command return count and percentage
```
options were top, count, stats etc....
```

- By default, which of the following fields would be listed in the fields sidebar under interesting Fields?
```
A. index (answer)
B. sourcetype
C. source
D. host
```

- What is a primary function of a scheduled report?
```
A. Triggering an alert in your Splunk instance when certain conditions are met (answer)
B. Auto-detect changes in performance
C. Auto-generated PDF reports of overall data trends
D. Regularly scheduled archiving to keep disk space use low
```

- In a deployment with multiple indexes, what will happen when a search is run and an index is not specified in the search string?
```
A. Events from every index searched by default to which the user has access will be returned. (answer)
B. No events will be returned.
C. All non-indexed events to which the user has access will be returned.
D. Splunk will prompt you to specify an index.
```

- how to optimize query speed
```
- time is the most efficient filter
- specify one or more index values at the bginning of your search string
- include as many search terms as possible
- make your search terms as specific as possible
- inclusion is generally better than exclusion
```
  
- how to set time range picker to make report which return events of 24 hours
```
options were 
- real-time | earleast = 1d@d and latest = now
- relative | earleast = 1d@d and latest = now
- advanced | earleast = 1d@d and latest = now         
```
  
- from -72h@h to 1d@d means 
```
query from 3days to the beginning of today
``` 

- how to expand report available time to 7 days
```
share the report
```
  
- if boolean operation is not exist in query
```
default option is AND 
```

- if event is indexed, what is the default field of time
```
_time (maybe?)
```
    
- what interesting fields on side bar means
```
20% of events have the field
``` 

- what is the meaning of number on the left size of field name on side bar
```
how many unique values are exist on field (maybe?)
```

- what is the options of top command
```
showperc, countfield
```

- rare command means
```
- return the least values in events
- option was return the minimum values in events (etc....)
```

- how to naming objects
```
<group>_<object>_<description>
```

- how to get search result at statistic table
```
click field name on statistic table
```

- how to define ky / value pairs 
```
=, < , >
```

- how to divide field in sort command
```
,
```

- if field is added to selected field, what will happen
```
the field you added into selected field will be shown under row of search result
```

- what is the meaning of timeline under search bar
```
user can find spike by timeline
- zoom-in doesn't re-search result
```

- how long search job is available
```
10 minutes
```

- what is the query to get count of 'specified field'
```
index='specified index' | stats count by 'specified field'
```

- what is the query to get the most common 15 values of 'specified field' 
```
top limit 15 (specified field)  
```

- if somebody can modify report, what that person can do
```
- options were permission, accelation, schedule, ?
- accelation maybe incorrect 
```

- what report owner can edit on report edit panel

- if alert triggers script, where the script should be located in
```
please somebody find the answer
```

- how to make query fast by using field "+" or dedup command

- why create panels from reports
```
- a single report can be used across different dashboards
- any change to the underlying report affects every dashboard panel that utilizes that report
```

- how to make schedule report
```
- select 'schedule' on 'save as report' panel
- options were 'schedule' and 'scheduling'
```
  
- how to express boolean (true or false)
```
boolean should be lower case (maybe?)
```