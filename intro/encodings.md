# Encodings
## Encoding channels
[Marks](./marks.md) are encoded with values or data. Depending on the type of Mark, different **encoding channels** are used.

The easy ones to relate to are the **positional** channels:
|[Line/Shape](https://vega.github.io/vega-lite/docs/encoding.html#position)| |[Polar](https://vega.github.io/vega-lite/docs/encoding.html#polar)| |[Geographic](https://vega.github.io/vega-lite/docs/encoding.html#geo) | |
|--|--|--|--|--|--|
|`x`|`y`|`theta`|`radius`|`longitude`|`latitude`|
|`x2`|`y2`|`theta2`|`radius2`|`longitude2`|`latitude2`|
|`xOffset`|`yOffset`|||
|`xError`|`yError`|||
|`xError2`|`yError2`|||

Then there are also [**Mark property**](https://vega.github.io/vega-lite/docs/encoding.html#mark-prop) channels:

`angle`, `color`, `fill`, `stroke`, `opacity`, `fillOpacity`, `strokeOpacity`, `shape`, `size`, `strokeDash`, `strokeWidth`, 
`text`, `tooltip`, `href` (hyperlink), `description` (ARIA accessibility), `detail`, `key`, `order`, `facet`, `row`, `column`

## Encoding properties
For each of these channels, you specify 1 or more properties. Every channel must have data tied to it from one of these three properties:

|Property|Description|
|--|--|
|[`field`](https://vega.github.io/vega-lite/docs/field.html)|The name of a field. It should also specify the [`type`](https://vega.github.io/vega-lite/docs/type.html) property, set to `"quantitative"`, `"temporal"`, `"ordinal"`, `"nominal"` or `"geojson"`|
|[`value`](https://vega.github.io/vega-lite/docs/value.html)|A hard coded visual value (text)|
|[`datum`](https://vega.github.io/vega-lite/docs/datum.html)|A hard coded data value (number, [DateTime](https://vega.github.io/vega-lite/docs/datetime.html), or [expression](https://vega.github.io/vega-lite/docs/types.html#exprref))|

Optional properties don't apply to every channel.
[`aggregate`](https://vega.github.io/vega-lite/docs/aggregate.html),
[`Axis`](https://vega.github.io/vega-lite/docs/axis.html),
[`Band`](https://vega.github.io/vega-lite/docs/band.html),
[`Bin`](https://vega.github.io/vega-lite/docs/bin.html),
[`Condition`](https://vega.github.io/vega-lite/docs/condition.html),
[`Format`](https://vega.github.io/vega-lite/docs/format.html),
[`Header`](https://vega.github.io/vega-lite/docs/header.html),
[`Impute`](https://vega.github.io/vega-lite/docs/impute.html),
[`Legend`](https://vega.github.io/vega-lite/docs/legend.html),
[`Scale`](https://vega.github.io/vega-lite/docs/scale.html),
[`Stack`](https://vega.github.io/vega-lite/docs/stack.html),
[`Sort`](https://vega.github.io/vega-lite/docs/sort.html),
[`Time Unit`](https://vega.github.io/vega-lite/docs/timeunit.html)

---
[**Home**](../README.md)

**Next:** [Vega-lite editor](./vega-lite-editor.md)

**Prev:** [Marks](./marks.md)