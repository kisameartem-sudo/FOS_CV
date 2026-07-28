# Автоматические проверки

Каталог содержит проверки программного окружения и unit-тесты вспомогательного пакета `cv_course`.

| Файл | Назначение |
|---|---|
| `test_environment.py` | Проверка версии Python, обязательных библиотек и доступности CUDA |
| `test_metrics.py` | Тесты метрик IoU, BLEU, CER и WER |

## Подготовка окружения

Из корня репозитория:

```bash
python -m venv .venv
source .venv/bin/activate  # Windows PowerShell: .venv\Scripts\Activate.ps1
pip install -r requirements-course.txt
```

## Команды запуска

Проверка окружения:

```bash
python tests/test_environment.py
```

Все unit-тесты:

```bash
pytest -q tests
```

Только тесты метрик:

```bash
pytest -q tests/test_metrics.py
```

Альтернативный запуск без `pytest`:

```bash
python tests/test_metrics.py
```

Команды следует выполнять из корня репозитория, чтобы пакет `cv_course` импортировался корректно.
