# Make text safe for HTML

Topic: Strings | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.html_safe:solve`)

## Task

Given `comment`, return `safe`: the text with the characters &, <, > and " replaced by their HTML entities. Example: a<b gives a&lt;b.

## Signature

```
INPUTS: comment (String)
OUTPUTS: safe (String)
```

## Solution

Four chained INVOKE steps of `pub.string:replace`: & to `&amp;` first, then < to `&lt;`, > to `&gt;` and " to `&quot;`.

## Package contents

`html_safe.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/html_safe/solve/`.

All sample tests and the hidden test passed on the site.
