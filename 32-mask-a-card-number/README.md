# Mask a card number

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.mask_card:solve`)

## Task

Given `cardNumber` (digits only, at least 4), return `masked`: the same length, with every character replaced by * except the last four. Example: 1234567812345678 gives ************5678.

## Signature

```
INPUTS: cardNumber (String)
OUTPUTS: masked (String)
```

## Solution

Four INVOKE steps: `pub.string:length` (n), `pub.math:subtractInts` (n minus 4), `pub.string:substring` for the last four characters, then `pub.string:padLeft` of those with `*` to length n.

## Package contents

`mask_card.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/mask_card/solve/`.

All sample tests and the hidden test passed on the site.
