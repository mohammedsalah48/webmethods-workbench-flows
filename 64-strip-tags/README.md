# Remove HTML tags

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.strip_tags:solve`)

## Task

Given `html`, return `text`: the same content with every tag (anything between < and >) removed. Example: <b>Paid</b> in full gives Paid in full.

## Signature

```
INPUTS: html (String)
OUTPUTS: text (String)
```

## Solution

One INVOKE of `pub.string:replace` with searchString `<[^>]*>`, useRegex true and an empty replaceString.

## Package contents

`strip_tags.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/strip_tags/solve/`.

All sample tests and the hidden tests passed on the site.
