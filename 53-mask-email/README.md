# Mask an email address

Topic: Strings | Difficulty: Hard | 40 points | webMethods Workbench flow challenge (`challenge.mask_email:solve`)

## Task

Given `email`, return `masked`: the first character of the user part, then `***`, then the @ and the domain unchanged. Example: mona@example.com gives m***@example.com.

## Signature

```
INPUTS: email (String)
OUTPUTS: masked (String)
```

## Solution

One INVOKE of `pub.string:replace` with searchString `^(.).*(@.*)$`, useRegex true and replaceString `$1***$2`.

## Package contents

`mask_email.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/mask_email/solve/`.

All sample tests and the hidden tests passed on the site.
