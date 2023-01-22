# Why use Deneb?
In Power BI, the standard visuals are pretty good, but not always fully customizable. If a formatting option doesn't exist, there isn't much more you can do about it. The standard visuals also don't support all chart types (gantt, bloxplot, word cloud, radar, raincloud, etc.). 

You can often find visuals on AppSource that have better formatting options or cover special chart types, but they also have limited formatting options and often require licenses.

The Deneb custom visual in Power BI is free and creates visuals via [Vega code](./what-is-vega.md). That generally means if you can envision it, Vega can create it. It also does a smashing job at creating combo charts, which often can have a drastic improvement in performance on a visual-heavy page and keeps your charts axes in sync.

Finally, Deneb has some real advantages over Python and R visuals in Power BI. Python and R generate static images that you can't click on. Deneb offers fully cross-hitering and cross-highlighting with other Power BI visuals. It also has better hover and click interactions than the standard Power BI visuals. Python and R have the advantage of having a rich and deep set of libraries, but few libraries are supported in PowerBI.com for published dashboards, and you are limited to years old versions of Python and R. Library management is a huge problem for Python and R in Power BI. Deneb's dependency to Vega is baked into the visual.

---
[**Home**](../README.md)

**Next:** [JSON basics](./json-basics.md)

**Prev:** [Why is it called Deneb?](./why-named-deneb.md)