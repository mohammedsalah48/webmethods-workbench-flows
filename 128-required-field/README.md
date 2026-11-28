# Reject a missing customer ID

Topic: Validation | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.required_field:solve`)

## Task

Validate the input before doing any work.

If `customerId` is missing or empty, the service must fail with a message that contains customerId is required. Otherwise set `status` to OK.

## Signature

```
INPUTS: customerId (String)
OUTPUTS: status (String)
```

## Solution

One BRANCH step switched on `customerId`:

- label `$null` runs an EXIT step that signals FAILURE with the message `customerId is required`
- label `` (blank) runs the same EXIT step
- label `$default` sets `status` = OK

## Package contents

`required_field.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/required_field/`.

All sample tests and both hidden tests passed on the site.
