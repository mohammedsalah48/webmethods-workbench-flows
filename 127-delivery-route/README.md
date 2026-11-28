# Choose a delivery route

Topic: Branching | Difficulty: Hard | 40 points | webMethods Workbench flow challenge (`challenge.delivery_route:solve`)

## Task

Given `country` and a whole number `weight` in kilograms, return `route`:

- outside EG: INTERNATIONAL
- inside EG, more than 20 kg: FREIGHT
- inside EG, 20 kg or less: COURIER

## Signature

```
INPUTS: country (String), weight (String)
OUTPUTS: route (String)
```

## Solution

Two nested BRANCH steps:

1. The outer BRANCH is switched on `country`:
   - label `EG` holds an inner BRANCH with evaluated labels: `%weight% > 20` sets `route` = FREIGHT, `$default` sets `route` = COURIER
   - label `$default` sets `route` = INTERNATIONAL

## Package contents

`delivery_route.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/delivery_route/`.

All sample tests and all four hidden tests passed on the site.
