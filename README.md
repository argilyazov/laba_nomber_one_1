# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #5 выполнил(а):
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
Обучить экономическую модель, которая будет подстраиваться под инфляцию в игре и построить графики изменения данных.

## Задание 1
### Обучение модели добытчика ресурсов
Ход работы:
- Cкачиваем проект и устанавливаем необходимые пакеты
![image](https://user-images.githubusercontent.com/103649799/204909171-25728d68-dff0-49f2-97ce-f91db234205f.png)

-Создаем виртуальное окружение, скачиваем библиотеки и запускаем обучение
![image](https://user-images.githubusercontent.com/103649799/204909305-20081cca-4742-4f66-b00b-087cfca66d3d.png)

-Принимаем результаты
![image](https://user-images.githubusercontent.com/103649799/204912925-e113bb21-e7d0-4d80-afdf-1c0304e1145d.png)


## Задание 2
### Визуализировать данные обучения
Ход работы:
- Теперь скачаем библиотеку для визуализации наших данных
![image](https://user-images.githubusercontent.com/103649799/204914095-79302aec-db83-4c02-9c6f-0e939ead9309.png)

- Смотрим графики первого обучения, график наград идет вверх, а loss вниз, что хорошо
![image](https://user-images.githubusercontent.com/103649799/204914083-9e60c7f2-098d-4fa7-8aa3-34a828f756b5.png)

- Далее меняем праметры yaml файла и смотрим результаты и так пять раз:

```strength: 0.5```

![image](https://user-images.githubusercontent.com/103649799/204917059-01f3bfc3-aabc-4eb0-90cf-97bfa16c6f8d.png)
При таких значениях график наград стал убывающим

```strength: 1.5```
## Задание 3
### 


## Выводы




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
