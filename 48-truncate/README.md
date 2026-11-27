# Shorten a long text

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.truncate:solve`)

## Task

Given `text`, return `short`: if the text is longer than 10 characters, its first 10 characters followed by `...`; otherwise the text unchanged.

## Signature

```
INPUTS: text (String)
OUTPUTS: short (String)
```

## Solution

One INVOKE of `pub.string:replace` with searchString `^(.{10}).+$`, useRegex true and replaceString `$1...`. Texts of ten characters or fewer do not match and pass through unchanged.

## Package contents

`truncate.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/truncate/solve/`.

All sample tests and the hidden tests passed on the site.
