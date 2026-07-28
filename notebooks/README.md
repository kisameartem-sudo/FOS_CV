# Исполняемые лабораторные блокноты

Каталог содержит стартовые Jupyter Notebook для девяти лабораторных работ. Блокноты повторяют структуру соответствующих КИМ и содержат заготовки, которые обучающийся дополняет самостоятельно.

## Подготовка окружения

Из корня репозитория:

```bash
python -m venv .venv
# Linux/macOS
source .venv/bin/activate
# Windows PowerShell
# .venv\Scripts\Activate.ps1

python -m pip install --upgrade pip
pip install -r requirements-course.txt
pip install jupyter
```

## Запуск

Открыть каталог блокнотов в JupyterLab:

```bash
jupyter lab notebooks/
```

Открыть конкретную лабораторную работу:

```bash
jupyter notebook notebooks/lab01_viola_jones.ipynb
```

Пересоздать все стартовые блокноты из генератора:

```bash
python notebooks/generate_all.py
```

> Команда генерации перезаписывает файлы `lab01_*.ipynb`–`lab09_*.ipynb`. Перед запуском сохраните собственные изменения в другом каталоге или ветке.

## Связанные материалы

- [КИМ модулей](../README.md#3-контрольно-измерительные-материалы)
- [Baseline-заготовки](../baselines/README.md)
- [Общие функции курса](../cv_course/README.md)
- [Проверка окружения и тесты](../tests/README.md)
