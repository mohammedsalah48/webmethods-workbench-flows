# Translate a flag

Topic: Branching | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.yes_no:solve`)

## Task

Given `flag`, return `answer`: Y gives true, N gives false, anything else gives unknown.

## Signature

```
INPUTS: flag (String)
OUTPUTS: answer (String)
```

## Solution

One BRANCH step switched on `flag` with MAP children: label `Y` sets `answer` = true, label `N` sets `answer` = false, `$default` sets `answer` = unknown.

## Package contents

`yes_no.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/yes_no/solve/`.

All sample tests and both hidden tests passed on the site.
