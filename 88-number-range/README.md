# Spread of a list

Topic: Math | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.number_range:solve`)

## Task

Given `numbers` (String List of whole numbers), return `range`: the highest value minus the lowest. Example: [4, 9, 1] gives 8.

## Signature

```
INPUTS: numbers (String List)
OUTPUTS: range (String)
```

## Solution

1. INVOKE `pub.math:max` with numList = `numbers`; maxValue maps to `hi`.
2. INVOKE `pub.math:min` with numList = `numbers`; minValue maps to `lo`.
3. INVOKE `pub.math:subtractInts` with num1 = `hi`, num2 = `lo`, giving `range`.

## Package contents

`number_range.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/number_range/solve/`.

All sample tests and both hidden tests passed on the site.
