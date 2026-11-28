# Accept digits only

Topic: Validation | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.numeric_only:solve`)

## Task

Given `accountNo`, set `status` to OK when it contains digits only (at least one). Otherwise fail with a message that contains must be numeric.

## Signature

```
INPUTS: accountNo (String)
OUTPUTS: status (String)
```

## Solution

One BRANCH step switched on `accountNo`:

- regex label `/^[0-9]+$/` sets `status` = OK (leading zeros are kept, the value stays a string)
- label `$default` runs an EXIT step signalling FAILURE with the message `must be numeric`

## Package contents

`numeric_only.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/numeric_only/`.

All sample tests and all three hidden tests passed on the site.
