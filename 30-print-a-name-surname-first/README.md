# Print a name surname first

Topic: Strings | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.surname_first:solve`)

## Task

Given `firstName` and `lastName`, return `display`: the last name in upper case, a comma and a space, then the first name. Example: Mona and Adel give ADEL, Mona.

## Signature

```
INPUTS: firstName, lastName (String)
OUTPUTS: display (String)
```

## Solution

Three INVOKE steps: `pub.string:toUpper` on lastName, `pub.string:concat` with `, `, then `pub.string:concat` with `%firstName%`.

## Package contents

`surname_first.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/surname_first/solve/`.

All sample tests and the hidden test passed on the site.
