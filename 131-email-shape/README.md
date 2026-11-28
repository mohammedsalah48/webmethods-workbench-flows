# Check the shape of an email address

Topic: Validation | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.email_shape:solve`)

## Task

Given `email`, set `status` to OK when it looks like an address: some text, one @, some text, a dot, some text, and no spaces. Otherwise fail with a message that contains invalid email.

## Signature

```
INPUTS: email (String)
OUTPUTS: status (String)
```

## Solution

One BRANCH step switched on `email`:

- regex label `/^[^@\s]+@[^@\s]+\.[^@\s]+$/` (text, one @, text, a dot, text, no spaces) sets `status` = OK
- label `$default` runs an EXIT step signalling FAILURE with the message `invalid email` (also covers a missing value, which no label matches)

## Package contents

`email_shape.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/email_shape/`.

All sample tests and all four hidden tests passed on the site.
