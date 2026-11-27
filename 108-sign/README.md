# Sign of a number

Topic: Branching | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.sign:solve`)

## Task

Given a whole number `n`, return `sign`: positive, negative or zero.

## Signature

```
INPUTS: n (String)
OUTPUTS: sign (String)
```

## Solution

One BRANCH step with evaluated labels: `%n% > 0` = positive, `%n% < 0` = negative, `$default` = zero.

## Package contents

`sign.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/sign/solve/`.

All sample tests and all three hidden tests passed on the site.
