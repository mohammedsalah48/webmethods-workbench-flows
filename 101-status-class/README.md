# Classify an HTTP status

Topic: Branching | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.status_class:solve`)

## Task

Given an HTTP status `code`, return `result`: 200 to 299 is success, 400 to 499 is client error, 500 to 599 is server error, anything else (including a missing code) is other.

## Signature

```
INPUTS: code (String)
OUTPUTS: result (String)
```

## Solution

One BRANCH step with evaluated labels, checked in order:

- `%code% >= 200 && %code% <= 299` sets `result` = success
- `%code% >= 400 && %code% <= 499` sets `result` = client error
- `%code% >= 500 && %code% <= 599` sets `result` = server error
- `$default` sets `result` = other (a missing code fails every comparison and lands here)

## Package contents

`status_class.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/status_class/solve/`.

All sample tests and all three hidden tests passed on the site.
