## fields sidebar
### selected fields
- selected fields are unimportant to user
- by select fields, we can limit what field will be shown on search result list

### interesting fields
- interesting fields show fields which have values in at least 20% of the events
- a means string
- hash tag means numeral

### search
- field name is case sensitive
- search value is not case sensitive
- equal and not equal is used with numerical or string values
- splunk support IN operation

### difference between not equal operation and NOT boolean operation
- Not equal operation return events that field value is not exactly equal
- NOT operation return all events that field value is not equal or not exist 