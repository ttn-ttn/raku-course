---
title: Оператор присвоено-или
---

{% include menu.html %}

Используйте так называемый _присвоено-или_ оператор `//`, чтобы получить
запасное значение, если оно еще не было присвоено.

```raku
my $a = 'alpha';
say $a // 'gamma';

my $b;
say $b // 'delta';
```

Эта программа выведет:

```
alpha
delta
```

Значение `$a` присвоено на первой строке, поэтому в выражении `$a // 'gamma'`
используется текущее значение `$a`. В случае же с `$b`, переменная еще не была
инициализирована, поэтому `$b // 'delta'` возвращает операнд с правой стороны, и
программа выводит `delta`.

## //=

Комбинация `//` и `=` дает в результате оператор `//=`, который присваивает
значение переменной, если оно отсутствует.

```raku
my $x;
$x //= 42;
say $x; # 42
```

{% include nav.html %}