# Spot an internal code

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.internal_code:solve`)

## Task

Given `code`, return `internal`: true when the code starts with INT-, otherwise false.

## Signature

```
INPUTS: code (String)
OUTPUTS: internal (String)
```

## Solution

Two INVOKEs of `pub.string:replace`: the first maps any code matching `^INT-.*` to `true`, the second maps anything that is not exactly `true` (`^(?!true$).*$`) to `false`.

## Package contents

`internal_code.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/internal_code/solve/`.

All sample tests and the hidden tests passed on the site.
