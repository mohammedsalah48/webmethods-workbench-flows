# Weighted final score

Topic: Math | Difficulty: Hard | 40 points | webMethods Workbench flow challenge (`challenge.weighted_score:solve`)

## Task

Given `exam`, `project` and `quiz` scores, return `final` = exam × 0.5 + project × 0.3 + quiz × 0.2, with exactly one decimal place. Example: 80, 90 and 70 give 81.0.

## Signature

```
INPUTS: exam (String), project (String), quiz (String)
OUTPUTS: final (String)
```

## Solution

1. INVOKE `pub.math:multiplyFloats` on each score with its weight (0.5, 0.3, 0.2), giving `e`, `p`, `q`.
2. INVOKE `pub.math:addFloats` with num1 = `e`, num2 = `p`, giving `ep`.
3. INVOKE `pub.math:addFloats` with num1 = `ep`, num2 = `q`, precision = 1, giving `final`.

## Package contents

`weighted_score.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/weighted_score/solve/`.

All sample tests and both hidden tests passed on the site.
