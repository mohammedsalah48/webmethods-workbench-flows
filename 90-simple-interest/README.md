# Simple interest

Topic: Math | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.simple_interest:solve`)

## Task

Given whole numbers `principal`, `ratePercent` and `years`, return `interest` = principal × ratePercent × years ÷ 100, using whole-number division. Example: 1000, 5 and 3 give 150.

## Signature

```
INPUTS: principal (String), ratePercent (String), years (String)
OUTPUTS: interest (String)
```

## Solution

1. INVOKE `pub.math:multiplyInts` with num1 = `principal`, num2 = `ratePercent`, giving `p1`.
2. INVOKE `pub.math:multiplyInts` with num1 = `p1`, num2 = `years`, giving `p2`.
3. INVOKE `pub.math:divideInts` with num1 = `p2`, num2 = 100 (whole-number division), giving `interest`.

## Package contents

`simple_interest.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/simple_interest/solve/`.

All sample tests and the hidden test passed on the site.
