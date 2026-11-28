# FizzBuzz for one number

Topic: Branching | Difficulty: Hard | 40 points | webMethods Workbench flow challenge (`challenge.fizzbuzz:solve`)

## Task

Given a whole number `n` (1 or more), return `result`:

- FizzBuzz when n can be divided by both 3 and 5
- Fizz when it can be divided by 3 only
- Buzz when it can be divided by 5 only
- otherwise the number itself

## Signature

```
INPUTS: n (String)
OUTPUTS: result (String)
```

## Solution

Six INVOKE steps compute the remainders against 3 and 5, then one BRANCH decides:

1. For each divisor d in 3 and 5: `q` = n ÷ d (`pub.math:divideInts`), `m` = q × d (`pub.math:multiplyInts`), `dN` = n − m (`pub.math:subtractInts`), giving `d3` and `d5`.
2. One BRANCH step with evaluated labels:
   - `%d3% == 0 && %d5% == 0` sets `result` = FizzBuzz
   - `%d3% == 0` sets `result` = Fizz
   - `%d5% == 0` sets `result` = Buzz
   - `$default` sets `result` = `%n%` (the number itself, with variable substitution)

## Package contents

`fizzbuzz.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/fizzbuzz/`.

All sample tests and all six hidden tests passed on the site.
