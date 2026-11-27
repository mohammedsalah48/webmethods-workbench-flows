# Translate a status code

Topic: Branching | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.status_text:solve`)

## Task

Given `status`, return `message`: A gives Active, S gives Suspended, no status at all (null) gives Unknown, anything else gives Invalid.

## Signature

```
INPUTS: status (String)
OUTPUTS: message (String)
```

## Solution

One BRANCH step switched on `status` with four MAP children:

- label `A` sets `message` = Active
- label `S` sets `message` = Suspended
- label `$null` sets `message` = Unknown
- label `$default` sets `message` = Invalid

## Package contents

`status_text.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/status_text/solve/`.

All sample tests and both hidden tests passed on the site.
