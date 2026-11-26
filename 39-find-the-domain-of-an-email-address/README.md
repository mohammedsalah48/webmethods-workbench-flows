# Find the domain of an email address

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.email_domain:solve`)

## Task

Given `email`, return `domain`: everything after the @. Example: mona@example.com gives example.com.

## Signature

```
INPUTS: email (String)
OUTPUTS: domain (String)
```

## Solution

One INVOKE of `pub.string:tokenize` with delim `@`; valueList[1] is linked to domain.

## Package contents

`email_domain.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/email_domain/solve/`.

All sample tests and the hidden test passed on the site.
