# Clean an email address

Topic: Strings | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.clean_email:solve`)

## Task

Given `email`, return `clean`: the address with surrounding white space removed and all letters in lower case.

## Signature

```
INPUTS: email (String)
OUTPUTS: clean (String)
```

## Solution

Two INVOKE steps: `pub.string:trim` then `pub.string:toLower`, value to clean.

## Package contents

`clean_email.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/clean_email/solve/`.

All sample tests and the hidden test passed on the site.
