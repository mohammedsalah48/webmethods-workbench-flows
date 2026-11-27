# Convert a currency amount

Topic: Math | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.convert_currency:solve`)

## Task

Given `amount` and `rate`, return `converted` = amount × rate with exactly two decimal places. Example: 100 and 30.9 give 3090.00.

## Signature

```
INPUTS: amount (String), rate (String)
OUTPUTS: converted (String)
```

## Solution

One INVOKE of `pub.math:multiplyFloats` with num1 = `amount`, num2 = `rate` and precision = 2 (the service formats the result with two decimals); value maps to `converted`.

## Package contents

`convert_currency.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/convert_currency/solve/`.

All sample tests and the hidden test passed on the site.
