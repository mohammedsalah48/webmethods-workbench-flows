# Wrap a payload in an envelope

Topic: Mapping | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.envelope:solve`)

## Task

Given `id` and the document `payload`, return a document `envelope` with meta/id copied from id, meta/source set to IS, and body holding the whole payload.

## Signature

```
INPUTS: id (String), payload (Document: type, value)
OUTPUTS: envelope (Document: meta (id, source), body (type, value))
```

## Solution

One MAP step: link id to envelope/meta/id, set envelope/meta/source to IS, link payload to envelope/body.

## Package contents

`envelope.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/envelope/solve/`.

All sample tests and the hidden test passed on the site.
