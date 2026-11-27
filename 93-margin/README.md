# Profit margin

Topic: Math | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.margin:solve`)

## Task

Given `price` and `cost`, return `margin`: (price − cost) ÷ price × 100, with exactly one decimal place. Example: 200 and 150 give 25.0.

## Signature

```
INPUTS: price (String), cost (String)
OUTPUTS: margin (String)
```

## Solution

1. INVOKE `pub.math:subtractFloats` with num1 = `price`, num2 = `cost`, giving `d`.
2. INVOKE `pub.math:divideFloats` with num1 = `d`, num2 = `price`, giving `r`.
3. INVOKE `pub.math:multiplyFloats` with num1 = `r`, num2 = 100, precision = 1, giving `margin`.

## Package contents

`margin.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/margin/solve/`.

All sample tests and both hidden tests passed on the site.
