## What is the Common Information Model(CIM)
- The Splunk Common Information Model provides a methodology to normalize data
## Splunk CIM Add-on
- Set of 22 pre-configured data models
    - Fields and event category tags
    - Least common denominator of a domain of interest
- Leverage the CIM so that knowledge objects in multiple apps can co-exist on a single Splunk deployment
## datamodel Command
- allows user to examine data models and run the search for a datamodel object
- return a description of all or a specified data model and its objects
- is a generating command and should be the first command in the pipeline
### example
```
| datamodel Web Web search | fields Web*
      A      B   C     D       E
A Command
B Data model name
C Data model dataset name
D Command
E Find field names with Web prefix
```
- When using the datamodel command, the data model name and dataset name are case-sensitive 