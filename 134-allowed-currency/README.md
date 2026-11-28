# Accept known currencies only

Topic: Validation | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.allowed_currency:solve`)

## Task

Given `currency`, set `status` to OK for USD, EUR or EGP. For anything else fail with the message unsupported currency: followed by the value that was sent.

## Signature

```
INPUTS: currency (String)
OUTPUTS: status (String)
```

## Solution

One BRANCH step switched on `currency`:

- labels `USD`, `EUR` and `EGP` each set `status` = OK
- label `$default` runs an EXIT step signalling FAILURE with the message `unsupported currency: %currency%` (the message substitutes the value that was sent)

## Package contents

`allowed_currency.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/allowed_currency/`.

All sample tests and all three hidden tests passed on the site.
