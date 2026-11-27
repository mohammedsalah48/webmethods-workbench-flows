# Compare two numbers

Topic: Branching | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.compare_two:solve`)

## Task

Given whole numbers `a` and `b`, return `result`: greater when `a` is larger than `b`, less when it is smaller, equal when they are the same.

## Signature

```
INPUTS: a (String), b (String)
OUTPUTS: result (String)
```

## Solution

One BRANCH step with evaluated labels: `%a% > %b%` = greater, `%a% < %b%` = less, `$default` = equal.

## Package contents

`compare_two.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/compare_two/solve/`.

All sample tests and all three hidden tests passed on the site (5 tests total).
