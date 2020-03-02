## Describing Tags
- Tags are like nicknames that you create for related field/value pairs
- Tags make your data more understandable and less ambiguous
- You can create one or more tags for any field/value combination
- Tags are case sensitive
## Using Tags
- To use tags in a search, use the syntax: tag=<tag name>
- To search for a tag associated with a value on a specific field
    - tag::<field>=<tagname>
- To search for a tag using a partial field value:
    - Use (*) wildcard
## Describing Event Types
- A method of categorizing events based on a search
- A useful method for institutional knowledge capturing and sharing
- Can be tagged to group similar types of event
## Using Event Types
- Splunk evaluates the events and applies the appropriate event types at search time

## Event types VS Saved Reports
### Event Types
- Categorize events based on search string
- Tag event types to organize data into categories
- The eventtype field can be included in a search string
- Does not include a time range
### Saved Reports
- Search criteria will not change
- Includes a time range and formatting of the results
- Can be shared with Splunk users and added to dashboards
  