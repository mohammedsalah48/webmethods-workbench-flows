# Capitalise a word

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.capitalize:solve`)

## Task

Given `word`, return `result`: the first letter in upper case and the rest in lower case. Example: cAIRO gives Cairo.

## Signature

```
INPUTS: word (String)
OUTPUTS: result (String)
```

## Solution

Five INVOKE steps: `pub.string:replace` (searchString `^(.)(.*)$`, replaceString `$1`) takes the first letter, `pub.string:toUpper` upper-cases it, a second `pub.string:replace` (`^.(.*)$` -> `$1`) takes the rest, `pub.string:toLower` lower-cases it, and `pub.string:concat` joins the two into `result`.

## Package contents

`capitalize.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/capitalize/solve/`.

All sample tests and the hidden tests passed on the site.
