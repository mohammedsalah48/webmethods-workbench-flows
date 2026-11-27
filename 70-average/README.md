# Average of a list

Topic: Math | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.average:solve`)

## Task

Given `numbers` (String List of whole numbers, never empty), return `average` with exactly two decimal places. Example: [1, 2, 3, 4] gives 2.50.

## Signature

```
INPUTS: numbers (String List)
OUTPUTS: average (String)
```

## Solution

1. INVOKE `pub.math:addIntList` with numList = `numbers`, giving `sum`.
2. INVOKE `pub.list:sizeOfList` with fromList = `numbers`, giving `count`.
3. INVOKE `pub.math:divideFloats` with num1 = `sum`, num2 = `count`, giving `avgF`.
4. INVOKE `pub.math:multiplyFloats` with num1 = `avgF`, num2 = 100, giving `cents`.
5. INVOKE `pub.math:roundNumber` with num = `cents`, numberOfDigits = 0, giving `c` (the average in cents, rounded).
6. INVOKE `pub.string:replace` with searchString `^(\d+)(\d\d)$`, replaceString `$1.$2`, useRegex true, inserting the decimal point for exactly two places.

## Package contents

`average.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/average/solve/`.

All sample tests and both hidden tests passed on the site.
