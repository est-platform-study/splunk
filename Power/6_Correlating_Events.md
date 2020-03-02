## Transaction
### What is a Transaction?
- A transaction is any group of related events that span time
### transaction Command
- Example: transaction field-list
    - Events are grouped into transactions based on the values of these fields
    - If multiple fields are specified and a relationship exists between those fields, events with related field values are grouped into a single transaction
- Common constraints
    - maxspan
        - Maximum total time between the earliest and latest events
    - maxpause
        - Maximum total time between events
    - startswith, endswith 
        - To form transactions based on terms, field values, or evaluations, use startswith and endswith options 
- The transaction command produces additional fields
    - duration
        - the difference between the timestamps for the first and last event in the transaction
    - eventcount
        - the number of events in the transaction
### transaction VS stats
- When you have a choice, use stats
    - it's faster and more efficient, especially in large Splunk environments
- Only use transaction when you:
    - need to see events correlated together
    - must define event grouping based on start / end values or segment on time
- Use stats when you:
    - want to see the results of a calculation
    - can group events based on a field value 
- By default, there's limit of 1000 events per transaction
    - No such limit applies to stats
    - Admin can change limit by configuring max_events_per_bucket in limits.conf

