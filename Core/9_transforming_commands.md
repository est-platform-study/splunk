## Transforming commands
- order search results into a data table for statistical purposes
## Top Command
- Finds the most common values of a given field
- If limit size is 0, it returns all data
- Top command clauses
    ```
    - limit = int
    - countfield = string
    - percentfield = string
    - showcount = T/F
    - showperc = T/F
    - showother = T/F
    - otherstr = string
    ``` 
- To split by another field, Use the "by" clause
## Rare Command
- Same options as the top command but shows the least common values
## Stats Command
- it is to produce statistics of search results
- list of stats command is below
    ```
    - count
    - distinct count
    - sum
    - average
    - min
    - max
    - list
        - display all values
    - values
        - display unique values
    ```
## Count Function
## Dc Function
## Sum Function
- To get sum values of list created by count function, count function and sum function must be within the same pipeline
## Avg Function
- Missing or misformatted values are not added to the calculation
## List Function
## Value Function