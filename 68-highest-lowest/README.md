# Find the highest and lowest

Topic: Math | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.highest_lowest:solve`)

## Task

Given `numbers` (String List of whole numbers), return the largest in `highest` and the smallest in `lowest`.

## Signature

```
INPUTS: numbers (String List)
OUTPUTS: highest (String), lowest (String)
```

## Solution

1. INVOKE `pub.math:max` with numList = `numbers`; maxValue maps to `highest`.
2. INVOKE `pub.math:min` with numList = `numbers`; minValue maps to `lowest`.

## Package contents

`highest_lowest.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/highest_lowest/solve/`.

All sample tests and the hidden test passed on the site.
