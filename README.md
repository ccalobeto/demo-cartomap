# About the project
This a simple demo of how to use protomaps. This [link](https://github.com/ccalobeto/build-pmtile/) explain how build a protomap. 

## Use the style
Go to *static/data/styles* and edit the `url` key with your recent pmtile located in `Public R2.dev Bucket URL`. Then in `src/routes/+page.svelte` edit the path of the recent custom style. 

## Preparate the style
- Build the protomap.
- Edit the `url` key of *peru-style.json* (gray scale):
```js
  "sources": {
    "protomaps": {
      "type": "vector",
      "attribution": "<a href=\"https://github.com/protomaps/basemaps\">Protomaps</a> © <a href=\"https://openstreetmap.org\">OpenStreetMap</a>",
      "url": "pmtiles://https://pub-d38145745fe247a1b3acb61ef28034c6.r2.dev/peru.pmtiles"
    }
  },
  ...
```

> [!WARNING]
> Don't forget to give credentials to your protomap file to be used only with specifics **urls**.

## See more styles
Use [carto](https://docs.carto.com/carto-for-developers/carto-for-react/guides/basemaps)

