# Add VAT to a price

Topic: Math | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.vat:solve`)

## Task

Given `net`, return `vat` = 14% of net, and `gross` = net + vat. Both with exactly two decimal places. Example: 200 gives vat 28.00 and gross 228.00.

## Signature

```
INPUTS: net (String)
OUTPUTS: vat (String), gross (String)
```

## Solution

1. INVOKE `pub.math:multiplyFloats` with num1 = `net`, num2 = 0.14, precision = 2, giving `vat`.
2. INVOKE `pub.math:addFloats` with num1 = `net`, num2 = `vat`, precision = 2, giving `gross`.

## Package contents

`vat.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/vat/solve/`.

All sample tests and both hidden tests passed on the site.
