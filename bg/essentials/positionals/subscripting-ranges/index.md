---
title: Индексиране на диапазони
---

{% include menu.html %}

`Диапазон`ът е позиционен тип данни. Както при масивите, можете да достъпвате неговите индивидуални елементи.

Например, ето как да отпечатате третия елемент в последователността от елементи, която диапазонът генерира:

```raku
my $r = 10..20;
say $r[3]; # 13
```

Важно е да се осъзнае, че диапазоните, за разлика от масивите, не е задължително да държат всички стойности в паметта.

## Размер

За да получите размера на диапазона, използвайте метода `elems`, както правите с масивите.

```raku
my $r = 10..20;
say $r.elems; # 11
```

{% include nav.html %}