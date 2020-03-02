## search and report app
- 7 component exist
- splunk bar, app bar, search bar, "how to search" panel, "what to search" panel, search history menu 
- sources means which the event originated
- host is usually ip, domain name, machine from which the event originated

## using search bar
- Limiting a search by time is key to faster results and is a best practice
- pattern tab is to see what your raw data is

## search job
- search job
    - By default, a search job wll remain active for ten minutes after its run
    - after 10 minutes, splunk rerun the search to get new result
- shared search job
    - Shared search job remain active for 7 days and everyone can see the same data

## search mode
- fast search
    - fast is cutting down on the field information that is returned
    - field discovery mode is unavailable in fast mode
- verbose mode
    - verbose mode return event information as much as it can
- smart mode
    - smart mode toggle search base on search we type on

## zoom in and zoom out
- if we select one event or zoom in, splunk use previous search data
- if we zoom out, splunk re-run search to get new result
 
## transforming
- commands that create statistics and visualizations are called transforming commands

## timezone format
- if data format is same, the time what you see in event is based on user timezone setting

## search term
- upper case NOT, OR, AND can be used for multiple terms
- if there s no boolean operation, AND is default action
- boolean operation ordering
    - NOT -> OR -> AND
- parentheses can change boolean operating ordering

## quiz
- events are not always returned in chronological order 



