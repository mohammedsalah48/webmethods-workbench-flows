# Reach into a document list

Topic: Mapping | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.second_line_sku:solve`)

## Task

Given `order` with a list `lines`, return `sku`: the sku of the second line.

## Signature

```
INPUTS: order (Document: lines (Document List: sku, qty))
OUTPUTS: sku (String)
```

## Solution

One MAP step with one link: order/lines[1]/sku -> sku.

## Package contents

`second_line_sku.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/second_line_sku/solve/`.

All sample tests and the hidden test passed on the site.
