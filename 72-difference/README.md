# Stock after a sale

Topic: Math | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.difference:solve`)

## Task

Given whole numbers `inStock` and `sold`, return `remaining` = in stock − sold.

## Signature

```
INPUTS: inStock (String), sold (String)
OUTPUTS: remaining (String)
```

## Solution

One INVOKE of `pub.math:subtractInts` with num1 = `inStock` and num2 = `sold`; value maps to `remaining`.

## Package contents

`difference.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/difference/solve/`.

All sample tests and the hidden test passed on the site.
