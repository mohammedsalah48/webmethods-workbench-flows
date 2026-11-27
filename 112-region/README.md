# Find the sales region

Topic: Branching | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.region:solve`)

## Task

Given a two-letter country code, return `region`: EG, SA, AE give MEA; DE, FR, IT give EU; US, CA give NA; anything else gives OTHER.

## Signature

```
INPUTS: country (String)
OUTPUTS: region (String)
```

## Solution

One BRANCH step switched on `country` with one MAP child per code (EG/SA/AE = MEA, DE/FR/IT = EU, US/CA = NA) and `$default` = OTHER.

## Package contents

`region.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/region/solve/`.

All sample tests and all six hidden tests passed on the site.
