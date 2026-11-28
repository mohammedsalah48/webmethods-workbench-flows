# Limit the length of a comment

Topic: Validation | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.max_length:solve`)

## Task

Given `comment`, return its `length`. If the comment is longer than 20 characters, fail with a message that contains comment is too long.

## Signature

```
INPUTS: comment (String)
OUTPUTS: length (String)
```

## Solution

1. INVOKE `pub.string:length` on `comment`, giving `len`.
2. One BRANCH step with evaluated labels:
   - `%len% > 20` runs an EXIT step signalling FAILURE with the message `comment is too long`
   - `$default` sets `length` = `%len%` (variable substitution)

## Package contents

`max_length.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/max_length/`.

All sample tests and both hidden tests passed on the site.
