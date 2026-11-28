# Two required fields

Topic: Validation | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.require_two:solve`)

## Task

Both `name` and `email` are required.

If name is missing, fail with a message that contains name is required. Otherwise, if email is missing, fail with a message that contains email is required. Otherwise set `status` to OK.

## Signature

```
INPUTS: name (String), email (String)
OUTPUTS: status (String)
```

## Solution

Two nested BRANCH steps:

1. The outer BRANCH is switched on `name`: labels `$null` and `` (blank) run an EXIT step signalling FAILURE with the message `name is required`.
2. Label `$default` holds an inner BRANCH switched on `email`: labels `$null` and `` (blank) run an EXIT step signalling FAILURE with the message `email is required`, and its `$default` sets `status` = OK.

## Package contents

`require_two.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/require_two/`.

All sample tests and both hidden tests passed on the site.
