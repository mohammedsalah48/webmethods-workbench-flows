# Total a list of amounts

Topic: Math | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.float_total:solve`)

## Task

Given `amounts` (String List of decimal numbers), return `total` with exactly two decimal places. Example: [1.10, 2.20] gives 3.30.

## Signature

```
INPUTS: amounts (String List)
OUTPUTS: total (String)
```

## Solution

1. INVOKE `pub.math:addFloatList` with numList = `amounts`, giving `sum`.
2. INVOKE `pub.math:roundNumber` with num = `sum`, numberOfDigits = 2 (formats with `toFixed`, so exactly two decimals); roundedNumber maps to `total`.

## Package contents

`float_total.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/float_total/solve/`.

All sample tests and both hidden tests passed on the site.
