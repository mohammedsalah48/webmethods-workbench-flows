# Add a fixed value

Topic: Mapping | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.add_source:solve`)

## Task

Given `id`, return a document `request` with `id` copied from the input and `source` set to `WEB`.

## Signature

```
INPUTS: id (String)
OUTPUTS: request (Document: id, source)
```

## Solution

One MAP step: link id -> request/id, and set request/source = WEB.

## Package contents

`add_source.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/add_source/solve/`.

All sample tests and the hidden test passed on the site.
