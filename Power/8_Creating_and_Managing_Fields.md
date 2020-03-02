## Field Extraction
- Splunk automatically discovers many fields based on source type and key/value pairs found in the data
- At search time, field discovery discovers fields directly related to the search's results
- In addition to the many fields Splunk auto-extracts, you can also extract your own fields with the Field Extractor(FX)
## Field Extraction Method
### Regex
- Use this option when your event contains unstructured data like a system log file
- FX attempts to extract fields using a Regular Expression that matches similar events
### Delimiter
- Use this option when your event contains structured data like a .csv file
- The data doesn't have headers and the fields must be separated by delimiters(spaces, commas, pipes, tabs, or other characters)
