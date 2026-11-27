# Show minutes as a clock time

Topic: Math | Difficulty: Hard | 40 points | webMethods Workbench flow challenge (`challenge.hhmm:solve`)

## Task

Given a whole number `minutes` (0 to 1439), return `time` in the form HH:MM, each part two digits. Example: 135 gives 02:15.

## Signature

```
INPUTS: minutes (String)
OUTPUTS: time (String)
```

## Solution

1. INVOKE `pub.math:divideInts` with num1 = `minutes`, num2 = 60, giving `h`.
2. INVOKE `pub.math:multiplyInts` with num1 = `h`, num2 = 60, giving `hm`.
3. INVOKE `pub.math:subtractInts` with num1 = `minutes`, num2 = `hm`, giving `m`.
4. INVOKE `pub.string:padLeft` on `h` with length 2, padString `0`, giving `hh`.
5. INVOKE `pub.string:padLeft` on `m` with length 2, padString `0`, giving `mm`.
6. INVOKE `pub.string:concat` with inString1 `%hh%` and inString2 `:%mm%` (variable substitution), giving `time`.

## Package contents

`hhmm.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/hhmm/solve/`.

All sample tests and both hidden tests passed on the site.
