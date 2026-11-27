# Add two numbers

Topic: Math | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.add_two:solve`)

## Task

Given whole numbers `a` and `b`, return `sum`.

## Signature

```
INPUTS: a (String), b (String)
OUTPUTS: sum (String)
```

## Solution

One INVOKE of `pub.math:addInts` with num1 = `a` and num2 = `b`; value maps to `sum`.

## Package contents

`add_two.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/add_two/solve/`.

All sample tests and the hidden test passed on the site.
