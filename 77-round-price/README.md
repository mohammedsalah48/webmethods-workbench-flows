# Round a price

Topic: Math | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.round_price:solve`)

## Task

Given `price`, return `rounded`: the price rounded to exactly two decimal places. Example: 19.987 gives 19.99 and 5 gives 5.00.

## Signature

```
INPUTS: price (String)
OUTPUTS: rounded (String)
```

## Solution

One INVOKE of `pub.math:roundNumber` with num = `price` and numberOfDigits = 2 (the service formats with `toFixed`, so the result always has exactly two decimals); roundedNumber maps to `rounded`.

## Package contents

`round_price.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/round_price/solve/`.

All sample tests and both hidden tests passed on the site.
