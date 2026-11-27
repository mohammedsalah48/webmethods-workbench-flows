# Pull a reference out of a message

Topic: Strings | Difficulty: Hard | 40 points | webMethods Workbench flow challenge (`challenge.bracket_ref:solve`)

## Task

Given `message`, which contains one reference in square brackets, return `ref`: the text between the brackets. Example: Order [A-123] received gives A-123.

## Signature

```
INPUTS: message (String)
OUTPUTS: ref (String)
```

## Solution

One INVOKE of `pub.string:replace` with searchString `^[^[]*\[([^\]]*)\].*$`, useRegex true and replaceString `$1`.

## Package contents

`bracket_ref.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/bracket_ref/solve/`.

All sample tests and the hidden tests passed on the site.
