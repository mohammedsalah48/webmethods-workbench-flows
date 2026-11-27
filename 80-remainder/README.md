# Find the remainder

Topic: Math | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.remainder:solve`)

## Task

Given positive whole numbers `a` and `b`, return `remainder`: what is left over when a is divided by b. Example: 17 and 5 give 2.

## Signature

```
INPUTS: a (String), b (String)
OUTPUTS: remainder (String)
```

## Solution

There is no modulo service, so the flow computes a − (a ÷ b) × b with whole-number division:

1. INVOKE `pub.math:divideInts` with num1 = `a`, num2 = `b`, giving `q` (remainder dropped).
2. INVOKE `pub.math:multiplyInts` with num1 = `q`, num2 = `b`, giving `qb`.
3. INVOKE `pub.math:subtractInts` with num1 = `a`, num2 = `qb`, giving `remainder`.

## Package contents

`remainder.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/remainder/solve/`.

All sample tests and both hidden tests passed on the site.
