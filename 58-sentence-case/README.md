# Write a sentence properly

Topic: Strings | Difficulty: Hard | 40 points | webMethods Workbench flow challenge (`challenge.sentence_case:solve`)

## Task

Given `text`, return `sentence`: runs of white space reduced to one space, nothing at the start or end, the first letter in upper case and every other letter in lower case. Example: the ORDER was shipped gives The order was shipped.

## Signature

```
INPUTS: text (String)
OUTPUTS: sentence (String)
```

## Solution

Seven INVOKE steps: `pub.string:replace` (`\s+` to one space), `pub.string:trim`, `pub.string:toLower`, `pub.string:replace` (`^(.).*$` to `$1`) for the first letter, `pub.string:toUpper`, another `pub.string:replace` (`^.(.*)$` to `$1`) for the rest, and `pub.string:concat` joins them.

## Package contents

`sentence_case.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/sentence_case/solve/`.

All sample tests and the hidden tests passed on the site.
