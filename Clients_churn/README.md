# [Прогноз оттока клиентов в компании](https://github.com/AlxndrSklv/Yandex-Practicum/blob/0e52fbb884d1a0fd5a0cd16b2d01fbf4aaff710e/Clients_churn/Clients_churn.ipynb)

## Описание проекта

Необходимо построить модель по прогнозу оттока клиентов. Требования: ROC-AUC>0.85, test size = 0.25, RANDOM_STATE=040723.

## Описание данных

contract.csv — информация о договоре;

personal.csv — персональные данные клиента;

internet.csv — информация об интернет-услугах;

phone.csv — информация об услугах телефонии.

## Навыки и инструменты

*Python, Pandas, Seaborn, Matplotlib, NumPy, Phik, Scikit-learn исследовательский анализ данных*


- import pandas as pd
- import numpy as np
- import seaborn as sns
- import phik

- from phik.report import plot_correlation_matrix
- from phik import report
- import datetime
- from datetime import timedelta
- import matplotlib.pyplot as plt

- from sklearn.model_selection import train_test_split
- from sklearn.preprocessing import StandardScaler
- from sklearn.utils import shuffle
- from sklearn.linear_model import LogisticRegression
- from sklearn.model_selection import GridSearchCV
- from sklearn.ensemble import RandomForestClassifier
- from sklearn.ensemble import GradientBoostingClassifier
- from sklearn.metrics import roc_auc_score, classification_report, roc_curve
- from sklearn.dummy import DummyClassifier
- from sklearn.metrics import f1_score, confusion_matrix, make_scorer
- from collections import Counter
- from imblearn.over_sampling import RandomOverSampler

## Общий вывод

Лучший результат roc-auc = 0.88 и F1 = 0.66 на тестовой выборке показала модель GradientBoostingClassifier.
