# Why use Deneb?
In Power BI, the standard visuals are pretty good, but not always fully customizable. If a formatting option doesn't exist, there isn't much more you can do about it. The standard visuals also don't support all chart types (gantt, bloxplot, word cloud, radar, raincloud, etc.). 

You can often find visuals on AppSource that have better formatting options or cover special chart types, but they also have limited formatting options and often require licenses.

The Deneb custom visual in Power BI is free and creates visuals via [Vega code](./what-is-vega.md). That generally means if you can envision it, Vega can create it. It also does a smashing job at creating combo charts, which often can have a drastic improvement in performance on a visual-heavy page and keeps your charts axes in sync.

Finally, Deneb has some real advantages over Python and R visuals in Power BI. Python and R generate static images that you can't click on. Deneb offers fully cross-hitering and cross-highlighting with other Power BI visuals. Vega also has better hover and click interactions than the standard Power BI visuals. Python and R have the advantage of having a rich and deep set of libraries, but few libraries are supported in PowerBI.com for published dashboards, and you are limited to years old versions of [Python 3.7.7 (March 2020)](https://learn.microsoft.com/en-us/power-bi/connect-data/service-python-packages-support#requirements-and-limitations-of-python-packages) and [R 3.4.4 (March 2018)](https://learn.microsoft.com/en-us/power-bi/connect-data/service-r-packages-support#requirements-and-limitations-of-r-packages). Library management is a huge problem for Python and R in Power BI. Deneb's dependency to Vega is baked into the visual. Deneb 1.4.0.0 uses Vega 5.22.1 (current as of January 2023) and Vega-Lite 5.4.0 (July 2022).

---
[**Home**](../README.md)

**Next:** [JSON basics](./json-basics.md)

**Prev:** [Why is it called Deneb?](./why-named-deneb.md)
