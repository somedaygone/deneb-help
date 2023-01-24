# Power Query data export
Let's say you have data in Power BI already loaded in a table, and are happily using it in Deneb. But then you have a need to try your Vega code in the online Vega editor, let's say so you can generate a link to your chart and sample data in StackOverflow.

What you need is a Power Query script that will convert your data to JSON. I've seen versions of this as a function, but I prefer to just paste this query in when I need it.

Note that I would also add a **Keep Top Rows** step and limit my data to under 20 rows. The more data you have, the longer the link gets, and short links are just less fussy.

```
// ExportQueryToVega
let
    // Change "Your_Query_Name" to the name of your existing query that you want to import into Vega
    // From Advanced Editor, enter "Source = Products,"
    // but from the formula bar, just enter "= Products"
    Source = Your_Query_Name,
    // It is a good idea to use Keep Top Rows to limit data to less than 20 rows
    JsonOutput = Json.FromValue(Source),
    OutputText = Text.FromBinary(JsonOutput),
    VegaWrap = """data"": {""values"": " & OutputText & " } }"
in
    VegaWrap
```

---
[**Home**](../README.md)

**Next:** [High level and common properties](./properties.md)

**Prev:** [Vega-lite editor](./vega-lite-editor.md)
