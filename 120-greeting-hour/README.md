# Greet by time of day

Topic: Branching | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.greeting_hour:solve`)

## Task

Given `hour` (0 to 23), return `greeting`: before 12 is Good morning, 12 to 17 is Good afternoon, 18 or later is Good evening.

## Signature

```
INPUTS: hour (String)
OUTPUTS: greeting (String)
```

## Solution

One BRANCH step with evaluated labels: `%hour% < 12` = Good morning, `%hour% >= 12 && %hour% <= 17` = Good afternoon, `$default` = Good evening.

## Package contents

`greeting_hour.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/greeting_hour/solve/`.

All sample tests and all five hidden tests passed on the site (7 tests total).
