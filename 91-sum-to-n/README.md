# Add the numbers from 1 to n

Topic: Math | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.sum_to_n:solve`)

## Task

Given a whole number `n` (1 or more), return `sum`: 1 + 2 + … + n. Example: 4 gives 10. No loop needed.

## Signature

```
INPUTS: n (String)
OUTPUTS: sum (String)
```

## Solution

Uses the formula n × (n + 1) ÷ 2:

1. INVOKE `pub.math:addInts` with num1 = `n`, num2 = 1, giving `n1`.
2. INVOKE `pub.math:multiplyInts` with num1 = `n`, num2 = `n1`, giving `p`.
3. INVOKE `pub.math:divideInts` with num1 = `p`, num2 = 2, giving `sum`.

## Package contents

`sum_to_n.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/sum_to_n/solve/`.

All sample tests and both hidden tests passed on the site.
