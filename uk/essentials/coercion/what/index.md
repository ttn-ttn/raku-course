---
title: Інтроспекція з `WHAT`
---

{% include menu.html %}

Можна побачити тип даних у змінній, викликавши метод `WHAT` на ній:

```raku
my $n = 42;
my $s = '42';
say $n.WHAT; # (Int)
say $s.WHAT; # (Str)
```

Тип виводиться в дужках, як показано в коментарях. Наприклад, `(Int)` або `(Str)`.

Немає проблем викликати метод на самому літералі. Наприклад:

```raku
say 42.WHAT;      # (Int)
say (-1).WHAT;    # (Int)
say 'Hello'.WHAT; # (Str)
say True.WHAT;    # (Bool)
```

Зверніть увагу, що у випадку з `-1`, ми ставимо число в дужки, оскільки `say -1.WHAT` спробує заперечити результат `1.WHAT`, що призведе до винятку.

{% include nav.html %}