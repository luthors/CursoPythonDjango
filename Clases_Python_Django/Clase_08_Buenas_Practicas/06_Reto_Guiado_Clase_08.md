# 🧠 Clase 08 · Reto Guiado: Proyecto Listo para Producción

[⬅️ Volver a la clase](Clase_08_Buenas_Practicas.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## 🎯 Objetivo

Aplicar una capa mínima de hardening para desplegar con seguridad básica.

## 🧱 Requisitos

- Variables sensibles fuera del código.
- `DEBUG=False` en escenario productivo.
- `ALLOWED_HOSTS` correcto.
- Estáticos y media configurados.
- Dependencias actualizadas y documentadas.

## 🪜 Paso a paso sugerido

1. Crear `.env` y mapear variables en settings.
2. Configurar `STATIC_ROOT`/`MEDIA_ROOT`.
3. Ejecutar `collectstatic`.
4. Generar `requirements.txt`.
5. Ejecutar `check --deploy` y corregir alertas críticas.

## ✅ Criterios de logro

- El proyecto corre con configuración productiva básica.
- No hay secretos en código fuente.
- Existe documentación mínima para deploy.

## 📌 Extensión opcional

- Separar settings por entorno.
- Integrar Whitenoise.
- Añadir logging de errores.
