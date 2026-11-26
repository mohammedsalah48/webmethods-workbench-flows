# Find the user part of an email address

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.email_user:solve`)

## Task

Given `email`, return `user`: everything before the @.

## Signature

```
INPUTS: email (String)
OUTPUTS: user (String)
```

## Solution

One INVOKE of `pub.string:tokenize` with delim `@`; valueList[0] is linked to user.

## Package contents

`email_user.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/email_user/solve/`.

All sample tests and the hidden test passed on the site.
