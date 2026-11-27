# Remove leading zeros

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.strip_zeros:solve`)

## Task

Given `padded`, a number with zeros in front, return `number` without them. Example: 000420 gives 420. Zeros that are not at the start stay.

## Signature

```
INPUTS: padded (String)
OUTPUTS: number (String)
```

## Solution

One INVOKE of `pub.string:replace` with searchString `^0+(?=\d)`, useRegex true and an empty replaceString: leading zeros are removed only when a digit follows, so an all-zero value keeps one zero.

## Package contents

`strip_zeros.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/strip_zeros/solve/`.

All sample tests and the hidden tests passed on the site.
