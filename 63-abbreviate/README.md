# Abbreviate a name

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.abbreviate:solve`)

## Task

Given `name`, several words, return `abbr`: the first letter of every word, in upper case. Example: Integration Server gives IS.

## Signature

```
INPUTS: name (String)
OUTPUTS: abbr (String)
```

## Solution

Two INVOKE steps: `pub.string:replace` with searchString `\s*(\w)\w*`, useRegex true and replaceString `$1` keeps the first letter of every word, then `pub.string:toUpper`.

## Package contents

`abbreviate.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/abbreviate/solve/`.

All sample tests and the hidden tests passed on the site.
