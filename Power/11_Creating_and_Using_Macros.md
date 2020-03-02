## Macros Overview
- Useful when you frequently run searches or reports with similar search syntax
- Macros can be a full search string or a portion of a search that can be reused in multiple places
- Allows you to define one or more arguments within search segment
    - Pass parameter values to macro at execution time 
    - Macro uses values to resolve search string
## Using a Basic Macro
- Type the Macro name into the search bar
- Surround the macro name with the backtick(or grave accent) character
    - \`macroname\` != 'macroname' 
    - Do not confuse with single-quote character(')
- Pipe to more commands, or precede with search string
## Adding arguments
- Include the number o arguments in parentheses after the macro name
```
monthly_sales(3)
```
- Within the search definition, use $arg$
- In the arguments field, enter the name of the argument(s)
## Using Arguments
- When using a macro with arguments, include the arguments(s) in parentheses following the macro name
- Be sure to pass in the arguments in the same order as you defined them
- Don't create macros with leading pipes
    - someone may put a pipe in front of the macro when using it in the actual search string
 