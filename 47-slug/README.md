# Turn a title into a slug

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.slug:solve`)

## Task

Given `title`, return `slug`: trimmed, in lower case, with each run of white space replaced by one -. Example: Order Status Report gives order-status-report.

## Signature

```
INPUTS: title (String)
OUTPUTS: slug (String)
```

## Solution

Three INVOKE steps: `pub.string:trim`, `pub.string:toLower`, then `pub.string:replace` with searchString `\s+`, useRegex true and replaceString `-`.

## Package contents

`slug.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/slug/solve/`.

All sample tests and the hidden tests passed on the site.
