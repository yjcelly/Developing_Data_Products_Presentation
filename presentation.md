Presentation of Simple Calculator
========================================================
author: liuyong
date: 2015-11-21


Framework of Simple Calculator
========================================================

Separate the input and calculation. Users only input the necessary numerics and operations. The server gathers the input and return the expression result online.

- User input the actual numeric, and click the button of 'Num'
- User click the '+', '-', '*', '/' to add the corresponding operations
- Server receive the numerics and operations, then return the result to user

UI action
========================================================
- numeric input text
- button of submit the numeric
- operation buttons of add, dec, mul and div
- show expression text online and dynamic update
- receive the result from servers
- show the usage help, warnings and examples for the users


Server code
========================================================
- receive the all numerics and operation, then convert them to a sequence string
- parse the sequence string and evaluate the expression
- return the value of expression to user

attention ideas
- record the multi-click num for every action button
- online update the expression string and the result

```r
eval_str <- "1+2*3+4"
eval(parse(text=eval_str))
```

```
[1] 11
```

Summary
========================================================
Disadvantage
- lack of strict parse module, the follow code will have error

```r
eval_str <- "1+*2*3"
eval(parse(text=eval_str))
```
- only contain basic operations

Advantage
- separate the input and Calculation
- online update the show expression and result
