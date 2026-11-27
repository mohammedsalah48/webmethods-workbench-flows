# Weekend or weekday

Topic: Branching | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.weekend:solve`)

## Task

Given `day` as a three-letter code (MON to SUN), return `type`: weekend for SAT and SUN, otherwise weekday.

## Signature

```
INPUTS: day (String)
OUTPUTS: type (String)
```

## Solution

One BRANCH step switched on `day` with MAP children: labels `SAT` and `SUN` set `type` = weekend, `$default` sets `type` = weekday.

## Package contents

`weekend.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/weekend/solve/`.

All sample tests and both hidden tests passed on the site.
