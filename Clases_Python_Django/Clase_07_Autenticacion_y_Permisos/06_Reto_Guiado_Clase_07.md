# 🧠 Clase 07 · Reto Guiado: Seguridad Básica en CRUD

[⬅️ Volver a la clase](Clase_07_Autenticacion_y_Permisos.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## 🎯 Objetivo

Proteger completamente el módulo CRUD para que solo usuarios autorizados puedan operar.

## 🧱 Requisitos

- Login, registro y logout funcionales.
- Crear productos solo para usuarios autenticados.
- Editar/eliminar solo para el creador del producto.
- Mensajes claros de acceso denegado.
- Navegación adaptada al estado de sesión.

## 🪜 Paso a paso sugerido

1. Configurar rutas de auth.
2. Implementar formularios y vistas de login/registro.
3. Proteger vistas con `@login_required`.
4. Asignar propietario al crear producto.
5. Validar propietario en update/delete.
6. Probar con dos usuarios distintos.

## ✅ Criterios de logro

- No autenticados no acceden a vistas protegidas.
- Usuario A no puede editar/eliminar recursos de usuario B.
- Flujo completo estable y sin errores.

## 📌 Extensión opcional

- Crear roles con grupos.
- Restringir acciones adicionales por rol.
- Añadir logging de eventos de seguridad básicos.
