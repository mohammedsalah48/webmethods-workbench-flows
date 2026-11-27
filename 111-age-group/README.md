# Sort into age groups

Topic: Branching | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.age_group:solve`)

## Task

Given a whole number `age`, return `group`: under 13 is child, 13 to 17 is teen, 18 to 64 is adult, 65 or more is senior.

## Signature

```
INPUTS: age (String)
OUTPUTS: group (String)
```

## Solution

One BRANCH step with evaluated labels, checked in order: `%age% < 13` = child, `%age% >= 13 && %age% <= 17` = teen, `%age% >= 18 && %age% <= 64` = adult, `$default` = senior.

## Package contents

`age_group.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/age_group/solve/`.

All sample tests and all six hidden tests passed on the site.
