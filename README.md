# Машинное обучение

Домашние задания по курсу машинного обучения
(материалы курса: https://github.com/NikolaiZolotykh/MachineLearningCourse).

## Датасет

[Used Cars Dataset (Craigslist)](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data) —
около 427 тыс. объявлений о продаже подержанных автомобилей в США.

**Задача:** регрессия — предсказать цену автомобиля (`price`) по его характеристикам
(год выпуска, пробег, марка, состояние, тип топлива, коробка передач и т.д.).

## Задания

| № | Ноутбук | Содержание |
|---|---------|------------|
| 1 | [hw1_craigslist.ipynb](hw1_craigslist.ipynb) | Разведочный анализ, предобработка, kNN-регрессия |

## Как запустить

```powershell
py -3.11 -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

Данные в репозиторий не входят (файл ~1.4 ГБ). Скачать их:

```powershell
python -c "import kagglehub, shutil, os; p = kagglehub.dataset_download('austinreese/craigslist-carstrucks-data'); os.makedirs('data', exist_ok=True); shutil.copy(os.path.join(p, 'vehicles.csv'), 'data/vehicles.csv')"
```

или вручную со страницы Kaggle — положить `vehicles.csv` в папку `data/`.
