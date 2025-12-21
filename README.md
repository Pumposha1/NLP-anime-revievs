# Практика по NLP: Анализ русскоязычных отзывов (Anime Reviews)

## 1) Описание работы
В данной работе выполняется анализ русскоязычных текстов и решение задачи классификации тональности отзывов:
- загрузка датасета из CSV,
- предобработка текста,
- мини-анализ данных (EDA),
- baseline-модель: TF-IDF + Logistic Regression,
- оценка качества (classification_report, confusion_matrix),
- сохранение результатов в папку `outputs/`.

## 2) Содержимое проекта
- `Otsiv.ipynb` — основной ноутбук с выполнением задания
- `data/Anime_reviews_RU.csv` — датасет (русскоязычные отзывы)
- `.venv/` — виртуальное окружение (может отсутствовать у преподавателя, тогда создаётся заново)
- `outputs/` — результаты (создаётся автоматически при запуске)

## 3) Как получить датасет (если файла нет в папке data/)
Если по какой-то причине в проекте отсутствует файл `data/Anime_reviews_RU.csv`, его можно скачать с Kaggle.

### Способ 1 (рекомендуется): через Kaggle API (CLI)
1) Зарегистрироваться/войти на Kaggle.
2) Kaggle -> Account -> Create New API Token.  
   Скачается файл `kaggle.json`.

3) Положить `kaggle.json` в папку Kaggle:

**Windows:**  
`C:\Users\<USERNAME>\.kaggle\kaggle.json`

**Linux/macOS:**  
`~/.kaggle/kaggle.json`

4) В терминале, находясь в папке проекта, выполнить:

```bash
pip install kaggle
kaggle datasets download -d theodaimones888/russian-anime-reviews-dataset -p data --unzip
