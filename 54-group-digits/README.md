# Print a card number in groups

Topic: Strings | Difficulty: Hard | 40 points | webMethods Workbench flow challenge (`challenge.group_digits:solve`)

## Task

Given `number` (digits only), return `grouped`: the digits in groups of four separated by single spaces. The last group may be shorter, and there is no space at the end. Example: 1234567812345678 gives 1234 5678 1234 5678.

## Signature

```
INPUTS: number (String)
OUTPUTS: grouped (String)
```

## Solution

One INVOKE of `pub.string:replace` with searchString `(\d{4})(?=\d)`, useRegex true and replaceString `$1 ` (a space after every four digits that are followed by more digits, so no trailing space).

## Package contents

`group_digits.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/group_digits/solve/`.

All sample tests and the hidden tests passed on the site.
