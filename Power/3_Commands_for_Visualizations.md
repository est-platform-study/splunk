## chart command
- the first field after the over clause is the x-axis
### over field by field
- You can use the by clause with the over clause to split results
- Alternatively, you can just use two **by** clauses 
- You can only split chart results over two dimensions

## Including Null and Other values
- To remove empty (NULL) and OTHER field values from display, use these options
```
useother=f
usenull=f
```
- To remove null values, add itemId=* to the base search

## Limiting the Number of Values
- For unlimited values, use limit=0
- When splitting on two dimensions, the limit option applies to the second split

## timechart Command
- timechart command performs statistical aggregations against time
- _time is always the x-axis
- Adjust the interval using the span argument, e.g. span=15m

