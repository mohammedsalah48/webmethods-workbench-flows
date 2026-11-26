# Build initials

Topic: Strings | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.initials:solve`)

## Task

Given `firstName` and `lastName`, return `initials`: the first letter of each, in upper case, with nothing between them. Example: mona and adel give MA.

## Signature

```
INPUTS: firstName, lastName (String)
OUTPUTS: initials (String)
```

## Solution

Four INVOKE steps: `pub.string:substring` (0 to 1) on each name, `pub.string:concat` of the two letters, then `pub.string:toUpper` into initials.

## Package contents

`initials.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/initials/solve/`.

All sample tests and the hidden test passed on the site.
