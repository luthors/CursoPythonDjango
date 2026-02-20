# 🧰 Clase 09 · Guía de Deploy Paso a Paso

[⬅️ Volver a la clase](Clase_09_Deploy_del_Proyecto.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## Paso 1: Preparar proyecto local

- Revisar `requirements.txt`.
- Verificar `DEBUG=False` para producción.
- Configurar `ALLOWED_HOSTS` por entorno.

## Paso 2: Publicar en GitHub

```bash
git init
git add .
git commit -m "Deploy inicial"
git branch -M main
git remote add origin <URL_REPO>
git push -u origin main
```

## Paso 3: Configurar servicio cloud

- Crear nuevo servicio Web.
- Conectar repositorio.
- Definir comando de build/start.

## Paso 4: Variables de entorno

- `SECRET_KEY`
- `DEBUG=False`
- `ALLOWED_HOSTS`
- credenciales de base de datos

## Paso 5: Migraciones y estáticos

```bash
python manage.py migrate
python manage.py collectstatic --noinput
```

## Paso 6: Verificación final

- Revisar URL pública.
- Probar login, CRUD y rutas principales.
- Revisar logs si algo falla.
