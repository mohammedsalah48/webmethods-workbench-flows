# Count the separators

Topic: Strings | Difficulty: Hard | 40 points | webMethods Workbench flow challenge (`challenge.count_commas:solve`)

## Task

Given `text`, return `commas`: how many commas it contains. Example: a,b,,c gives 3.

## Signature

```
INPUTS: text (String)
OUTPUTS: commas (String)
```

## Solution

Four INVOKE steps: `pub.string:replace` removes every comma (searchString `,`, empty replaceString, useRegex true), two `pub.string:length` steps measure the original and the stripped text, and `pub.math:subtractInts` returns the difference.

## Package contents

`count_commas.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/count_commas/solve/`.

All sample tests and the hidden tests passed on the site.
