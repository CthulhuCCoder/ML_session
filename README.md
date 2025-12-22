# ML_session

**Финальный проект по курсу Machine Learning**

В данном репозитории представлена реализация алгоритмов машинного обучения для анализа и предсказания популярности музыкальных треков на основе данных Spotify. Проект включает реализацию линейной и логистической регрессии "с нуля" (без использования высокоуровневых библиотек для обучения), а также сравнение с энсемблевыми методами (Random Forest).

## Авторы 
* *Мубаракшин Камиль**
* **Белов Глеб** 

---

## Описание проекта

Цель работы — проанализировать влияние аудио-характеристик (energy, danceability, loudness и др.) на популярность трека.

### Реализованные задачи:
1.  **Линейная регрессия (Linear Regression):**
    * Предсказание точного значения популярности (`track_popularity`).
    * **Реализация:** `NumPy`. Градиентный спуск (Mini-batch Gradient Descent) написан вручную.
    * **Метрики:** MSE (Mean Squared Error).
2.  **Классификация (Binary Classification):**
    * Определение, станет ли трек хитом (популярность выше медианы).
    * **Модель 1:** Логистическая регрессия (реализована вручную с Sigmoid activation и Log-Loss).
    * **Модель 2:** Random Forest Classifier (библиотека `sklearn` для сравнения).
    * **Метрики:** Accuracy, Precision, Recall, F1-score, ROC-AUC.

---

## Данные

Используемый датасет: `high_popularity_spotify_data.csv`
Источник данных: [[Указать источник, например Kaggle](https://www.kaggle.com/datasets/solomonameh/spotify-music-dataset)]

**Основные признаки:**
* `energy`, `tempo`, `danceability`: Характеристики звучания.
* `loudness`: Громкость (dB).
* `acousticness`, `instrumentalness`: Акустические параметры.
* `track_popularity`: Целевая переменная (0-100).

---

## Технологии и библиотеки

* **Python 3.x**
* **NumPy** (Матричные вычисления, реализация градиентного спуска)
* **Pandas** (Обработка данных)
* **Matplotlib / Seaborn** (Визуализация графиков потерь и регрессии)
* **Scikit-learn** (Только для препроцессинга, метрик и модели Random Forest)

---

## Установка и запуск

Для запуска проекта выполните следующие шаги:

1.  **Клонируйте репозиторий:**
    ```bash
    git clone [https://github.com/ВАШ_USERNAME/spotify-ml-project.git](https://github.com/ВАШ_USERNAME/spotify-ml-project.git)
    cd spotify-ml-project
    ```

2.  **Создайте виртуальное окружение (рекомендуется):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # Для Mac/Linux
    venv\Scripts\activate     # Для Windows
    ```

3.  **Установите зависимости:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Запустите Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
    Откройте файл `Project_Notebook.ipynb` (или как вы назвали файл).

---

## Результаты экспериментов

В ходе работы были проведены эксперименты с различными гиперпараметрами (`learning_rate`, `batch_size`).

* **Линейная регрессия:** Удалось достичь сходимости функции потерь (MSE) на уровне ~XX.X.
* **Классификация:** * Логистическая регрессия показала ROC-AUC: **0.XX**
    * Random Forest показал ROC-AUC: **0.XX** (обычно выше за счет нелинейности).

*Подробные графики (Loss history, ROC Curves, Confusion Matrix) доступны внутри ноутбука.*

---

## Структура репозитория

```text
├── data/
│   └── high_popularity_spotify_data.csv  # Исходные данные
├── notebooks/
│   └── ML_Final_Project.ipynb            # Основной код с реализацией и анализом
├── images/                               # Сохраненные графики (опционально)
├── README.md                             # Описание проекта
└── requirements.txt                      # Список зависимостей
