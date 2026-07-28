# Пакет `cv_course`

Каталог содержит общие вспомогательные функции курса, используемые в лабораторных блокнотах и автоматических проверках.

| Модуль | Назначение |
|---|---|
| `data.py` | Пути к данным, загрузка и распаковка наборов данных |
| `metrics.py` | IoU, FID, BLEU, CER и WER |
| `visualize.py` | Сетки изображений, карты внимания и визуализация детекций |
| `__init__.py` | Публичные импорты пакета |

## Подготовка окружения

Из корня репозитория:

```bash
python -m venv .venv
source .venv/bin/activate  # Windows PowerShell: .venv\Scripts\Activate.ps1
pip install -r requirements-course.txt
```

## Проверка импорта

```bash
python -c "from cv_course.metrics import compute_iou; print(compute_iou([1], [1]))"
```

Для запуска кода из блокнотов корень репозитория должен быть текущим рабочим каталогом либо добавлен в `PYTHONPATH`:

```bash
export PYTHONPATH="$PWD"  # Windows PowerShell: $env:PYTHONPATH = (Get-Location)
```

## Тестирование

```bash
pytest -q tests/test_metrics.py
```

Подробные команды приведены в [tests/README.md](../tests/README.md).
