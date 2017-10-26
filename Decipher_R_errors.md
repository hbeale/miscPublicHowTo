
## Closure

```
Error in as.character(x) : 
  cannot coerce type 'closure' to vector of type 'character'
```
  You've used a function name as a variable. Often I cause this by forgetting to indicate which tibble a column belongs to. For example, 
  ```
 gsub("^(TH[0-9A-Z]*)_.*$", "\\1", sample)
 ```
 can be fixed by changing sample to annoCorrsToPlot $sample
 
 
