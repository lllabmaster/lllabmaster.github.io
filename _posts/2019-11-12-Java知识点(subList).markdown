---
layout: post
title: Java知识点（subList）
date: 2019-11-12
comments: true
---

Java的subList函数使用比较容易出错，endIndex必须在列表范围内，超过列表长度，就会报错。

如果在lambda表达式中，可以使用limit替代

```java
List<String> anchorIds = whiteAnchorData.getRecList()
    .stream()
    .map(x -> Pair.of(x.getUserId(), -1 * x.getPopularity()))
    .sorted(Comparator.comparing(Pair::getRight))
    .limit(N)
    .map(x -> x.getLeft())
    .collect(Collectors.toList());
```