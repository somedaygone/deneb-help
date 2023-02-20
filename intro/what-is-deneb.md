# What is Deneb?

Deneb is a Power BI custom visual that allows you to create your own awesome visuals.

Before Deneb, if you wanted to create your own custom visual, you had to write code. The skill set required is beyond the average user of Power BI, so business users mostly stick with Microsoft visuals and some of the awesome free visuals on AppSource.

Now with Deneb, custom visuals can be created by savvy power users like you.<sup>[1](#savvy)</sup> It does require writing Vega or Vega-lite code, but if you ever had to create an HTML page for school, it's more like that!

```json 
{
  "description": "A simple bar chart.",
  "data": {"name": "dataset"},
  "mark": "bar",
  "encoding": {
    "x": {"field": "a", "type": "nominal"},
    "y": {"field": "b", "type": "quantitative"}
  }
}
```
---
[**Home**](../README.md)

**Next:** [What is Vega?](./what-is-vega.md)

<a name="savvy">1</a>: How do I know you are a savvy power user? You are reading a footnote on GitHub!
