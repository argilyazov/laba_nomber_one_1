# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #1 выполнил(а):
- Гилязов Арсель Мирасович
- РИ210950
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | * | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Структура отчета

- Данные о работе: название работы, фио, группа, выполненные задания.
- Цель работы.
- Задание 1.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 2.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 3.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Выводы.
- ✨Magic ✨

## Цель работы
Ознакомиться с основными операторами зыка Python на примере реализации линейной регрессии.

## Задание 1
### Написание программмы выводящей hello world на python и Unity
Ход работы:
![image](https://user-images.githubusercontent.com/103649799/195152500-3f337684-5118-4306-ade2-c11dccd7d9f8.png)
![image](https://user-images.githubusercontent.com/103649799/195152392-cc1259a6-b3c8-4b24-90d4-67b80283ea8d.png)
![image](https://user-images.githubusercontent.com/103649799/195152652-5e813c07-7485-4e15-ae9b-4cd1de2facad.png)



## Задание 2
### Скопровать и выполнить код.

Ход работы:
- Произвести подготовку данных для работы с алгоритмом линейной регрессии. 10 видов данных были установлены случайным образом, и данные находились в линейной зависимости. Данные преобразуются в формат массива, чтобы их можно было вычислить напрямую при использовании умножения и сложения.

```py
In [ ]:
#Import the required modules, numpy for calculation, and Matplotlib for drawing
import numpy as np
import matplotlib.pyplot as plt
#This code is for jupyter Notebook only
%matplotlib inline
# define data, and change list to array
x = [3,21,22,34,54,34,55,67,89,99]
x = np.array(x)
y = [2,22,24,65,79,82,55,130,150,199]
y = np.array(y)
#Show the effect of a scatter plot
plt.scatter(x,y)
```
![image](https://user-images.githubusercontent.com/103649799/192361978-8e197a6a-ad4f-49bd-8ded-2a7c9dcfcb99.png)


- Определите связанные функции. Функция модели: определяет модель линейной регрессии wx+b. Функция потерь: функция потерь среднеквадратичной ошибки. Функция оптимизации: метод градиентного спуска для нахождения частных производных w и b.

```py
def model(a, b, x):
    return a * x + b
 
 
def loss_function(a, b, x, y):
    num = len(x)
    prediction = model(a, b, x)
    return (0.5 / num) * (np.square(prediction - y)).sum()
 
 
def optimize(a, b, x, y):
    num = len(x)
    prediction = model(a, b, x)
    da = (1.0 / num) * ((prediction - y) * x).sum()
    db = (1.0 / num) * ((prediction - y).sum())
    a = a - Lr * da
    b = b - Lr * db
    return a, b
 
 
def iterate(a, b, x, y, times):
    for i in range(times):
        a, b = optimize(a, b, x, y)
    return a, b
```
- Первая итерация

```py
a = np.random.rand(1)
b = np.random.rand(1)
Lr = 0.000001
 
a, b = iterate(a, b, x, y, 1)
prediction = model(a, b, x)
loss = loss_function(a, b, x, y)
print(a, b, loss)
plt.scatter(x, y)
plt.plot(x, prediction)
```
![image](https://user-images.githubusercontent.com/103649799/192363196-be92b3b3-1d54-4fcf-bc2f-3f81afd84e05.png)

- Вторая итерация

![image](https://user-images.githubusercontent.com/103649799/192363239-06619adb-79c1-47e7-b627-82d7a76194c8.png)

- Третья итерация

![image](https://user-images.githubusercontent.com/103649799/192363283-ce4e216d-5ee3-4764-857b-de87263c79c4.png)

- Четвертая итерация

![image](https://user-images.githubusercontent.com/103649799/192363348-a15b3802-7fd8-41eb-ad37-92edd40fb513.png)

- Пятая итерация 

![image](https://user-images.githubusercontent.com/103649799/192363380-12d40e2a-e8b2-4da3-945b-bf155d1a6117.png)

- 1000-я итерация

![image](https://user-images.githubusercontent.com/103649799/192363444-db06d8a0-e8a2-402d-9144-5632be84a059.png)



## Задание 3
### Какова роль параметра Lr? Ответьте на вопрос, приведите пример выполнения кода, который подтверждает ваш ответ. В качестве эксперимента можете изменить значение параметра.
Ход работы:


- Первый вопрос.Чем ближе к прямой будут входные данные х и у, тем меньше будет переменная loss, визуализируящая отклонение от прямой, т.к. loss зависит от суммы квадратов расстояний отвходных точек до прямой

Пример упорядоченных данных:
![image](https://user-images.githubusercontent.com/103649799/192366795-55cda95a-49fb-4b1f-85a7-2e48328b5f9d.png)
![image](https://user-images.githubusercontent.com/103649799/192366861-d62de4ed-8b5b-48e5-b032-1b66f4152953.png)

Пример данных при которых точки максимально отдалены от прямой:
![image](https://user-images.githubusercontent.com/103649799/192367559-2cc9f0d0-cd5d-45ff-b637-963e993779ff.png)

- Второй вопрос: Величина lr  изменяетугол наклона синей прямой и угол наклонапряомй проведенной через точки, при увеличении первого уменьшается второе
![image](https://user-images.githubusercontent.com/103649799/192370859-53380026-66b1-4ad7-8328-3ef42c2d89ea.png)
![image](https://user-images.githubusercontent.com/103649799/192370954-db87bbc7-85d9-4eee-b4e8-6d4b7cdae6a5.png)

## Выводы

Я установил Юнити и узнал, как в нем создаются объекты и как присваивать им скрипты, узнал что такое линейная регрессия, и за что отвечают ее входные и выходные праметры

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
