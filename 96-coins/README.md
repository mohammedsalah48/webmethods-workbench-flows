# Give change in coins

Topic: Math | Difficulty: Hard | 40 points | webMethods Workbench flow challenge (`challenge.coins:solve`)

## Task

Given a whole number `cents`, give the change with as few coins as possible. Return `quarters` (25), `dimes` (10), `nickels` (5) and `pennies` (1). Example: 68 gives 2 quarters, 1 dime, 1 nickel and 3 pennies.

## Signature

```
INPUTS: cents (String)
OUTPUTS: quarters (String), dimes (String), nickels (String), pennies (String)
```

## Solution

Greedy with whole-number division, subtracting each coin's worth before the next:

1. `quarters` = cents ÷ 25 (`pub.math:divideInts`); `q25` = quarters × 25; `r1` = cents − q25.
2. `dimes` = r1 ÷ 10; `d10` = dimes × 10; `r2` = r1 − d10.
3. `nickels` = r2 ÷ 5; `n5` = nickels × 5; `pennies` = r2 − n5.

Nine INVOKE steps of `pub.math:divideInts`, `pub.math:multiplyInts` and `pub.math:subtractInts`.

## Package contents

`coins.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/coins/solve/`.

All sample tests and all three hidden tests passed on the site.
