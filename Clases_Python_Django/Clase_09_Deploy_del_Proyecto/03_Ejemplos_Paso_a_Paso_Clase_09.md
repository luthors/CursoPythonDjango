# 🧪 Clase 09 · Ejemplos Paso a Paso

[⬅️ Volver a la clase](Clase_09_Deploy_del_Proyecto.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## 1) Dependencias necesarias

```txt
# requirements.txt (ejemplo)
Django==5.2.0
gunicorn==22.0.0
whitenoise==6.8.2
psycopg[binary]==3.2.0
```

---

## 2) Procfile de arranque

```txt
web: gunicorn proyecto.wsgi
```

---

## 3) Configuración mínima de producción en settings

```python
DEBUG = os.getenv("DEBUG", "False") == "True"
ALLOWED_HOSTS = os.getenv("ALLOWED_HOSTS", "localhost").split(",")
```

---

## 4) Flujo Git básico para deploy

```bash
git add .
git commit -m "Ajustes para deploy"
git push origin main
```

---

## 5) Comandos post-deploy típicos

```bash
python manage.py migrate
python manage.py collectstatic --noinput
python manage.py createsuperuser
```

---

## 6) Diagnóstico rápido por logs

- Error de módulo: revisar `requirements.txt`.
- Error 400 host: revisar `ALLOWED_HOSTS`.
- Error DB: revisar variables de conexión.
