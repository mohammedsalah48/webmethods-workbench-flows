# Collect values into a list

Topic: Mapping | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.list_from_fields:solve`)

## Task

Given `a`, `b` and `c`, return `items`: a String List holding the three values in that order.

## Signature

```
INPUTS: a, b, c (String)
OUTPUTS: items (String List)
```

## Solution

One MAP step with three links: a -> items[0], b -> items[1], c -> items[2].

## Package contents

`list_from_fields.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/list_from_fields/solve/`.

All sample tests and the hidden test passed on the site.
