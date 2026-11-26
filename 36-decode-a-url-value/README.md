# Decode a URL value

Topic: Strings | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.url_decode:solve`)

## Task

Given `encoded`, a URL-encoded value, return `plain`: the original text. Example: Mona+Adel%21 gives Mona Adel!.

## Signature

```
INPUTS: encoded (String)
OUTPUTS: plain (String)
```

## Solution

One INVOKE of `pub.string:URLDecode` (encoded to inString, value to plain).

## Package contents

`url_decode.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/url_decode/solve/`.

All sample tests and the hidden test passed on the site.
