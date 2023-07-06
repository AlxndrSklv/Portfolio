# [Восстановление золота из руды](https://github.com/AlxndrSklv/Yandex-Practicum/blob/0fd8be8fe101819d84083bbf0753aa0a5c730881/Gold_recovery/Gold_recovery.ipynb)

## Описание проекта

Требуется подготовить прототип модели машинного обучения (написать функцию sMAPE), которая предскажет коэффициент восстановления золота из золотосодержащей руды. Модель поможет оптимизировать производство, чтобы не запускать предприятие с убыточными характеристиками.

## Описание данных

Данные находятся в трёх файлах:

gold_industry_train.csv — обучающая выборка;

gold_industry_test.csv — тестовая выборка;

gold_industry_full.csv — исходные данные.

Данные индексируются датой и временем получения информации (признак date). Соседние по времени параметры часто похожи.
Некоторые параметры недоступны, потому что замеряются и/или рассчитываются значительно позже. Из-за этого в тестовой выборке отсутствуют признаки, которые могут быть в обучающей. Также в тестовом наборе нет целевых признаков.

## Навыки и инструменты

*Python, Pandas, Matplotlib, NumPy, Scikit-learn исследовательский анализ данных*

- import pandas as pd
- from sklearn.metrics import mean_absolute_error
- import matplotlib.pyplot as plt
- import numpy as np
- from sklearn.model_selection import train_test_split
- from sklearn.linear_model import LinearRegression
- from sklearn.tree import DecisionTreeRegressor
- from sklearn.ensemble import RandomForestRegressor
- from sklearn.model_selection import cross_val_score
- from sklearn.dummy import DummyRegressor
- from sklearn.metrics import make_scorer
- from sklearn.model_selection import GridSearchCV
- from sklearn.metrics import mean_squared_error

## Общий вывод

Для обучения модели использовали три алгоритма: линейная регрессия, дерево решений и случайный лес. Лучший результат показал алгоритм случайный лес, у которого самый низкий показатель на тестовой выборке sMAPE (9.09) при глубине и количестве деревьев равным 10. Предлагаю использовать данную модель в качестве прототипа ML.
