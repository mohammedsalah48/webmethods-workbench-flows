# Grade a score

Topic: Branching | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.grade:solve`)

## Task

Given a whole number `score`, return `grade`: 90 or more is A, 80 to 89 is B, 70 to 79 is C, below 70 is F.

## Signature

```
INPUTS: score (String)
OUTPUTS: grade (String)
```

## Solution

One BRANCH step with evaluated labels, checked in order: `%score% >= 90` = A, `%score% >= 80` = B, `%score% >= 70` = C, `$default` = F.

## Package contents

`grade.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/grade/solve/`.

All sample tests and all five hidden tests passed on the site.
