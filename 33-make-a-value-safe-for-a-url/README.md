# Make a value safe for a URL

Topic: Strings | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.url_encode:solve`)

## Task

Given `term`, return `encoded`: the value encoded for use in a URL query string. Example: a b&c gives a+b%26c.

## Signature

```
INPUTS: term (String)
OUTPUTS: encoded (String)
```

## Solution

One INVOKE of `pub.string:URLEncode` (term to inString, value to encoded).

## Package contents

`url_encode.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/url_encode/solve/`.

All sample tests and the hidden test passed on the site.
