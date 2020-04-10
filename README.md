# Курс "Программирование на Python"

Курс посвящен базовым понятиям и элементам языка программирования Python (операторы, числовые и строковые переменные, списки, условия и циклы). Курс является вводным и наиболее подойдет слушателям, не имеющим опыта написания программ ни на одном из языков программирования.

- [Курс "Программирование на Python"](#Курс-Программирование-на-python)
  - [Операторы. Переменные. Типы данных. Условия](#Операторы-Переменные-Типы-данных-Условия)
    - [Переменные](#Переменные)
    - [Условия](#Условия)
    - [Задачи по материалам недели](#Задачи-по-материалам-недели)
  - [Циклы. Строки. Списки](#Циклы-Строки-Списки)
  - [Функции. Словари. Интерпретатор. Файлы. Модули](#Функции-Словари-Интерпретатор-Файлы-Модули)

## Операторы. Переменные. Типы данных. Условия

<details>
<summary>
### Переменные
</summary>

---

Напишите программу:

Тимофей обычно спит ночью ![X](https://render.githubusercontent.com/render/math?math=X) часов и устраивает себе днем тихий час на ![Y](https://render.githubusercontent.com/render/math?math=Y) минут. Определите, сколько всего минут Тимофей спит в сутки.

Внимание, программа принимает значения ![X](https://render.githubusercontent.com/render/math?math=X) и ![Y](https://render.githubusercontent.com/render/math?math=Y) из стандартного потока ввода (функция `input`), результат надо выводить в стандартный поток вывода (функция `print`). Обратите внимание на то, что приглашение, переданное в качестве аргумента в функцию input, считается выводом вашей программы. Используйте эту функцию без аргументов:

```python
values = input()  # без строки приглашения!
```

**Sample Input 1:**

```
7
30
```

**Sample Output 1:**

```
450
```

**Sample Input 2:**

```
0
42
```

**Sample Output 2:**

```
42
```

[Решение](solutions/week-1/variables_1.py)

---

<br>

Коля каждый день ложится спать ровно в полночь и недавно узнал, что оптимальное время для его сна составляет ![X](https://render.githubusercontent.com/render/math?math=X) минут. Коля хочет поставить себе будильник так, чтобы он прозвенел ровно через ![X](https://render.githubusercontent.com/render/math?math=X) минут после полуночи, однако для этого необходимо указать время сигнала в формате часы, минуты. Помогите Коле определить, на какое время завести будильник.

Часы и минуты в выводе программы должны располагаться на разных строках (см. пример работы программы)

Помните, что для считывания данных нужно вызывать функцию `input` без аргументов!

**Sample Input 1:**

```
480
```

**Sample Output 1:**

```
8
0
```

**Sample Input 2:**

```
512
```

**Sample Output 2:**

```
8
32
```

[Решение](solutions/week-1/variables_2.py)

---

<br>

Катя узнала, что ей для сна надо ![X](https://render.githubusercontent.com/render/math?math=X) минут. В отличие от Коли, Катя ложится спать после полуночи в ![H](https://render.githubusercontent.com/render/math?math=H) часов и ![M](https://render.githubusercontent.com/render/math?math=M) минут. Помогите Кате определить, на какое время ей поставить будильник, чтобы он прозвенел ровно через ![X](https://render.githubusercontent.com/render/math?math=X) минут после того, как она ляжет спать.

На стандартный ввод, каждое в своей строке, подаются значения ![X](https://render.githubusercontent.com/render/math?math=X), ![H](https://render.githubusercontent.com/render/math?math=H) и ![M](https://render.githubusercontent.com/render/math?math=M). Гарантируется, что Катя должна проснуться в тот же день, что и заснуть. Программа должна выводить время, на которое нужно поставить будильник: в первой строке часы, во второй — минуты.

**Sample Input 1:**

```
480
1
2
```

**Sample Output 1:**

```
9
2
```

**Sample Input 2:**

```
475
1
55
```

**Sample Output 2:**

```
9
50
```

[Решение](solutions/week-1/variables_3.py)

---

</details>

<details>
<summary>
### Условия
</summary>

---

Из передачи “Здоровье” Аня узнала, что рекомендуется спать хотя бы ![A](https://render.githubusercontent.com/render/math?math=A) часов в сутки, но пересыпать тоже вредно и не стоит спать более ![B](https://render.githubusercontent.com/render/math?math=B) часов. Сейчас Аня спит ![H](https://render.githubusercontent.com/render/math?math=H) часов в сутки. Если режим сна Ани удовлетворяет рекомендациям передачи “Здоровье”, выведите “Это нормально”. Если Аня спит менее ![A](https://render.githubusercontent.com/render/math?math=A) часов, выведите “Недосып”, если же более ![B](https://render.githubusercontent.com/render/math?math=B) часов, то выведите “Пересып”.

Получаемое число ![A](https://render.githubusercontent.com/render/math?math=A) всегда меньше либо равно ![B](https://render.githubusercontent.com/render/math?math=B).

На вход программе в три строки подаются переменные в следующем порядке: ![A](https://render.githubusercontent.com/render/math?math=A), ![B](https://render.githubusercontent.com/render/math?math=B), ![H](https://render.githubusercontent.com/render/math?math=H).

Обратите внимание на регистр символов: вывод должен в точности соответствовать описанному в задании, т. е. если программа должна вывести "Пересып", выводы программы "пересып", "ПЕРЕСЫП", "ПеРеСыП" и другие не будут считаться верными.

Это первое не самое тривиальное задание на условное выражение. В случаях, когда разбить исполнение программы на несколько направлений, стоит **внимательно** обдумать все условия, которые нужно использовать. Особое внимание стоит уделить строгости используемых условных операторов: различайте ![\lt](https://render.githubusercontent.com/render/math?math=%5Clt) и ![\le](https://render.githubusercontent.com/render/math?math=%5Cle); ![\gt](https://render.githubusercontent.com/render/math?math=%5Cgt) и ![\ge](https://render.githubusercontent.com/render/math?math=%5Cge). Для того, чтобы понимать, какой из них стоит использовать, **внимательно** прочитайте условие задания.

**Sample Input 1:**

```
6
10
8
```

**Sample Output 1:**

```
Это нормально
```

**Sample Input 2:**

```
7
9
10
```

**Sample Output 2:**

```
Пересып
```

**Sample Input 3:**

```
7
9
2
```

**Sample Output 3:**

```
Недосып
```

[Решение](solutions/week-1/conditions_1.py)

---

</details>

<details>
<summary>
### Задачи по материалам недели
</summary>

---

В то далёкое время, когда Паша ходил в школу, ему очень не нравилась формула Герона для вычисления площади треугольника, так как казалась слишком сложной. В один прекрасный момент Павел решил избавить всех школьников от страданий и написать и распространить по школам программу, вычисляющую площадь треугольника по трём сторонам.

Одна проблема: так как эта формула не нравилась Павлу, он её не запомнил. Помогите ему завершить доброе дело и напишите программу, вычисляющую площадь треугольника по переданным длинам трёх его сторон по формуле Герона:

![S=\sqrt{p(p-a)(p-b)(p-c)}](<https://render.githubusercontent.com/render/math?math=S%3D%5Csqrt%7Bp(p-a)(p-b)(p-c)%7D>)

где ![p=\dfrac{a+b+c}2](https://render.githubusercontent.com/render/math?math=p%3D%5Cdfrac%7Ba%2Bb%2Bc%7D2)
​
– полупериметр треугольника. На вход программе подаются целые числа, выводом программы должно являться вещественное число, соответствующее площади треугольника.

**Sample Input:**

```
3
4
5
```

**Sample Output:**

```
6.0
```

[Решение](solutions/week-1/triangle_area.py)

---

<br>

Напишите программу, принимающую на вход целое число, которая выводит True, если переданное значение попадает в интервал ![formula](<https://render.githubusercontent.com/render/math?math=(-15%2C%2012%5D%20%5Ccup%20(14%2C%2017)%20%5Ccup%20%5B19%2C%20%2B%5Cinfty)>) и `False` в противном случае (регистр символов имеет значение).

**Sample Input 1:**

```
20
```

**Sample Output 1:**

```
True
```

**Sample Input 2:**

```
-20
```

**Sample Output 2:**

```
False
```

[Решение](solutions/week-1/interval.py)

---

<br>

Напишите простой калькулятор, который считывает с пользовательского ввода три строки: первое число, второе число и операцию, после чего применяет операцию к введённым числам ("первое число" "операция" "второе число") и выводит результат на экран.

Поддерживаемые операции: +, -, /, \*, mod, pow, div, где
`mod` — это взятие остатка от деления,
`pow` — возведение в степень,
`div` — целочисленное деление.

Если выполняется деление и второе число равно 0, необходимо выводить строку "Деление на 0!".

Обратите внимание, что на вход программе приходят вещественные числа.

**Sample Input 1:**

```
5.0
0.0
mod
```

**Sample Output 1:**

```
Деление на 0!
```

**Sample Input 2:**

```
-12.0
-8.0
*
```

**Sample Output 2:**

```
96.0
```

**Sample Input 3:**

```
5.0
10.0
/
```

**Sample Output 3:**

```
0.5
```

[Решение](solutions.solutions/week-1/simple_calculator.py)

---

<br>

Жители страны Малевии часто экспериментируют с планировкой комнат. Комнаты бывают треугольные, прямоугольные и круглые. Чтобы быстро вычислять жилплощадь, требуется написать программу, на вход которой подаётся тип фигуры комнаты и соответствующие параметры, которая бы выводила площадь получившейся комнаты.
Для числа π в стране Малевии используют значение 3.14.

Формат ввода, который используют Малевийцы:

```
треугольник
a
b
c
```

где a, b и c — длины сторон треугольника

```
прямоугольник
a
b
```

где a и b — длины сторон прямоугольника

```
круг
r
```

где r — радиус окружности

**Sample Input 1:**

```
прямоугольник
4
10
```

**Sample Output 1:**

```
40.0
```

**Sample Input 2:**

```
круг
5
```

**Sample Output 2:**

```
78.5
```

**Sample Input 3:**

```
треугольник
3
4
5
```

**Sample Output 3:**

```
6.0
```

[Решение](solutions/week-1/malevia_livingarea.py)

---

<br>

Напишите программу, которая получает на вход три целых числа, по одному числу в строке, и выводит на консоль в три строки сначала максимальное, потом минимальное, после чего оставшееся число.

На ввод могут подаваться и повторяющиеся числа.

**Sample Input 1:**

```
8
2
14
```

**Sample Output 1:**

```
14
2
8
```

**Sample Input 2:**

```
23
23
21
```

**Sample Output 2:**

```
23
21
23
```

[Решение](solutions/week-1/max_min.py)

---

<br>

В институте биоинформатики по офису передвигается робот. Недавно студенты из группы программистов написали для него программу, по которой робот, когда заходит в комнату, считает количество программистов в ней и произносит его вслух: "n программистов".

Для того, чтобы это звучало правильно, для каждого ![n](https://render.githubusercontent.com/render/math?math=n) нужно использовать верное окончание слова.

Напишите программу, считывающую с пользовательского ввода целое число ![n](https://render.githubusercontent.com/render/math?math=n) (неотрицательное), выводящее это число в консоль вместе с правильным образом изменённым словом "программист", для того, чтобы робот мог нормально общаться с людьми, например: 1 программист, 2 программиста, 5 программистов.

В комнате может быть очень много программистов. Проверьте, что ваша программа правильно обработает все случаи, как минимум до 1000 человек.

**Дополнительный комментарий к условию:**
Обратите внимание, что задача не так проста, как кажется на первый взгляд. Если ваше решение не проходит какой-то тест, это значит, что вы не рассмотрели какой-то из случаев входных данных (число программистов ![0 \le n \le 1000](https://render.githubusercontent.com/render/math?math=0%20%5Cle%20n%20%5Cle%201000)). Обязательно проверяйте свои решения на дополнительных значениях, а не только на тех, что приведены в условии задания.

**Sample Input 1:**

```
5
```

**Sample Output 1:**

```
5 программистов
```

**Sample Input 2:**

```
0
```

**Sample Output 2:**

```
0 программистов
```

**Sample Input 3:**

```
1
```

**Sample Output 3:**

```
1 программист
```

**Sample Input 4:**

```
2
```

**Sample Output 4:**

```
2 программиста
```

[Решение](solutions/week-1/ending.py)

---

<br>

**Дополнительная**

Паша очень любит кататься на общественном транспорте, а получая билет, сразу проверяет, счастливый ли ему попался. Билет считается счастливым, если сумма первых трех цифр совпадает с суммой последних трех цифр номера билета.

Однако Паша очень плохо считает в уме, поэтому попросил вас написать программу, которая проверит равенство сумм и выведет "Счастливый", если суммы совпадают, и "Обычный", если суммы различны.

На вход программе подаётся строка из шести цифр.

Выводить нужно только слово "Счастливый" или "Обычный", с большой буквы.

**Sample Input 1:**

```
090234
```

**Sample Output 1:**

```
Счастливый
```

**Sample Input 2:**

```
123456
```

**Sample Output 2:**

```
Обычный
```

[Решение](solutions/week-1/lucky_ticket.py)

---

</details>

## Циклы. Строки. Списки

## Функции. Словари. Интерпретатор. Файлы. Модули
