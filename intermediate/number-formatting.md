# Number Formatting
I'll have more out here later, but the quick version is that Vega number formatting is awkward, Excel formatting rocks, and Power BI's formatting is almost as awesome as Excel but frustratingly different.

While you are stuck with hacky work-arounds in Vega, the good news is that you can use Power BI's formatting in Deneb because Daniel Marsh-Patrick rocks! He build in a formatter that uses Power BI's format strings. See [Formatting Values](https://deneb-viz.github.io/formatting) on the Deneb help site.

> In Vega-Lite, we can specify `"pbiFormat"` as a `formatType` wherever you're specifying a format.
```json
  "encoding": {
    "x": {
      "field": "$ Sales",
      "type": "quantitative",
      "axis": {
        "format": "$#0,,,.0bn",
        "formatType": "pbiFormat"
      }
    }
  }
 ```
 
Remember that Power BI format strings aren't quite the same as Excel. See [Custom Format Strings](https://docs.microsoft.com/en-us/power-bi/create-reports/desktop-custom-format-strings).
