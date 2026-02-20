# 🧰 Clase 04 · Comandos Base de Django

[⬅️ Volver a la clase](Clase_04_Introduccion_Django.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## Flujo mínimo recomendado

```bash
# 1) Crear entorno virtual (opcional pero recomendado)
python -m venv .venv

# 2) Activar entorno (Windows PowerShell)
.\.venv\Scripts\Activate.ps1

# 3) Instalar Django
pip install django

# 4) Crear proyecto
django-admin startproject mi_proyecto .

# 5) Crear app
python manage.py startapp core

# 6) Ejecutar servidor
python manage.py runserver
```

## Comandos útiles de verificación

```bash
python -m django --version
python manage.py check
python manage.py showmigrations
```

## Tip rápido

Si cambias archivos de rutas o vistas y el servidor está arriba, Django suele recargar automáticamente.
