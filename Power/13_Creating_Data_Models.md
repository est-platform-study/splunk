## Overview of Data Models
- Hierarchically structured datasets that generate searches and drive Pivot
- Pivot reports are created based on datasets
- Each event, search or transaction is saved as a separate dataset
### dataset types
- Events
- Searches
- Transactions
## Event datasets
- Event datasets contain constraints and fields
- Constraints are essentially the search down into a hierarchy
- Fields are properties associated with the events
## Adding Fields
- Auto-extracted 
    - can be default fields or manually extracted fields
- Eval Expression
    - a new field based on an expression that you define
- Lookup
    - leverage an existing lookup table
- Regular Expression
    - extract a new field based on regex
- Geo IP
    - add geographical fields such as latitude/longitude, country, etc
## Field Types
- String
- Number
- Boolean
- IPV4
## Field Flags
- Optional
    - this field doesn't have to appear in every event
- Required
    - Only events that contain this field are returned in Pivot
- Hidden
    - This field is not displayed to Pivot users when they select the dataset in Pivot
    - Use for fields that are only being used to define another field, such as an eval expression
- Hidden & Required
    - Only events that contain this field are returned, and the fields are hidden from use in  Pivot
## Adding Child Datasets
- When you create a new child dataset, you give it one or more additional constraints
- Child datasets inherit all fields from the parent events
- You can add more field to child datasets
## Search and Transaction Dataset Considerations
- There must be at least one event or search dataset before adding a transaction dataset
- Search and transaction datasets cannot benefit from persistent data model acceleration
- As you learn to create data models, consider the types of reports your users will run
## Data Model Acceleration
- With persistent data model acceleration, all fields in the model become "indexed"  fields
- You must have administrative permissions or the accelerate_datamodel capability to accelerate a data model
- Private data models cannot be accelerated
- Accelerated data models cannot be edited
- Only root events can be accelerated
    - If there are multiple root events, only the first root event is accelerated

