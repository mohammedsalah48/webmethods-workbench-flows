# Follow a long path

Topic: Mapping | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.deep_colour:solve`)

## Task

Given the document `data`, return `colour`: the value at items (first entry) > attrs > colour.

## Signature

```
INPUTS: data (Document: items (Document List: attrs (Document: colour)))
OUTPUTS: colour (String)
```

## Solution

One MAP step with a single link: data/items[0]/attrs/colour to colour.

## Package contents

`deep_colour.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/deep_colour/solve/`.

All sample tests and the hidden test passed on the site.
