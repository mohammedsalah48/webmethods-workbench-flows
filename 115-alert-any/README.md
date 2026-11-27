# Either condition raises an alert

Topic: Branching | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.alert_any:solve`)

## Task

Given whole numbers `cpu` and `memory` (percent used), return `state`: ALERT when either is above 90, otherwise OK.

## Signature

```
INPUTS: cpu (String), memory (String)
OUTPUTS: state (String)
```

## Solution

One BRANCH step with evaluated labels: `%cpu% > 90 || %memory% > 90` = ALERT, `$default` = OK.

## Package contents

`alert_any.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/alert_any/solve/`.

All sample tests and all three hidden tests passed on the site.
