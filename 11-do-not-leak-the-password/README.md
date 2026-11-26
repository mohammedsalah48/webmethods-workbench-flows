# Do not leak the password

Topic: Mapping | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.drop_secret:solve`)

## Task

The service receives `user` and `password`. Return `user` unchanged.

Extra rule: when the service ends, `user` must be the only variable in the pipeline.

## Signature

```
INPUTS: user (String), password (String)
OUTPUTS: user (String)
```

## Solution

One MAP step that drops `password`; `user` passes through unchanged.

## Package contents

`drop_secret.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/drop_secret/solve/`.

All sample tests and the hidden test passed on the site.
