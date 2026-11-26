# Normalise a product code

Topic: Strings | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.normalise_code:solve`)

## Task

Product codes arrive with stray spaces and mixed case. Given `code`, return `cleanCode`: the same text with leading and trailing white space removed and all letters in upper case.

## Signature

```
INPUTS: code (String)
OUTPUTS: cleanCode (String)
```

## Solution

Two INVOKE steps: `pub.string:trim` (code to inString, value to cleanCode), then `pub.string:toUpper` (cleanCode to inString, value to cleanCode).

## Package contents

`normalise_code.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/normalise_code/solve/`.

All sample tests and the hidden test passed on the site.
