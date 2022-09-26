# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #1 выполнил(а):
- Толочко Дмитрий Александрович
- РИ-210944
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
- Задание 1.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 2.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 3.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Выводы.
- ✨Magic ✨

## Цель работы
Ознакомиться с основными операторами языка Python на примере реализации линейной регрессии.

## Задание 1
### Написать программы Hello World на Python и Unity
- Для Python в отчёте привести скриншоты с демонстрацией сохранения документа google.collab на свой диск с запуском программы, выводящей сообщение Hello world.
![image](https://user-images.githubusercontent.com/100460661/192241133-1268a5e3-5f17-4c1c-8e2c-d861d4d667df.png)
![image](https://user-images.githubusercontent.com/100460661/192241208-994970c6-1190-4ae8-a91c-4cc8977c3a75.png)

![image](https://user-images.githubusercontent.com/100460661/192250872-906bf264-f4c8-464f-b192-731d6e1764aa.png)
![image](https://user-images.githubusercontent.com/100460661/192250942-43023940-bc4f-4a16-b459-87e7d93a4e3e.png)


## Задание 2
### Пошагово выполнить каждый пункт раздела "ход работы" с описанием и примерами реализации задач
Ход работы:
1) Произвести подготовку данных для работы с алгоритмом линейной регрессии. 10 видов данных были установлены случайным образом, и данные находились в линейной зависимости. Данные преобразуются в формат массива, чтобы их можно было вычислить напрямую при использовании умножения и сложения.

```py

In [ ]:
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

![image](https://user-images.githubusercontent.com/100460661/192266360-56f2f840-c419-4401-a103-32595ee164e8.png)


2) Определите связанные функции. Функция модели: определяет модель линейной регрессии wx+b. Функция потерь: функция потерь среднеквадратичной ошибки. Функция оптимизации: метод градиентного спуска для нахождения частных производных w и b.

![image](https://user-images.githubusercontent.com/100460661/192269147-205f060e-63fc-4a80-826b-5e5c4992b369.png)

3) Начать итерацию.
### Шаг 1 Инициализация и модель итеративной оптимизации

![image](https://user-images.githubusercontent.com/100460661/192276821-c1756b55-a0d2-4a22-8def-bb17113e4a86.png)

### Шаг 2 На второй итерации отображаются значения параметров, значения потерь и эффекты визуализации после итерации

![image](https://user-images.githubusercontent.com/100460661/192276987-d43c4408-5d0e-45bf-a3bc-1a39125b1880.png)

### Шаг 3 Третья итерация показывает значения параметров, значения потерь и визуализацию после итерации

![image](https://user-images.githubusercontent.com/100460661/192277144-c9d3be83-591d-4224-9465-f44a990c55dc.png)

### Шаг 4 На четвертой итерации отображаются значения параметров, значения потерь и эффекты визуализации

![image](https://user-images.githubusercontent.com/100460661/192277197-4c2664ab-2136-4e06-820b-ff7f8f779996.png)

### Шаг 5 Пятая итерация показывает значение параметра, значение потерь и эффект визуализации после итерации

![image](https://user-images.githubusercontent.com/100460661/192277273-0c592663-2dd2-40c5-8b63-cf01402f3555.png)

### Шаг 6 10000-я итерация, показывающая значения параметров, потери и визуализацию после итерации

![image](https://user-images.githubusercontent.com/100460661/192277337-fb3d2673-f4cb-49af-b992-6111b7c048eb.png)

## Задание 3
### Должна ли величина loss стремиться к нулю при изменении исходных данных? Ответьте на вопрос, приведите пример выполнения кода, который подтверждает ваш ответ.

Да, loss будет уменьшаться, то есть стремиться к нулю. Она зависит от a и b,а они в свою очередь зависят от величины times. Если мы увеличим times, то loss уменьшится.

1) ![image](https://user-images.githubusercontent.com/100460661/192295499-1c89efff-64e4-4079-ad7b-f55f0c408093.png)
При times = 100, loss = 1298,5

2) ![image](https://user-images.githubusercontent.com/100460661/192295835-86a9316a-ad9f-4df1-b0ae-1f203c2dac92.png)
При times = 1000, loss = 193.58

3) ![image](https://user-images.githubusercontent.com/100460661/192296070-05e41a8a-175f-47ca-95a1-468ccc0f064f.png)
При times = 100000, loss = 188.8

### Какова роль параметра Lr? Ответьте на вопрос, приведите пример выполнения кода, который подтверждает ваш ответ. В качестве эксперимента можете изменить значение параметра.

От параметра Lr зависит угол прямой на графике

1) ![image](https://user-images.githubusercontent.com/100460661/192300176-ef6f4b05-4ef8-46a2-8f90-11c780221593.png)
При Lr = 0.000001 и times = 100

2) ![image](https://user-images.githubusercontent.com/100460661/192300512-3c58ac9a-73ec-453e-b13f-c468f4db9231.png)
При Lr = 0.0001 и times = 100

## Выводы

В ходе данной работы я написал программу Hello world на питоне в Google Collab и на C# в Unity. Я познакомился с алгоритмом линейной регрессии, осуществил функции модели, потерь и оптимизации. Я провёл эксперимент над переменными Lr и loss и выявил их зависимости.

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
