# Split a key and its value

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.key_value:solve`)

## Task

Given `pair` in the form key=value, return `key` and `val`. Example: colour=blue gives colour and blue.

## Signature

```
INPUTS: pair (String)
OUTPUTS: key, val (String)
```

## Solution

Two INVOKEs of `pub.string:replace`: `^([^=]*)=.*$` to `$1` keeps the part before the first equals sign, and `^[^=]*=` to an empty string keeps the part after it.

## Package contents

`key_value.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/key_value/solve/`.

All sample tests and the hidden tests passed on the site.
