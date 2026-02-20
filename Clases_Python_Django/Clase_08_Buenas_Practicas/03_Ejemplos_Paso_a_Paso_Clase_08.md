# 🧪 Clase 08 · Ejemplos Paso a Paso

[⬅️ Volver a la clase](Clase_08_Buenas_Practicas.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## 1) Crear `.env` local

```env
DEBUG=True
SECRET_KEY=mi-clave-local-segura
ALLOWED_HOSTS=127.0.0.1,localhost
```

---

## 2) Leer entorno desde settings

```python
import os

DEBUG = os.getenv("DEBUG", "False") == "True"
SECRET_KEY = os.getenv("SECRET_KEY")
ALLOWED_HOSTS = os.getenv("ALLOWED_HOSTS", "127.0.0.1").split(",")
```

---

## 3) Generar dependencias congeladas

```bash
pip freeze > requirements.txt
```

---

## 4) Preparar estáticos

```bash
python manage.py collectstatic --noinput
```

---

## 5) Validar configuración Django

```bash
python manage.py check --deploy
```

---

## 6) Ignorar archivos sensibles en Git

```gitignore
.env
.venv/
__pycache__/
*.sqlite3
```
