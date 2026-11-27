# Check a range

Topic: Branching | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.in_range:solve`)

## Task

Given a whole number `value`, return `inRange`: true when it is from 1 to 100 inclusive, otherwise false.

## Signature

```
INPUTS: value (String)
OUTPUTS: inRange (String)
```

## Solution

One BRANCH step with evaluated labels: `%value% >= 1 && %value% <= 100` = true, `$default` = false.

## Package contents

`in_range.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/in_range/solve/`.

All sample tests and all four hidden tests passed on the site (6 tests total).
