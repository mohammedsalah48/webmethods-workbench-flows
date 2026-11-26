# Replace spaces with dashes

Topic: Strings | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.dashes_for_spaces:solve`)

## Task

Given `title`, return `dashed`: the same text with every space replaced by -.

## Signature

```
INPUTS: title (String)
OUTPUTS: dashed (String)
```

## Solution

One INVOKE of `pub.string:replace` with searchString a space and replaceString `-`.

## Package contents

`dashes_for_spaces.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/dashes_for_spaces/solve/`.

All sample tests and the hidden test passed on the site.
