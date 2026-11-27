# Even or odd

Topic: Branching | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.even_odd:solve`)

## Task

Given a whole number `n` (0 or more), return `parity`: even or odd.

## Signature

```
INPUTS: n (String)
OUTPUTS: parity (String)
```

## Solution

1. INVOKE `pub.math:divideInts` with num1 = `n`, num2 = 2, giving `h`.
2. INVOKE `pub.math:multiplyInts` with num1 = `h`, num2 = 2, giving `h2`.
3. INVOKE `pub.math:subtractInts` with num1 = `n`, num2 = `h2`, giving `r` (the remainder: 0 or 1).
4. BRANCH on `r`: label `0` sets `parity` = even, `$default` sets `parity` = odd.

## Package contents

`even_odd.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/even_odd/solve/`.

All sample tests and all three hidden tests passed on the site.
