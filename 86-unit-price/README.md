# Work out a unit price

Topic: Math | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.unit_price:solve`)

## Task

Given `total` and `quantity`, return `unitPrice` = total ÷ quantity with exactly two decimal places. Example: 10 and 4 give 2.50.

## Signature

```
INPUTS: total (String), quantity (String)
OUTPUTS: unitPrice (String)
```

## Solution

One INVOKE of `pub.math:divideFloats` with num1 = `total`, num2 = `quantity` and precision = 2; value maps to `unitPrice`.

## Package contents

`unit_price.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/unit_price/solve/`.

All sample tests and the hidden test passed on the site.
