# Функции ввода, вывод на консоль. Типы данных. Полезные функции

## Описание встроеных функций
[https://docs.python.org/3/library/functions.html#input](Документация)

Функция начинается с имени функции. Скобки () вызывают выполнение функции.

## Команда ввода input

`input([prompt])`

Данная команда читает данные из консоли ввода и возвращает результат как строку. Если задан параметр prompt, то значение prompt перед этим печатается в консоль без перевода строки.

## Команды вывода print

`print(*objects, sep=' ', end='\n', file=sys.stdout, flush=False)`

Печатает строку или строки из аргумента objects в консоль с переводом строки
Можно аргументом sep передать разделитель, если objects это несколько строк.
Аргумент end - определяет как закончится строка. "\n" - Это перевод строки.

## Специальные символы при выводе на консоль

- `\n` - Новая строка
- `\uхххх` - Символ Unicode с 16 битным шестнадцатеричным значением xxxx
- `\\` - Сам символ `\`

Если надо вывести строку без всяких спец символов, то достаточно перед строкой поставить r:
`print(r'Перевода\nнет')` - работает только для строк

## Форматирование строк. Функция format

`format(*args, **kwargs)`

Форматирует value по формату, заданному format_spec
Примеры:

```
>>> "The sum of 1 + 2 is {0}".format(1+2)
'The sum of 1 + 2 is 3'

# можно даже вывести числа в обратном порядке
>>> "{2}, {1}, {0}".format(5, 6, 7)
'7, 6, 5'

# Можно даже давать имена переменным:
>>> "{first} гонялась за {second}".format(second="мячиком", first="Собака")
'Собака гонялась за мячиком'
```

## Тип int

Это целые числа. Такие как ... -2, -1, 0, 1, 2, 3 ...

Чтобы преобразовать строку к целому числу необходимо строку поместить в функцию int()

`int(x, base=10)`

x - значение, которое надо перевести в число
base - система счисления. Например десятеричная, шестнадцатеричная, двоичная

## Тип float

Это вещественные числа. Такие как 5.33

`float([x])`

х - строка, которую надо интерпретировать(перевести) как вещественное число. В строке могут присутствовать знаки + или -

Примеры: 

Просто число
> float('+1.23') `1.23`

Тут есть перевод строки
> float('   -12345\n') `-12345.0`

Это ещё одно представление чисел
> float('1e-003') `0.001`

И еще одно представление чисел. Тут большая буква!
> float('+1E6') `1000000.0`

А это бесконечность!
> float('-Infinity') `-inf`

## Тип Boolean

`bool([x])`

Имеет лишь 2 значения:
- True
- False

Чтобы преобразовать в булево значение примените к строке функцию bool():

`bool("True")`

## Тип string

`str(object='')` - Создает строку из переданного аргумента.

К строке могут быть преобразованы объекты!

## Другие функции

`bin(x)` - Конвертирует целое цисло в строку, которая является двоичным представлением данного числа.

`hex(x)` - Конвертирует целое число в строку, которая является шестнадцатеричным представлением данного числа.

`round(number[, ndigits])` - Округляет вещественное число

`len(s)` - Возвращает длину объекта. Например длинну строки

`max(arg1, arg2, *args[, key])` - Возвращает максимальное число из переданных аргументов

`min(arg1, arg2, *args[, key])` - Возвращает минимальное число из переданных аргументов

`sum(iterable[, start])` - Суммирует перечисляемый объект(например, массив), начиная с индекса start