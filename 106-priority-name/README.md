# Name a priority

Topic: Branching | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.priority_name:solve`)

## Task

Given `priority`, return `name`: 1 gives High, 2 gives Normal, 3 gives Low. Anything else, or no value, gives Normal.

## Signature

```
INPUTS: priority (String)
OUTPUTS: name (String)
```

## Solution

One BRANCH step switched on `priority` with MAP children: `1` = High, `2` = Normal, `3` = Low, `$default` = Normal (covers everything else and a missing value).

## Package contents

`priority_name.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/priority_name/solve/`.

All sample tests and all three hidden tests passed on the site.
