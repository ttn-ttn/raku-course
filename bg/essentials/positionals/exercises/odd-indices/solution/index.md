---
title: 'Решение: Нечетни индекси'
---

{% include menu.html %}

За да решите тази задача, можете да използвате конструкцията `loop` и да увеличавате променливата на цикъла с 2 при всяка итерация. Но можете също така да използвате цикъл `for` и да сканирате числата от 1 до половината от дължината на масива, след което да ги умножите по две.

## Код

Ето решението:

```raku
my @data = 10, 12, 1, 5, -9, 8, 36, 18, 21;

say @data[2 * $_ - 1] for 1 .. @data/2;
```

🦋 Намерете програмата във файла [odd-indices.raku](https://github.com/ash/raku-course/blob/master/exercises/positionals/odd-indices.raku).

## Резултат

Първо, изпълнете програмата с оригиналните елементи на данните.

```console
$ raku exercises/positionals/odd-indices.raku
12
5
8
18
```

След това добавете още един елемент към данните:

```raku
my @data = 10, 12, 1, 5, -9, 8, 36, 18, 21, 22;
```

Потвърдете, че новият елемент с нечетен индекс се появява в резултата:

```console
$ raku exercises/positionals/odd-indices.raku
12
5
8
18
22
```

## Коментари

В следващата част на курса ще се върнем към тази задача, за да я решим с напълно различен подход.

{% include nav.html %}