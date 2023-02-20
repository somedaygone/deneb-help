# High level and common properties
|Property|Type|Description|
|---|---|---|
|`$schema`|text|This sets the version of Vega, but is ignored in Deneb.|
|`name`|String|Name of the visualization.|
|`description`|String|Description of a spec or `mark` for commenting purposes. JSON doesn't support comments, so use this instead with every `mark`. Always include a web link when using sample code from the Internet.|
|`title`|Text or [TitleParams](https://vega.github.io/vega-lite/docs/title.html#params)|Title for the plot. Can include a `subtitle` and other formatting.|
|`data`|Data|Required. Always the same for Deneb to access data from Power BI: `"data": {"name": "dataset"}`. You cannot pull in external data from the AppSource version of Deneb, though you can hard code data as in Vega samples, but you have to add one field to the Deneb visual to access the Deneb editor. See [Deneb help](https://deneb-viz.github.io/dataset#augmenting-other-datasets) for more on the `data` object.|
|`transform`|array|An array of data transformations such as filters and new field calculations.|
|`params`|array|An array of parameters that may either be simple variables, or more complex selections that map user input to data queries. This is where mouse hover and selection occurs.|
|`mark`|
|`encoding`|
|`layer`|
|`hconcat`|
|`vconcat`|
|`facet`|

## Deneb Template specific properties
This is as of version 1.4.0 (2022-08-31) of Deneb. Check [Deneb documentation](https://deneb-viz.github.io/templates#template-structure), as this is one area that will likely change. See also the [Deneb schema](https://deneb-viz.github.io/schema/deneb-template-usermeta-v1.json).

### `deneb` object
|Property|Description|
|---|---|
|`build`|Which version the template was built with. Whist this is required, it is purely for the purposes of troubleshooting at these early stages, so is ideally left as-is.|
|`metaVersion`|The template metadata version. Only a value of 1 is currently supported.|
|`provider`|Which provider should be used when loading and parsing the template. Valid values are vega or vegaLite. If this is manually modified, Deneb will do its best to auto-resolve this from the top-level $schema property (if supplied), falling-back to parsing spec. It's not guaranteed to be successful. |

### `information` object
|Property|Description|
|---|---|
|`name`|The name of the template that is displayed in the dialog for users, once imported.|
|`description`|Longer-form details of the template purpose that are displayed in the dialog for users, once imported.|
|`author`|Used to identify the author. Currently not displayed in the dialog upon import (but might be later on).|
|`uuid`|unique ID for the template.|
|`generated`|time (in UTC) the template was generated.|
|`supportUri`|(reserved for future use) A URI to indicate where further information about the template can be found (such as a blog or website).|
|`videoUri`|(reserved for future use) A URI to indicate where a supporting video asset, such as a demo or 'how-to' guide can be found.|
|`previewImageBase64PNG`|(reserved for future use) Placeholder for a base64-encoded PNG image, which could be used for displaying a thumbnail or assistive image. This is shown in the Create New Specification dialog if included with the template. Images should be no larger than 150x150 pixels.|

---
[**Home**](../README.md)

**Prev:** [Power Query data export](./export-for-vega-editor.md)