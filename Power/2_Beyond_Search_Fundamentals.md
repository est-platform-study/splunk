## Case sensitive VS Case insensitive
### case sensitive
- Boolean Operators (Uppercase)
- Field names
- Field values from lookup (default, but configurable)
- Regular expressions
- eval and where commands
- Tags
### case insensitive
- Command names
- Command clauses
- Search terms
- Statistical functions
- Field values
## Buckets
- As events come in, Splunk places them into an index's hot bucket
- As buckets age, they roll from the hot to cold
## Searching
- Splunk uses the time range to choose which buckets to search and then uses the bucket indexes to find qualifying events
- When you search, Splunk uses the time range to choose which buckets to search and then uses the bucket indexes to find qualifying events
- As events are stored by time, time is the most efficient filter
- After time, most powerful keywords are host, source, sourcetype
## Wildcards
- Wildcards at beginning of string scan all events within time frame
- Wildcards in middle of string may return inconsistent results
## General Search Practices
- Inclusion is generally better than exclusion
- Filter as early in your search as possible
