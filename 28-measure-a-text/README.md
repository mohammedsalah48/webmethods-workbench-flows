# Measure a text

Topic: Strings | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.text_length:solve`)

## Task

Given `text`, return `size`: the number of characters in it.

## Signature

```
INPUTS: text (String)
OUTPUTS: size (String)
```

## Solution

One INVOKE of `pub.string:length` (text to inString, value to size).

## Package contents

`text_length.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/text_length/solve/`.

All sample tests and the hidden test passed on the site.
