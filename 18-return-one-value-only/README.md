# Return one value only

Topic: Mapping | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.keep_one:solve`)

## Task

The service receives `a`, `b`, `c` and `d`. Return `result` with the value of `b`. Extra rule: `result` must be the only variable left in the pipeline.

## Signature

```
INPUTS: a, b, c, d (String)
OUTPUTS: result (String)
```

## Solution

One MAP step: link b to result, then drop a, b, c and d.

## Package contents

`keep_one.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/keep_one/solve/`.

All sample tests and the hidden test passed on the site.
