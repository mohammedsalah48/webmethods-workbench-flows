# Choose a shipping band

Topic: Branching | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.shipping_band:solve`)

## Task

Given a whole-number order `amount`, return `shipping`: 1000 or more is FREE, 500 to 999 is REDUCED, below 500 is STANDARD.

## Signature

```
INPUTS: amount (String)
OUTPUTS: shipping (String)
```

## Solution

One BRANCH step with evaluate-labels on and three MAP children, checked in order:

- label `%amount% >= 1000` sets `shipping` = FREE
- label `%amount% >= 500` sets `shipping` = REDUCED
- label `$default` sets `shipping` = STANDARD

## Package contents

`shipping_band.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/shipping_band/solve/`.

All sample tests and all three hidden tests passed on the site.
