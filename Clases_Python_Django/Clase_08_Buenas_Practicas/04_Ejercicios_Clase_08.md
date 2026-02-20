# 🧩 Clase 08 · Repertorio Amplio de Ejercicios

[⬅️ Volver a la clase](Clase_08_Buenas_Practicas.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## 🟢 Nivel Básico (1–15)

1. Crear archivo `.env` local.
2. Mover `SECRET_KEY` a variable de entorno.
3. Configurar `DEBUG` por entorno.
4. Configurar `ALLOWED_HOSTS`.
5. Crear `requirements.txt` actualizado.
6. Agregar `.env` a `.gitignore`.
7. Configurar `STATIC_URL`.
8. Configurar `STATIC_ROOT`.
9. Configurar `MEDIA_URL`.
10. Configurar `MEDIA_ROOT`.
11. Ejecutar `collectstatic`.
12. Ejecutar `python manage.py check`.
13. Ejecutar `python manage.py check --deploy`.
14. Verificar que app sigue corriendo.
15. Documentar variables necesarias en README.

## 🟡 Nivel Intermedio (16–30)

1. Crear settings separados por entorno (base/dev/prod).
2. Activar Whitenoise para estáticos.
3. Validar cabeceras seguras básicas.
4. Configurar timezone e idioma correctamente.
5. Revisar dependencias obsoletas.
6. Definir política mínima de contraseñas.
7. Ajustar `CSRF_TRUSTED_ORIGINS` para dominio real.
8. Proteger cookies de sesión para producción.
9. Configurar logging básico de errores.
10. Crear script de checklist pre-deploy.
11. Validar configuración en entorno limpio.
12. Simular despliegue local con `DEBUG=False`.
13. Medir errores al servir estáticos.
14. Agregar validaciones de variables críticas.
15. Crear mini manual de hardening inicial.

## 🔵 Nivel Desafío (31–45)

1. Configurar entornos dev/staging/prod.
2. Automatizar instalación desde requirements.
3. Añadir validación fuerte de variables de entorno.
4. Configurar pipeline mínimo de verificación.
5. Integrar chequeos de seguridad recurrentes.
6. Crear estrategia de backup de base de datos.
7. Diseñar plan de rotación de secretos.
8. Definir política de logs y retención.
9. Probar rollback de configuración.
10. Documentar incidentes y respuesta.
11. Ajustar settings para múltiples dominios.
12. Configurar subida segura de media.
13. Testear comportamiento sin variables obligatorias.
14. Crear checklist final de salida a producción.
15. Entregar proyecto con hardening inicial listo.

## 🏁 Proyecto de cierre de clase

Preparar un proyecto Django con configuración segura mínima para deploy, documentada y verificable.
