# Fill in a default

Topic: Branching | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.default_currency:solve`)

## Task

The input `currency` is optional. Return `currency`: the value sent, or USD when nothing was sent.

## Signature

```
INPUTS: currency (String)
OUTPUTS: currency (String)
```

## Solution

One BRANCH step switched on `currency` with MAP children: label `$null` sets `currency` = USD, and `$default` sets `currency` = `%currency%` (the value that was sent).

## Package contents

`default_currency.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/default_currency/solve/`.

All sample tests and the hidden test passed on the site.
