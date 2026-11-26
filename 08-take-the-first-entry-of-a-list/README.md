# Take the first entry of a list

Topic: Mapping | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.first_item:solve`)

## Task

Given `items` (String List, never empty), return `first`: its first entry.

## Signature

```
INPUTS: items (String List)
OUTPUTS: first (String)
```

## Solution

One MAP step with one link: items[0] -> first.

## Package contents

`first_item.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/first_item/solve/`.

All sample tests and the hidden test passed on the site.
