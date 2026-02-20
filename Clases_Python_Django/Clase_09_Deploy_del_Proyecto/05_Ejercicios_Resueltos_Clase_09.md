# ✅ Clase 09 · Ejercicios Resueltos (Selección)

[⬅️ Volver a la clase](Clase_09_Deploy_del_Proyecto.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## Resuelto 1: `requirements.txt` mínimo para deploy

```txt
Django==5.2.0
gunicorn==22.0.0
whitenoise==6.8.2
```

## Resuelto 2: Procfile correcto

```txt
web: gunicorn proyecto.wsgi
```

## Resuelto 3: Push inicial a GitHub

```bash
git init
git add .
git commit -m "Deploy inicial"
git branch -M main
git remote add origin <URL_REPO>
git push -u origin main
```

## Resuelto 4: Variables de entorno mínimas

```env
DEBUG=False
SECRET_KEY=clave-segura-produccion
ALLOWED_HOSTS=miapp.onrender.com
```

## Resuelto 5: Comandos post-deploy

```bash
python manage.py migrate
python manage.py collectstatic --noinput
python manage.py createsuperuser
```
