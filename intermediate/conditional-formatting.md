# Conditional Formatting

**General form**  
Replace `"value"` with `{"expr": "if(datum.Field == 'test','value1','value2')"}`

**Notes:**  
- `expr` is short for expression, meaning you are entering a formula.
- Some help on Expression syntax can be found on the [Vega help site](https://vega.github.io/vega/docs/expressions/)
- Surround text literals and text values in single quotes eg. `'test','value1','value2'`
- Any columns you reference in the formula need to be prefixed with `datum.`, eg. `datum.ColumnName`. If there are spaces in the column name, replace them with underscores in the expression like this: `datum.My_Column_Name`.
- To test a value, use this format: `"if(test, thenValue, elseValue)"`
  - Note there is an alternate format using Ternary operators: `"test ? thenValue : elseValue"`. Don't use the ternary format. It is harder to understand. 
  - The `if` must be lowercase. Uppercase `IF` will not work.
  - When testing equality, use a double equal sign `==`. A single equal `=` will not work.
- Note that you can't do any aggregations (eg. `sum`) in the formula like `"if(sum(datum.ColumnA) > 1000,1,0)"`
  - If you want an aggregation, you have to use a [`transform`](https://vega.github.io/vega-lite/docs/transform.html) statement (either [`aggregate`](https://vega.github.io/vega-lite/docs/aggregate.html) or [`joinaggregate`](https://vega.github.io/vega-lite/docs/joinaggregate.html)) or [Aggregate in Encoding Field Definition](https://vega.github.io/vega-lite/docs/aggregate.html#encoding).

## Examples  
### Format positive and negative values differently in same mark  
```
	    {
	      "description": "Labels",
	      "mark": {
	        "type": "text",
	        "color": "black",
	        "align": {"expr": "if(datum.Field >= 0,'left','right')"},
	        "angle": 315,
	        "dx": {"expr": "if(datum.Field >= 0,10,-15)"}
	      },
```

### Different line styles in same mark
```
      "mark": {
        "type": "line",
        "strokeWidth": {"expr": "if(datum.Type=='Forecast',10, 6)"},
        "strokeDash": {"expr": "if(datum.Type=='Forecast',[10,20],[1,0])"}
      },
```

### Change KPI line color based on field aggregation  
Normally you use `datum.Amount` in the expression. If you want to use an aggregated value, prefix the column with agg_type and an underscore, like `datum.mean_Amount`.

```
{
  "description": "KPI line",
  "mark": {
    "type": "rule",
    "color": {
      "expr": "if(datum.mean_Amount >= 0,'green','red')"
    }
  },
  "encoding": {
    "y": {
      "aggregate": "mean",
      "field": "Amount"
    }
  }
}
```
