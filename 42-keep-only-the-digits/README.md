# Keep only the digits

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.digits_only:solve`)

## Task

Phone numbers arrive with spaces, dashes and brackets. Given `phone`, return `digits`: only the digits, in the same order.

## Signature

```
INPUTS: phone (String)
OUTPUTS: digits (String)
```

## Solution

One INVOKE of `pub.string:replace` with searchString `[^0-9]`, useRegex true and an empty replaceString.

## Package contents

`digits_only.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/digits_only/solve/`.

All sample tests and the hidden test passed on the site.
