# Split seconds into minutes and seconds

Topic: Math | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.seconds_split:solve`)

## Task

Given a whole number `seconds`, return `minutes`: the whole minutes, and `rest`: the seconds left over. Example: 135 gives 2 and 15.

## Signature

```
INPUTS: seconds (String)
OUTPUTS: minutes (String), rest (String)
```

## Solution

1. INVOKE `pub.math:divideInts` with num1 = `seconds`, num2 = 60, giving `minutes` (remainder dropped).
2. INVOKE `pub.math:multiplyInts` with num1 = `minutes`, num2 = 60, giving `m`.
3. INVOKE `pub.math:subtractInts` with num1 = `seconds`, num2 = `m`, giving `rest`.

## Package contents

`seconds_split.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/seconds_split/solve/`.

All sample tests and both hidden tests passed on the site.
