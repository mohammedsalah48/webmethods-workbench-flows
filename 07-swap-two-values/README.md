# Swap two values

Topic: Mapping | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.swap_values:solve`)

## Task

Given `a` and `b`, return them swapped: `a` holds what `b` held, and `b` holds what `a` held.

## Signature

```
INPUTS: a (String), b (String)
OUTPUTS: a (String), b (String)
```

## Solution

One MAP step with two links: a -> b and b -> a.

## Package contents

`swap_values.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/swap_values/solve/`.

All sample tests and the hidden test passed on the site.
