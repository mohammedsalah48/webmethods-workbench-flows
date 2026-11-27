# Describe the stock level

Topic: Branching | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.stock_status:solve`)

## Task

Given a whole number `quantity`, return `status`: 0 or less is OUT, 1 to 5 is LOW, more than 5 is OK.

## Signature

```
INPUTS: quantity (String)
OUTPUTS: status (String)
```

## Solution

One BRANCH step with evaluated labels: `%quantity% <= 0` = OUT, `%quantity% >= 1 && %quantity% <= 5` = LOW, `$default` = OK.

## Package contents

`stock_status.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/stock_status/solve/`.

All sample tests and all four hidden tests passed on the site (6 tests total).
