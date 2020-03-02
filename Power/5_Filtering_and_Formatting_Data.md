## eval Command
- eval allows you to calculate and manipulate field values in your report
```
eval fieldname1 = expression [, fieldname2 = expression2]
```
- Results of eval written to either new or existing field you specify
    - if the destination field exist, the values of the field are replaced by the results of eval
    - Indexed data is not modified, and no new data is written into the index
### round function
- round(field/number, decimals) function sets the value of a field to the number of decimals you specify
### tostring function
- tostring converts a numeric field value to a string
```
tostring(field, "option")
```
- options
    - "commas"
        - applies commas
    - "duration"
        - formats the number as "hh:mm:ss"
    - "hex"
        - formats the number in hexadecimal

## formatting and sorting values
- eval with added characters converts numeric field values to string
- To order numerically, first sort, thn use eval
## eval Command - if and case
- if(X, Y, Z)
    - The if function takes three arguments
    - The first argument, X, is a Boolean expression
        - If it evaluates to TRUE, the result evaluates to the second argument, Y
        - If it evaluates to FALSE, the result evaluates to th third argument, Z
    - Field values are treated in a case-sensitive manner
- case(X1,Y1,X2,Y2...)
    - The first argument, X1, is a Boolean expression
    - If it evaluates to TRUE, the result evaluates to Y1
    - If it evaluates to FALSE, the next Boolean expression, X2, is evaluated, etc
    - If you want an "otherwise" clause, just test for a condition you know is true at the end (e.g., 0=0)
## eval function
- To count the number of events that contain a specific field value, use the count nd eval functions
    - Used within a transforming command, such as stats
    - Requires an as clause
    - Field values are case-sensitive
## Filtering Results - search and where
- The search and where commands both filter results
    - search
        - Treats field values in a case-insensitive manner
        - Allows searching on keyword
        - Can be used at any point in the search pipeline
    - where
        - Can compare values from two different fields
        - Functions are available, such as isnotnull()
        - Treats field values in a case-sensitive manner
        - Can't appear before first pipe in search pipeline
## fillnull Command
- Use fillnull to replace null values in fields
```
Example: fillnull value=NULL
```
- If no value=clause, default replacement value is 0