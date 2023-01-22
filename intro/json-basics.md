# JSON basics
Vega specs are written in [JSON](https://en.wikipedia.org/wiki/JSON) (JavaScript Object Notation), which uses *attribute-value pairs*.

````
{
    "attribute": "value",
    "anotherAttribute": 2,
    "object: {
        "objectAttribute": null
    },
    "list": ["list", "aka array"]
}
````

- Attributes and values are separated with a colon `:`
- Attributes and strings are put between double quotes `" "`
- Numbers are not put between quotes
- Lists (aka arrays) are put between square brackets `[]`
- Objects are put between curly brackets `{}`
- Comments are not supported 

**Tips for working with JSON in the Deneb editor**
- Changes are not effective until applied. You can do that four different ways:
    1. Type Ctrl+Enter after each edit
    2. Click the Apply button after each edit
    3. Type Ctrl+Shift+Enter once to turn on Auto-apply
    4. Click the Auto-apply button once
- Indenting code is essential for matching up braces and brackets in JSON. Keep your indent levels clean as you enter code. After pasting in code, use the **Repair and Format JSON** button to clean up indents or fix errors
- When you get an error, start by checking quotes, commas, and braces
- Use triangles to expand/collapse sections
- If you are trying to confirm what a `"mark"` or `"layer"` does, collapse it, delete it, see what disappeared in the preview pane, and then use Undo (Ctrl+Z) to bring it back.
- Always start a spec with a `"description"`. If you've copied the spec from the web, include a link to the source.
- Always start a `"mark"` with a `"description"`. These are the best way to include comments. You can't put descriptions everywhere, but do it at every `"mark"`.
- Don't forget about the `config` tab, especially when copying from another Deneb viz. Often the formatting can be essential for the viz to look right.

---
[**Home**](../README.md)

**Next:** [Vega-lite documentation](./vega-lite-doc.md)

**Prev:** [Why use Deneb?](./why-use-deneb.md)