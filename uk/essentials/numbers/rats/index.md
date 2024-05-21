---
title: Раціональні числа в Raku
---

{% include menu.html %}

Раціональні числа є унікальною особливістю Raku. Тип даних `Rat` представляє такі числа.

Внутрішньо раціональні числа є дробами з двома цілими частинами: чисельником і знаменником. Таким чином, ви можете легко представити числа, такі як 1/3, без втрати точності.

Існує кілька способів записати число типу `Rat` у програмі на Raku:

```raku
my $x = 1/2;
my $y = <2/3>;
```

Зверніть увагу, що слеш тут є частиною нотації. Це не оператор ділення, тому `1/2` не означає, що ви ділите 1 на 2. Однак при виведенні раціональні числа показуються як десяткові числа або цілі числа:

```raku
say 1/2; # 0.5
say 3/4; # 0.75
```

Частина рядка після символу `#` є коментарем і ігнорується компілятором. Такі коментарі будуть використовуватися в курсі для показу виводу програми.

## Десяткова форма

Важливо розуміти, що коли ви записуєте число в десятковій формі, наприклад, `0.5`, Raku створює число типу `Rat` в цей момент. Це не ціле число, але це також не число з плаваючою комою (`float` або `double` в інших мовах). Це все ще раціональне число!

Розглянемо наступний приклад:

```raku
say 0.1 + 0.2 - 0.3;
```

Якщо мова програмування використовує арифметику з плаваючою комою для цих обчислень, результат не буде дорівнювати 0. Вебсайт [0.30000000000000004.com](https://0.30000000000000004.com) надає вичерпний список прикладів, де арифметика з плаваючою комою не дає очікуваного результату.

Але Raku виводить точний `0`. Це відбувається тому, що він трактує числа `0.1`, `0.2` і `0.3` як раціональні числа і зберігає їх як `1/10`, `2/10` і `3/10` внутрішньо. Запустіть це з командного рядка, щоб підтвердити:

```console
$ raku -e 'say 0.1 + 0.2 - 0.3'
0
```

## Юнікодні форми

Також можливо використовувати юнікодні символи, які представляють дроби, такі як `½` або `¼` або `¾`. Можливо, не завжди легко набрати їх на клавіатурі, але ці дроби є точно такими ж значеннями, як їх ASCII версії, записані у вигляді дробу або десяткового числа:

`½` | `1/2` | `<1/2>` | `0.5`
`¼` | `1/4` | `<1/4>` | `0.25`
`¾` | `3/4` | `<3/4>` | `0.75`

З деякими дробами, такими як `1/3`, у вас менше варіантів, `⅓` або `<1/3>`, оскільки десяткова форма вимагала б нескінченної кількості цифр.

{% include nav.html %}