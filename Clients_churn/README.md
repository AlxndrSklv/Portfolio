# [Прогноз оттока клиентов в компании](https://github.com/AlxndrSklv/Yandex-Practicum/blob/0e52fbb884d1a0fd5a0cd16b2d01fbf4aaff710e/Clients_churn/Clients_churn.ipynb)

## Описание проекта

Необходимо построить модель по прогнозу оттока клиентов. Требования к модели: ROC-AUC>0.85, test size = 0.25, RANDOM_STATE=040723.

## Описание данных

Данные состоят из файлов, полученных из разных источников:

contract.csv — информация о договоре;

personal.csv — персональные данные клиента;

internet.csv — информация об интернет-услугах;

phone.csv — информация об услугах телефонии.

## Навыки и инструменты

*Python, Pandas, Seaborn, Matplotlib, NumPy, Phik, Scikit-learn исследовательский анализ данных*

## Общий вывод

Лучший результат roc-auc = 0.88 и F1 = 0.66 на тестовой выборке показала модель GradientBoostingClassifier с гиперпараметрами:

learning_rate - 0.05,

max_depth - 7,

max_features - 1.0,

min_samples_leaf - 5,

n_estimators - 35.

