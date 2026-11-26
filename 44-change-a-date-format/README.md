# Change a date format

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.swap_date:solve`)

## Task

Given `isoDate` in the form YYYY-MM-DD, return `localDate` in the form DD/MM/YYYY. Example: 2024-03-15 gives 15/03/2024.

## Signature

```
INPUTS: isoDate (String)
OUTPUTS: localDate (String)
```

## Solution

One INVOKE of `pub.string:replace` with a regex of three captured groups (year, month, day), useRegex true and replaceString `$3/$2/$1`.

## Package contents

`swap_date.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/swap_date/solve/`.

All sample tests and the hidden test passed on the site.
