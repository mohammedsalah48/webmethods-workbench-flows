# Split a bill

Topic: Math | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.split_bill:solve`)

## Task

Given whole numbers `total` and `people`, return `share`: total ÷ people as a whole number (the remainder is dropped). Example: 100 and 3 give 33.

## Signature

```
INPUTS: total (String), people (String)
OUTPUTS: share (String)
```

## Solution

One INVOKE of `pub.math:divideInts` with num1 = `total` and num2 = `people` (whole-number division); value maps to `share`.

## Package contents

`split_bill.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/split_bill/solve/`.

All sample tests and the hidden test passed on the site.
