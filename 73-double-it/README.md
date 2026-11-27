# Double a number

Topic: Math | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.double_it:solve`)

## Task

Given a whole number `n`, return `doubled` = n × 2.

## Signature

```
INPUTS: n (String)
OUTPUTS: doubled (String)
```

## Solution

One INVOKE of `pub.math:multiplyInts` with num1 = `n` and num2 = 2; value maps to `doubled`.

## Package contents

`double_it.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/double_it/solve/`.

All sample tests and the hidden test passed on the site.
