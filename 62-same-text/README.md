# Compare two values loosely

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.same_text:solve`)

## Task

Given `a` and `b`, return `same`: true when they are equal after ignoring upper and lower case and surrounding white space, otherwise false.

## Signature

```
INPUTS: a, b (String)
OUTPUTS: same (String)
```

## Solution

Six INVOKE steps: `pub.string:trim` and `pub.string:toLower` normalise each side, `pub.string:replace` with searchString `^%b2%$` (the normalised b substituted in) maps a match to `true`, and a final `pub.string:replace` (`^(?!true$).*$`) maps anything else to `false`.

## Package contents

`same_text.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/same_text/solve/`.

All sample tests and the hidden tests passed on the site.
