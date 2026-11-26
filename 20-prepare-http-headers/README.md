# Prepare HTTP headers

Topic: Mapping | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.auth_headers:solve`)

## Task

Before calling a REST API you need a `headers` document. Given `token`, return `headers` with Authorization set to Bearer followed by the token, and Accept set to application/json.

## Signature

```
INPUTS: token (String)
OUTPUTS: headers (Document: Authorization, Accept)
```

## Solution

One MAP step: set headers/Authorization to `Bearer %token%` and headers/Accept to `application/json`.

## Package contents

`auth_headers.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/auth_headers/solve/`.

All sample tests and the hidden test passed on the site.
