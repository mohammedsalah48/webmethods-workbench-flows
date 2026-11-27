# Try one way, then another

Topic: Flow control | Difficulty: Hard | 40 points | webMethods Workbench flow challenge (`challenge.fallback_format:solve`)

## Task

Given `payload`: when it is JSON, return `format` = json and `name` from the field name of the JSON; otherwise return `format` = text and `name` = the payload itself. The service must not fail.

## Signature

```
INPUTS: payload (String)
OUTPUTS: format (String), name (String)
```

## Solution

One SEQUENCE step with exit on SUCCESS and two children:

1. INVOKE `pub.json:jsonStringToDocument` with jsonString = `payload`. On success it sets `format` = json and links `document/name` to `name` (the sim uses IData slash paths). On a non-JSON payload the service throws a ServiceException, so this child fails and the sequence tries the next one.
2. MAP (fallback) sets `format` = text and `name` = `%payload%`.

Because the sequence exits on SUCCESS, a successful parse skips the fallback; a failed parse runs it, so the service never fails.

## Package contents

`fallback_format.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/fallback_format/solve/`.

All sample tests and both hidden tests passed on the site.
