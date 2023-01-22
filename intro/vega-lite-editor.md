# Vega-lite editor
When working with Vega code, you may choose to edit your code in different places.

## The Deneb code editor
**Pro:**
- Pull data straight from Power Query
- Integration with Power BI visuals, especially slicers
- Developing right where the visual will be used
- JSON repair and formatter is better
- Can generate a template to share with other Power BI users or your own reuse

**Con:**
- Source code is hard to manage
- Type-ahead isn't great
- Error messages aren't particularly helpful

## The online Vega editor
**Pro:**
- Easy to start from Vega examples or documentation
- Samples start with sample data
- Great type-ahead
- Better error messages
- Easy to generate link to share work in progress, especially for StackOverflow

**Con:**
- Difficult to bring in your data
- Security challenges of using confidential data or mocking up data
- Easy to lose progress in a browser window
- JSON formatter is aggressive

## Your favorite IDE, such as VS Code
**Pro:**
- Integration into your development environment
- Great if using visuals also in web app or Python/Jupyter

**Con:**
- Environment takes more effort to setup and configure
- Probably never as seamless as Vega editor or even Deneb editor

## When should I use each?
There probably is a time for each. I suggest using the **Vega editor** for trying new techniques or when you want help getting code to work. Use **Deneb** to work with your data and to support your production visuals. If you are a pure code shop and have development pipelines and source code management, I'd get your **IDE** set up and look at [pbi-tools](https://github.com/pbi-tools/pbi-tools) for your Vega source code management. (No idea if it works, but it's a good starting point.)

---
[**Home**](../README.md)

**Next:** [Power Query data export](./export-for-vega-editor.md)

**Prev:** [Encodings](./encodings.md)