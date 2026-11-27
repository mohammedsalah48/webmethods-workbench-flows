# Calculate a line total

Topic: Math | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.order_total:solve`)

## Task

Given whole numbers `quantity` and `unitPrice`, return `total` = quantity × unit price.

## Signature

```
INPUTS: quantity (String), unitPrice (String)
OUTPUTS: total (String)
```

## Solution

One INVOKE of `pub.math:multiplyInts` with num1 = `quantity` and num2 = `unitPrice`; value maps to `total`.

## Package contents

`order_total.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/order_total/solve/`.

All sample tests and the hidden test passed on the site.
