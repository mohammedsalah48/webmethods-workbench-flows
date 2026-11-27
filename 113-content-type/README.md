# Route by content type

Topic: Branching | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.content_type:solve`)

## Task

Given the `contentType` header of a request, return `format`: JSON when the header contains json, XML when it contains xml, otherwise OTHER. Example: application/json; charset=utf-8 gives JSON.

## Signature

```
INPUTS: contentType (String)
OUTPUTS: format (String)
```

## Solution

One BRANCH step switched on `contentType` with regex labels: `/[Jj][Ss][Oo][Nn]/` = JSON, `/[Xx][Mm][Ll]/` = XML (case-insensitive without needing flags), `$default` = OTHER.

## Package contents

`content_type.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/content_type/solve/`.

All sample tests and all three hidden tests passed on the site.
