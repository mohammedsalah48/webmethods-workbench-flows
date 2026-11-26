# Read the check character

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.last_char:solve`)

## Task

The last character of `reference` is a check character. Return it in `check`. Example: AB-1029-X gives X.

## Signature

```
INPUTS: reference (String)
OUTPUTS: check (String)
```

## Solution

Three INVOKE steps: `pub.string:length` (to n), `pub.math:subtractInts` (n minus 1, to idx), then `pub.string:substring` from `%idx%` to `%n%`.

## Package contents

`last_char.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/last_char/solve/`.

All sample tests and the hidden test passed on the site.
