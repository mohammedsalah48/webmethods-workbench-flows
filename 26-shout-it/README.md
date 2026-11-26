# Shout it

Topic: Strings | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.shout:solve`)

## Task

Given `text`, return `shout`: the text in upper case followed by !. Example: hello gives HELLO!.

## Signature

```
INPUTS: text (String)
OUTPUTS: shout (String)
```

## Solution

Two INVOKE steps: `pub.string:toUpper` (text to up), then `pub.string:concat` (`%up%` and `!`, value to shout).

## Package contents

`shout.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/shout/solve/`.

All sample tests and the hidden test passed on the site.
