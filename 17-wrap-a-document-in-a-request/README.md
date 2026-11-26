# Wrap a document in a request

Topic: Mapping | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.wrap_request:solve`)

## Task

Given the document `order`, return a document `request` that holds the whole order under `order` and a field `version` set to 2.

## Signature

```
INPUTS: order (Document: id, total)
OUTPUTS: request (Document: order, version)
```

## Solution

One MAP step: link order to request/order, then set request/version to 2.

## Package contents

`wrap_request.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/wrap_request/solve/`.

All sample tests and the hidden test passed on the site.
