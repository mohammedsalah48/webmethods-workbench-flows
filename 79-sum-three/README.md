# Add three numbers

Topic: Math | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.sum_three:solve`)

## Task

Given whole numbers `a`, `b` and `c`, return `sum`.

## Signature

```
INPUTS: a (String), b (String), c (String)
OUTPUTS: sum (String)
```

## Solution

1. INVOKE `pub.math:addInts` with num1 = `a`, num2 = `b`, giving `s`.
2. INVOKE `pub.math:addInts` with num1 = `s`, num2 = `c`, giving `sum`.

## Package contents

`sum_three.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/sum_three/solve/`.

All sample tests and the hidden test passed on the site.
