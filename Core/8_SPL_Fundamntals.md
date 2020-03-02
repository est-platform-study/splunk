## The Splunk Seach Language
### Search Terms
### Commands
- Commands tell Splunk what we want to do with the search results
- this includes creating charts, computing statistics and formatting
### Functions
- Functions explain how we want to chart, compute and evaluate the result
### Arguments
- Arguments are the variables that we want to apply to the function
### Clauses
- clauses explain how we want results grouped, or defined
### pretty
- Ctrl + \ format SPL more readable
### field command
- only selected field will be shown on search result
- negative sign means that field with negative sign will be excluded on search result
- field extraction is one of the most costly parts of searching in splunk
- field inclusion happens before field extraction and can improve performance
### table command
- retains searched data in a tabulated format
- this command is to make search result more easy to understand
- the result of this command will be shown in table
### rename command
- Once renamed, original name is not available to subsequent search commands
### dedup command
- dedup command removes events with duplicate values
### sort command
- numeric field will be displayed in ascending order
- plus mark('+') after sort command means ascending order, minus means descending order
- if there is no space between plus mark and field name, the operation only affects the field directly behind it
- limit operation can be available after sort command  