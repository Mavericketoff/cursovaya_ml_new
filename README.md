# CML — Drug Parameter Optimization

## Описание проекта

Анализ данных и построение моделей для прогнозирования биологических параметров (IC50, CC50, SI) на основе молекулярных дескрипторов.

## Структура проекта

```
data.xlsx          # Исходные данные (1001 соединение, 211 признаков)
report.md          # Аналитический отчёт с результатами всех экспериментов
requirements.txt   # Зависимости Python

# Jupyter-ноутбуки:
01_eda.ipynb           # Разведочный анализ данных
02_regression_ic50.ipynb    # Регрессия IC50
03_regression_cc50.ipynb    # Регрессия CC50
04_regression_si.ipynb      # Регрессия SI
05_classification_ic50_median.ipynb  # Классификация IC50 > median
06_classification_cc50_median.ipynb  # Классификация CC50 > median
07_classification_si_median.ipynb    # Классификация SI > median
08_classification_si_gt8.ipynb       # Классификация SI > 8

assets/              # Папка для графиков
```

## Установка

```bash
pip install -r requirements.txt
```

## Запуск

```bash
jupyter notebook .
```

Каждый ноутбик запускается сверху вниз без ручных действий.

## Результаты (кратко)

- **Регрессия:** R² < 0 для всех задач — дескрипторы не предсказывают абсолютные значения
- **Классификация CC50 > median:** ROC-AUC=0.89 — лучшее качество
- **Классификация IC50 > median:** ROC-AUC=0.80
- **Классификация SI:** ROC-AUC=0.67-0.74

## Лицензия

Исследовательский проект.
# cursovaya_ml_new
