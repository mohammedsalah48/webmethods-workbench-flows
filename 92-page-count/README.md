# Count the pages

Topic: Math | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.page_count:solve`)

## Task

A list shows `pageSize` records per page. Given whole numbers `records` and `pageSize`, return `pages`: how many pages are needed. A part-filled page counts as a page. Example: 21 records, 10 per page gives 3.

## Signature

```
INPUTS: records (String), pageSize (String)
OUTPUTS: pages (String)
```

## Solution

Ceiling division with whole numbers: pages = (records + pageSize − 1) ÷ pageSize:

1. INVOKE `pub.math:addInts` with num1 = `records`, num2 = `pageSize`, giving `s`.
2. INVOKE `pub.math:subtractInts` with num1 = `s`, num2 = 1, giving `s1`.
3. INVOKE `pub.math:divideInts` with num1 = `s1`, num2 = `pageSize` (remainder dropped), giving `pages`.

## Package contents

`page_count.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/page_count/solve/`.

All sample tests and both hidden tests passed on the site.
