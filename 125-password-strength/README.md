# Rate a password

Topic: Branching | Difficulty: Hard | 40 points | webMethods Workbench flow challenge (`challenge.password_strength:solve`)

## Task

Given `password`, return `strength`:

- strong: 8 or more characters, with at least one digit and at least one upper-case letter
- medium: 8 or more characters, but not strong
- weak: fewer than 8 characters

## Signature

```
INPUTS: password (String)
OUTPUTS: strength (String)
```

## Solution

Seven INVOKE steps measure the password, then one BRANCH decides:

1. `len` = length of `password` (`pub.string:length`).
2. `nd` = `password` with every digit removed (`pub.string:replace`, regex `[0-9]`); `lend` = length of `nd`; `diffD` = `len` − `lend` (`pub.math:subtractInts`), the count of digits.
3. `nu` = `password` with every upper-case letter removed (regex `[A-Z]`); `lenu` = length of `nu`; `diffU` = `len` − `lenu`, the count of upper-case letters.
4. One BRANCH step with evaluated labels:
   - `%len% < 8` sets `strength` = weak
   - `%diffD% > 0 && %diffU% > 0` sets `strength` = strong
   - `$default` sets `strength` = medium

## Package contents

`password_strength.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/password_strength/`.

All sample tests and all five hidden tests passed on the site.
