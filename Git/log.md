# git log --pretty=format

## Простой построчный вывод

```bash
$ git log --pretty=oneline
```
Короткий, построчный вывод записи коммитов. Удобно, когда нужно "полистать":
```bash
zac27dac22b720a069acbd0520ce95d6c730ffc4 Update Gulp config
a7faca578a87b460f79196c4918caba9fec2350e [fix] comment encoding
```

## Кастомный формат вывода

```bash
$ git log --pretty=format:"%h - %an, %ar : %s"
```

Кастомизированный формат вывода через параметр **--pretty=format**.
В данном случае показывает хэш, автора коммита, относительное время, имя коммита:
```bash
e68d70d - c01nd01r, 9 days ago : Update Gulp config
40ed0d3 - c01nd01r, 9 days ago : Разработка #3598
```

## Фильтрация вывода

```bash
$ git log --pretty=format:"%h - %an, %ar : %s" --before="2015-12-15" --author="c01nd01r"
```
Кастомный вывод, фильтрация по автору и дате:
```bash
27467bd - c01nd01r, 3 months ago : Adaptive main menu
d39cff4 - c01nd01r, 3 months ago : Yandex.Map
```

## Etc...
* [Больше по фильтрам и формату](https://git-scm.com/book/ru/v1/%D0%9E%D1%81%D0%BD%D0%BE%D0%B2%D1%8B-Git-%D0%9F%D1%80%D0%BE%D1%81%D0%BC%D0%BE%D1%82%D1%80-%D0%B8%D1%81%D1%82%D0%BE%D1%80%D0%B8%D0%B8-%D0%BA%D0%BE%D0%BC%D0%BC%D0%B8%D1%82%D0%BE%D0%B2)
* [К вопросу поиска по коммитам](https://toster.ru/q/138885)
