# 🧠 Clase 02 · Reto Guiado: CRUD Modular de Usuarios

[⬅️ Volver a la clase](Clase_02_Estructuras_y_Funciones.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## 🎯 Objetivo

Construir un sistema en consola con funciones separadas para cada operación CRUD.

## 🧱 Requisitos

- Lista de diccionarios para almacenar usuarios.
- Funciones mínimas: `crear`, `listar`, `actualizar`, `eliminar`, `menu`.
- Validación de índices.
- Salida clara de mensajes.

## 🪜 Paso a paso sugerido

1. Crear la lista `usuarios = []`.
2. Implementar `crear_usuario()`.
3. Implementar `listar_usuarios()`.
4. Implementar `actualizar_usuario(indice)`.
5. Implementar `eliminar_usuario(indice)`.
6. Conectar todo en `menu()` con `while True`.

## ✅ Criterios de logro

- El programa no se cae con entradas inválidas.
- El CRUD funciona de principio a fin.
- El código está separado en funciones legibles.

## 📌 Extensión opcional

- Agregar campo `activo`.
- Permitir buscar usuario por nombre.
- Mostrar total de usuarios registrados.
