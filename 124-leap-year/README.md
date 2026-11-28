# Leap year

Topic: Branching | Difficulty: Hard | 40 points | webMethods Workbench flow challenge (`challenge.leap_year:solve`)

## Task

Given `year`, return `leap`: true or false.

A year is a leap year when it can be divided by 4, except years that can be divided by 100, which are leap years only when they can also be divided by 400.

## Signature

```
INPUTS: year (String)
OUTPUTS: leap (String)
```

## Solution

Nine INVOKE steps compute the remainder against 4, 100 and 400, then one BRANCH decides:

1. For each divisor d in 4, 100, 400: `q` = year ÷ d (`pub.math:divideInts`), `m` = q × d (`pub.math:multiplyInts`), `dN` = year − m (`pub.math:subtractInts`), giving `d4`, `d100` and `d400`.
2. One BRANCH step with evaluated labels:
   - `%d4% > 0` sets `leap` = false (not divisible by 4)
   - `%d100% > 0` sets `leap` = true (divisible by 4, not by 100)
   - `%d400% == 0` sets `leap` = true (century divisible by 400)
   - `$default` sets `leap` = false (century not divisible by 400)

## Package contents

`leap_year.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/leap_year/`.

All sample tests and all four hidden tests passed on the site.
