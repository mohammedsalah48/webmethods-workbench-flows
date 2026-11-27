# Apply a percentage discount

Topic: Math | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.discount:solve`)

## Task

Given whole numbers `amount` and `percent`, return `discount` = amount × percent ÷ 100 using whole-number division (remainder dropped), and `net` = amount − discount. Example: 200 and 15 give discount 30 and net 170.

## Signature

```
INPUTS: amount (String), percent (String)
OUTPUTS: discount (String), net (String)
```

## Solution

1. INVOKE `pub.math:multiplyInts` with num1 = `amount`, num2 = `percent`, giving `prod`.
2. INVOKE `pub.math:divideInts` with num1 = `prod`, num2 = 100 (whole-number division), giving `discount`.
3. INVOKE `pub.math:subtractInts` with num1 = `amount`, num2 = `discount`, giving `net`.

## Package contents

`discount.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/discount/solve/`.

All sample tests and both hidden tests passed on the site.
