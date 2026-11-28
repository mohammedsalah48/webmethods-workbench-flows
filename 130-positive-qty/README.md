# Quantity must be positive

Topic: Validation | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.positive_qty:solve`)

## Task

Given a whole number `quantity`:

- if it is greater than 0, set `status` to OK
- otherwise, or when it is missing, fail with a message that contains quantity must be positive

## Signature

```
INPUTS: quantity (String)
OUTPUTS: status (String)
```

## Solution

Two nested BRANCH steps:

1. The outer BRANCH is switched on `quantity`: labels `$null` and `` (blank) run an EXIT step signalling FAILURE with the message `quantity must be positive`.
2. Label `$default` holds an inner BRANCH with evaluated labels: `%quantity% > 0` sets `status` = OK, and its `$default` runs the same EXIT step (covers zero and negative values).

## Package contents

`positive_qty.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/positive_qty/`.

All sample tests and all three hidden tests passed on the site.
