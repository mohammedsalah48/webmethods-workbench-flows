# Take the prefix of a code

Topic: Strings | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.code_prefix:solve`)

## Task

Given `code` (at least three characters), return `prefix`: its first three characters. Example: EGY-2291 gives EGY.

## Signature

```
INPUTS: code (String)
OUTPUTS: prefix (String)
```

## Solution

One INVOKE of `pub.string:substring` with beginIndex 0 and endIndex 3, value to prefix.

## Package contents

`code_prefix.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/code_prefix/solve/`.

All sample tests and the hidden test passed on the site.
