# Курс "Программирование на Python"

Курс посвящен базовым понятиям и элементам языка программирования Python (операторы, числовые и строковые переменные, списки, условия и циклы). Курс является вводным и наиболее подойдет слушателям, не имеющим опыта написания программ ни на одном из языков программирования.

- [Курс "Программирование на Python"](#Курс-Программирование-на-python)
  - [Операторы. Переменные. Типы данных. Условия](#Операторы-Переменные-Типы-данных-Условия)
    - [Переменные](#Переменные)
    - [Условия](#Условия)
  - [Циклы. Строки. Списки](#Циклы-Строки-Списки)
  - [Функции. Словари. Интерпретатор. Файлы. Модули](#Функции-Словари-Интерпретатор-Файлы-Модули)

## Операторы. Переменные. Типы данных. Условия

<details>
<summary>
### Переменные
</summary>

<br>

Напишите программу:

Тимофей обычно спит ночью ![X](https://render.githubusercontent.com/render/math?math=X) часов и устраивает себе днем тихий час на ![Y](https://render.githubusercontent.com/render/math?math=Y) минут. Определите, сколько всего минут Тимофей спит в сутки.

Внимание, программа принимает значения ![X](https://render.githubusercontent.com/render/math?math=X) и ![Y](https://render.githubusercontent.com/render/math?math=Y) из стандартного потока ввода (функция `input`), результат надо выводить в стандартный поток вывода (функция print). Обратите внимание на то, что приглашение, переданное в качестве аргумента в функцию input, считается выводом вашей программы. Используйте эту функцию без аргументов:

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
<br>

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

## Циклы. Строки. Списки

## Функции. Словари. Интерпретатор. Файлы. Модули
