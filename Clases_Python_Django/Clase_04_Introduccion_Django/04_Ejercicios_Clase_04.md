# 🧩 Clase 04 · Repertorio Amplio de Ejercicios

[⬅️ Volver a la clase](Clase_04_Introduccion_Django.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## 🟢 Nivel Básico (1–15)

1. Instalar Django en entorno virtual.
2. Crear proyecto llamado `sitio_curso`.
3. Crear app `core`.
4. Registrar app en `INSTALLED_APPS`.
5. Crear vista `inicio` con `HttpResponse`.
6. Crear ruta raíz para `inicio`.
7. Levantar servidor con `runserver`.
8. Crear vista `acerca`.
9. Crear vista `contacto`.
10. Conectar rutas para `acerca` y `contacto`.
11. Verificar las tres rutas en navegador.
12. Reemplazar `HttpResponse` por template en `inicio`.
13. Crear carpeta `templates/core`.
14. Crear archivo `inicio.html` básico.
15. Renderizar `inicio.html` desde la vista.

## 🟡 Nivel Intermedio (16–30)

1. Crear layout base `base.html`.
2. Hacer herencia de templates con `{% extends %}`.
3. Agregar navbar con enlaces a 3 páginas.
4. Agregar pie de página reutilizable.
5. Pasar contexto desde vista a template.
6. Mostrar nombre de curso dinámico en template.
7. Mostrar año actual (fijo o por contexto).
8. Crear página `servicios`.
9. Crear página `faq`.
10. Configurar `STATIC_URL` y cargar CSS simple.
11. Agregar archivo CSS propio.
12. Mostrar lista simple en template usando `{% for %}`.
13. Agregar validación de URL inexistente (página 404 por defecto).
14. Reorganizar URLs por app (`core/urls.py`).
15. Documentar estructura de carpetas del proyecto.

## 🔵 Nivel Desafío (31–45)

1. Crear mini sitio institucional de 5 páginas.
2. Añadir página `equipo` con datos dinámicos desde vista.
3. Añadir página `blog` con posts simulados en lista Python.
4. Crear vista que reciba parámetro en URL (`/saludo/<nombre>/`).
5. Renderizar saludo personalizado en template.
6. Crear vista de detalle simple con parámetro numérico.
7. Añadir plantilla reutilizable para tarjetas.
8. Integrar Bootstrap por CDN en `base.html`.
9. Aplicar diseño responsive básico.
10. Crear menú activo según ruta actual (simple).
11. Separar templates por secciones.
12. Crear carpeta `static/core` y usar archivo CSS local.
13. Crear archivo `README` técnico de arranque del proyecto.
14. Validar que todo funcione al clonar en otra máquina.
15. Entregar mini proyecto navegable y ordenado.

## 🏁 Proyecto de cierre de clase

Construir un **sitio de presentación** con mínimo 5 páginas, templates heredados y navegación completa.
