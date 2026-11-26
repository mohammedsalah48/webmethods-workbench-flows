# Count the words

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.count_words:solve`)

## Task

Given `sentence`, words separated by one or more spaces, return `words`: how many words it has.

## Signature

```
INPUTS: sentence (String)
OUTPUTS: words (String)
```

## Solution

Two INVOKE steps: `pub.string:tokenize` (sentence to inString, valueList to parts), then `pub.list:sizeOfList` (parts to fromList, size to words).

## Package contents

`count_words.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/count_words/solve/`.

All sample tests and the hidden test passed on the site.
