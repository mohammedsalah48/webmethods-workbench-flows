# Read a yes/no answer

Topic: Branching | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.truthy:solve`)

## Task

Different systems send yes in different ways. Given `answer`, return `flag`: true when the answer, ignoring case and surrounding spaces, is yes, y, true or 1. Otherwise false.

## Signature

```
INPUTS: answer (String)
OUTPUTS: flag (String)
```

## Solution

1. INVOKE `pub.string:trim` on `answer`, giving `t`, dropping the surrounding spaces.
2. INVOKE `pub.string:toLower` on `t`, giving `low`, so the comparison ignores case.
3. One BRANCH step switched on `low` with five MAP children:
   - labels `yes`, `y`, `true` and `1` each set `flag` = true
   - label `$default` sets `flag` = false

## Package contents

`truthy.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/truthy/`.

All sample tests and all five hidden tests passed on the site.
