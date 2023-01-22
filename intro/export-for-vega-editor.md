# Power Query data export
Let's say you have data in Power BI already loaded in a table, and are happily using it in Deneb. But then you have a need to try your Vega code in the online Vega editor, let's say so you can generate a link to your chart and sample data in StackOverflow.

What you need is a Power Query script that will convert your data to JSON. I've seen versions of this as a function, but I prefer to just paste this query in when I need it.

Note that I would also add a **Keep Top Rows** step and limit my data to under 20 rows. The more data you have, the longer the link gets, and short links are just less fussy.

```
SCRIPT GOES HERE
```

---
[**Home**](../README.md)

**Next:** [High level and common properties](./properties.md)

**Prev:** [Vega-lite editor](./vega-lite-editor.md)