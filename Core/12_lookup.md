## lookup
- a lookup is categorized as a dataset
- two steps to set up a lookup file
    1. define a lookup table
    2. define the lookup
- optionally configure your lookup to run automatically
- lookup field values are case-sensitive by default
## define lookup
- time-base lookup can be configured if csv file is time-based file
## lookup command
```
lookup http_status code as status
- status exist in our data will be matched to code in csv file
```
- if there is the same field name when lookup command creates new field by output operation, previous field will be overwritten
- outputnew operation is to make new field without overwrite previous field
## automatic lookups
## additional lookup options
- populate lookup table with search results
- define lookup based on external script or command
- use splunk db connect application to create lookups based on external databases
- use geospatial lookups to create queries that can be used to generate choropleth map visualizations
- populate events with KV store fields
## etc
- inputlookup command is to match internal data to external file like lookup command
