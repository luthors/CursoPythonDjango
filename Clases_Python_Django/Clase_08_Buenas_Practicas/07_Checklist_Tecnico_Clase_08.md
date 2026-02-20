# ✅ Clase 08 · Checklist Técnico de Entrega

[⬅️ Volver a la clase](Clase_08_Buenas_Practicas.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## Seguridad

- [ ] `DEBUG=False` en configuración de producción.
- [ ] `SECRET_KEY` tomada desde entorno.
- [ ] `.env` fuera de control de versiones.
- [ ] `ALLOWED_HOSTS` definido correctamente.

## Configuración

- [ ] `requirements.txt` actualizado.
- [ ] `STATIC_ROOT` configurado.
- [ ] `MEDIA_ROOT` configurado.
- [ ] `collectstatic` ejecutado.

## Verificación

- [ ] `python manage.py check` sin errores críticos.
- [ ] `python manage.py check --deploy` revisado.
- [ ] App funcional con settings de producción.

## Documentación

- [ ] Variables obligatorias documentadas.
- [ ] Pasos de arranque descritos.
- [ ] Preparación para deploy validada.
