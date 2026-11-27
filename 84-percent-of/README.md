# Work out a percentage

Topic: Math | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.percent_of:solve`)

## Task

Given `part` and `total`, return `percent`: part as a percentage of total, with exactly one decimal place. Example: 1 and 4 give 25.0.

## Signature

```
INPUTS: part (String), total (String)
OUTPUTS: percent (String)
```

## Solution

1. INVOKE `pub.math:divideFloats` with num1 = `part`, num2 = `total`, giving `r`.
2. INVOKE `pub.math:multiplyFloats` with num1 = `r`, num2 = 100, precision = 1, giving `percent`.

## Package contents

`percent_of.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/percent_of/solve/`.

All sample tests and both hidden tests passed on the site.
