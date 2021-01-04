---
title: Subscripting ranges
---

{% include menu.html %}

A `Range` is a positional data type. As with arrays, you can assess its individual elements.

Print the third element in the sequence of items that the range generates:

```raku
my $r = 10..20;
say $r[3]; # 13
```

It is important to realise that ranges, unlike arrays, do not necessarily keep all the values in memory.

{% include nav.html %}