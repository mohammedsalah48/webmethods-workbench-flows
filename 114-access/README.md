# Both conditions must hold

Topic: Branching | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.access:solve`)

## Task

Given `active` and `verified`, each true or false, return `decision`: ALLOW only when both are true, otherwise DENY.

## Signature

```
INPUTS: active (String), verified (String)
OUTPUTS: decision (String)
```

## Solution

One BRANCH step with evaluated labels: `%active% == true && %verified% == true` = ALLOW, `$default` = DENY.

## Package contents

`access.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/access/solve/`.

All sample tests and both hidden tests passed on the site.
