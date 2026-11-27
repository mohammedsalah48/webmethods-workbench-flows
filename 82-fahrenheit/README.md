# Convert Celsius to Fahrenheit

Topic: Math | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.fahrenheit:solve`)

## Task

Given `celsius`, return `fahrenheit` = celsius × 1.8 + 32, with exactly one decimal place. Example: 100 gives 212.0.

## Signature

```
INPUTS: celsius (String)
OUTPUTS: fahrenheit (String)
```

## Solution

1. INVOKE `pub.math:multiplyFloats` with num1 = `celsius`, num2 = 1.8, precision = 1, giving `t`.
2. INVOKE `pub.math:addFloats` with num1 = `t`, num2 = 32, precision = 1, giving `fahrenheit`.

## Package contents

`fahrenheit.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/fahrenheit/solve/`.

All sample tests and both hidden tests passed on the site.
