# Remove the digits

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.remove_digits:solve`)

## Task

Given `text`, return `letters`: the text with every digit removed. Example: a1b22c gives abc.

## Signature

```
INPUTS: text (String)
OUTPUTS: letters (String)
```

## Solution

One INVOKE of `pub.string:replace` with searchString `[0-9]`, useRegex true and an empty replaceString.

## Package contents

`remove_digits.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/remove_digits/solve/`.

All sample tests and the hidden test passed on the site.
