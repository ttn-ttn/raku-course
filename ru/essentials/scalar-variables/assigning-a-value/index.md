---
title: Присвоение значения
---

{% include menu.html %}

Используйте оператор `=`, чтобы присвоить новое значение в скалярный контейнер.

```raku
my $name;
$name = 'Anna';
```

Теперь вы можете использовать эту переменную и, например, вывести ее:

```raku
say $name;
```

## Несколько присвоений

Значения можно присвоить нескольким переменным сразу. Например, вот так можно
присвоить два значения скалярам за одну инструкцию:

```raku
my ($a, $b);
($a, $b) = 10, 20;
```

Важно: нельзя убрать скобки с левой стороны. Но для симметрии вы можете их
добавить с правой стороны:

```raku
($a, $b) = (10, 20);
```

{% include nav.html %}