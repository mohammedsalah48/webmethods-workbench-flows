# Tax in bands

Topic: Math | Difficulty: Hard | 40 points | webMethods Workbench flow challenge (`challenge.tax_bands:solve`)

## Task

Given a whole number `income`, return `tax`, using whole-number division: the first 1000 is free, income above 1000 and up to 5000 is taxed at 10%, income above 5000 at 20%. Example: 3000 gives 200; 6000 gives 400 + 200 = 600.

## Signature

```
INPUTS: income (String)
OUTPUTS: tax (String)
```

## Solution

tax = min(max(income − 1000, 0), 4000) × 10 ÷ 100 + max(income − 5000, 0) × 20 ÷ 100, built from `pub.math:subtractInts`, `pub.list:appendToStringList` (to build two-element lists), `pub.math:max` / `pub.math:min` (clamp the bands), `pub.math:multiplyInts`, `pub.math:divideInts` and `pub.math:addInts`. Each fresh list first clears the pipeline `toList` variable, which otherwise leaks between steps.

## Package contents

`tax_bands.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/tax_bands/solve/`.

All sample tests and all four hidden tests passed on the site.
