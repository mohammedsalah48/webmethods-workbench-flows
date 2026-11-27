# Pay with overtime

Topic: Math | Difficulty: Hard | 40 points | webMethods Workbench flow challenge (`challenge.overtime_pay:solve`)

## Task

Given whole numbers `hours` and `rate`, return `pay`: up to 40 hours, hours × rate; above 40, 40 × rate plus the extra hours at twice the rate. Example: 45 hours at 10 gives 400 + 5 × 20 = 500.

## Signature

```
INPUTS: hours (String), rate (String)
OUTPUTS: pay (String)
```

## Solution

Branch-free: pay = hours × rate + max(hours − 40, 0) × rate (the extra hours add one more rate on top of the base rate already paid for every hour).

1. INVOKE `pub.math:subtractInts` with num1 = `hours`, num2 = 40, giving `h40`.
2. INVOKE `pub.list:appendToStringList` with fromItem = `h40`, giving list `l1`.
3. INVOKE `pub.list:appendToStringList` with toList = `l1`, fromItem = 0, giving list `l2`.
4. INVOKE `pub.math:max` with numList = `l2`; maxValue maps to `extra` (negative overage becomes 0).
5. INVOKE `pub.math:multiplyInts` with num1 = `hours`, num2 = `rate`, giving `base`.
6. INVOKE `pub.math:multiplyInts` with num1 = `extra`, num2 = `rate`, giving `ot`.
7. INVOKE `pub.math:addInts` with num1 = `base`, num2 = `ot`, giving `pay`.

## Package contents

`overtime_pay.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/overtime_pay/solve/`.

All sample tests and all three hidden tests passed on the site.
