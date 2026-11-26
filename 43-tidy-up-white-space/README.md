# Tidy up white space

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.collapse_spaces:solve`)

## Task

Given `text`, return `clean`: runs of white space replaced by a single space, with nothing at the start or the end.

## Signature

```
INPUTS: text (String)
OUTPUTS: clean (String)
```

## Solution

Two INVOKE steps: `pub.string:replace` with searchString `\s+`, useRegex true and replaceString a single space, then `pub.string:trim`.

## Package contents

`collapse_spaces.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/collapse_spaces/solve/`.

All sample tests and the hidden test passed on the site.
