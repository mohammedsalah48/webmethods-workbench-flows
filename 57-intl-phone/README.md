# Convert a phone number to international form

Topic: Strings | Difficulty: Hard | 40 points | webMethods Workbench flow challenge (`challenge.intl_phone:solve`)

## Task

Given `phone`, first remove every character that is not a digit. Then return `intl`: if the digits start with 00, replace those two zeros with +; otherwise, if they start with 0, replace that zero with +20; otherwise put + in front. Example: 0100 123 4567 gives +201001234567.

## Signature

```
INPUTS: phone (String)
OUTPUTS: intl (String)
```

## Solution

Four INVOKEs of `pub.string:replace`: strip `\D` to keep only digits, map `^00` to `+`, map a remaining `^0` to `+20`, then `^(?!\+)` to `+` prefixes a plus only when one is not there yet.

## Package contents

`intl_phone.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/intl_phone/solve/`.

All sample tests and the hidden tests passed on the site.
