---
title: Заметки по использованию Юникода
---

{% include menu.html %}

Raku предполагает, что все ваши файлы с кодом сохранены в кодировке UTF-8.
С практической точки зрения это означает, что вам не нужно волноваться о содержании
в них символов не из ASCII таблицы, например, в строках. Но этим все не ограничивается.
Скорее всего вам не придется волноваться из-за того, что ваша программа прочитает
файл, который тоже имеет кодировку UTF-8. Это также означает, что длина строки
правильно определяется как количество букв, а не количество байтов в строке
(позже мы посмотрим на это более подробно).

Следующее, что вам следует знать, это что в качестве идентификаторов вы можете
использовать буквы помимо латинского и английского алфавитов. Вы можете назвать
свою переменную `$и` заместо `$i`, если того пожелаете, и компилятор правильно
это прочитает.

Raku достаточно педантично подходит к свойствам букв Юникода. Например, он не только
знает, если символ является буквой или цифрой, но так же правильно распознает парные
символы, такие как скобки разных форм. К примеру, вы можете изменить нашу программу
"Привет, Мир!", чтобы она использовала кавычки не из латинского алфавита (вы увидите
их снова, когда мы начнем работать с грамматической системой Raku):

```raku
say ｢Hello, World!｣;
```

Некоторые встроенные операторы имеют две формы: Юникод и ASCII. Например,
неравенство можно написать как `!=`, но также и `≠`. То же касается операций
над множествами, к примеру, оператор `∈` имеет ASCII вариант `(elem)`. А еще
есть встроенная константа, к которой можно одинаково обращаться как `pi`, так и `π`.

Когда вы работаете с числами, вы можете записать число в форме `½` заместо `0.5`.
Или вычислить квадрат `$x` как `$x²`, используя число в верхнем индексе.

Вы можете найти полный список всех таких пар на следующей странице документации:
📖 [Юникод и ASCII символы](https://docs.raku.org/language/unicode_ascii).

{% include nav.html %}