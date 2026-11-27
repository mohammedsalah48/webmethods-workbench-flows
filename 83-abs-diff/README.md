# Distance between two numbers

Topic: Math | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.abs_diff:solve`)

## Task

Given whole numbers `a` and `b`, return `distance`: how far apart they are. The result is never negative. Example: 3 and 10 give 7; 10 and 3 also give 7.

## Signature

```
INPUTS: a (String), b (String)
OUTPUTS: distance (String)
```

## Solution

1. INVOKE `pub.math:subtractInts` with num1 = `a`, num2 = `b`, giving `d`.
2. INVOKE `pub.math:absoluteValue` with num = `d`; positiveNumber maps to `distance`.

## Package contents

`abs_diff.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/abs_diff/solve/`.

All sample tests and both hidden tests passed on the site.
