# ✅ Clase 08 · Ejercicios Resueltos (Selección)

[⬅️ Volver a la clase](Clase_08_Buenas_Practicas.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## Resuelto 1: Variables críticas en `settings.py`

```python
import os
from pathlib import Path

BASE_DIR = Path(__file__).resolve().parent.parent
DEBUG = os.getenv("DEBUG", "False") == "True"
SECRET_KEY = os.getenv("SECRET_KEY", "solo-dev")
ALLOWED_HOSTS = os.getenv("ALLOWED_HOSTS", "127.0.0.1,localhost").split(",")
```

## Resuelto 2: Static y media

```python
STATIC_URL = '/static/'
STATIC_ROOT = BASE_DIR / 'staticfiles'

MEDIA_URL = '/media/'
MEDIA_ROOT = BASE_DIR / 'media'
```

## Resuelto 3: `.gitignore` mínimo

```gitignore
.env
.venv/
__pycache__/
*.sqlite3
```

## Resuelto 4: requirements actualizado

```bash
pip freeze > requirements.txt
```

## Resuelto 5: chequeo de seguridad

```bash
python manage.py check --deploy
```
