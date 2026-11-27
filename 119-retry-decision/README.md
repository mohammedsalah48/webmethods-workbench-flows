# Decide whether to retry a call

Topic: Branching | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.retry_decision:solve`)

## Task

Given the HTTP `status` of a failed or finished call, return `decision`: any 5xx status, or 429 = RETRY; any other 4xx status = FAIL; any 2xx status = DONE; anything else = UNKNOWN.

## Signature

```
INPUTS: status (String)
OUTPUTS: decision (String)
```

## Solution

One BRANCH step with evaluated labels: `%status% == 429` = RETRY, `%status% >= 500 && %status% <= 599` = RETRY, `%status% >= 400 && %status% <= 499` = FAIL, `%status% >= 200 && %status% <= 299` = DONE, `$default` = UNKNOWN.

## Package contents

`retry_decision.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/retry_decision/solve/`.

All sample tests and all six hidden tests passed on the site (8 tests total).
