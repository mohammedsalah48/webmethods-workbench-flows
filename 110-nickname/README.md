# Choose a display name

Topic: Branching | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.nickname:solve`)

## Task

Given `firstName` and an optional `nickname`, return `display`: the nickname when one was sent, otherwise the first name.

## Signature

```
INPUTS: firstName (String), nickname (String)
OUTPUTS: display (String)
```

## Solution

One BRANCH step switched on `nickname` with MAP children: `$null` (and a blank value) sets `display` = `%firstName%`, and `$default` sets `display` = `%nickname%`.

## Package contents

`nickname.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/nickname/solve/`.

All sample tests and both hidden tests passed on the site.
