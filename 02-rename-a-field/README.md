# Rename a field

Topic: Mapping | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.rename_field:solve`)

## Task

The caller sends `custId` but the next system expects `customerId`. Return `customerId` with the same value.

## Signature

```
INPUTS: custId (String)
OUTPUTS: customerId (String)
```

## Solution

One MAP step with one link: custId -> customerId.

## Package contents

`rename_field.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/rename_field/solve/`.

All sample tests and the hidden test passed on the site.
