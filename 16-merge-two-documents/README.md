# Merge two documents

Topic: Mapping | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.merge_docs:solve`)

## Task

Given the documents `billing` (with `name`) and `shipping` (with `city`), return one document `merged` with both `name` and `city`.

## Signature

```
INPUTS: billing (Document: name), shipping (Document: city)
OUTPUTS: merged (Document: name, city)
```

## Solution

One MAP step with two links: billing/name to merged/name and shipping/city to merged/city.

## Package contents

`merge_docs.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/merge_docs/solve/`.

All sample tests and the hidden test passed on the site.
