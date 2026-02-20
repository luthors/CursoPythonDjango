# 🧩 Clase 05 · Repertorio Amplio de Ejercicios

[⬅️ Volver a la clase](Clase_05_Modelos_y_Base_de_Datos.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## 🟢 Nivel Básico (1–15)

1. Crear modelo `Categoria` con campo `nombre`.
2. Crear modelo `Producto` con `nombre` y `precio`.
3. Agregar relación `Producto -> Categoria`.
4. Ejecutar `makemigrations` y `migrate`.
5. Crear superusuario.
6. Registrar modelos en admin.
7. Insertar 3 categorías desde admin.
8. Insertar 5 productos desde admin.
9. Mostrar `__str__` legible en ambos modelos.
10. Agregar campo `descripcion` a `Producto`.
11. Agregar campo booleano `activo`.
12. Aplicar nueva migración correctamente.
13. Entrar al shell y contar productos.
14. Filtrar productos activos en shell.
15. Ordenar productos por nombre.

## 🟡 Nivel Intermedio (16–30)

1. Crear modelo `Marca` relacionado con `Producto`.
2. Proteger borrado de marca con `PROTECT`.
3. Crear modelo `Proveedor`.
4. Relacionar `Producto` con `Proveedor`.
5. Añadir campo `stock` entero a producto.
6. Filtrar productos con stock bajo.
7. Mostrar en admin columnas clave personalizadas.
8. Buscar productos por nombre en admin.
9. Agregar fecha de creación con `auto_now_add`.
10. Agregar fecha de actualización con `auto_now`.
11. Crear consulta por rango de precios.
12. Crear consulta por categoría específica.
13. Validar que precio no sea negativo (a nivel de lógica).
14. Crear carga inicial de datos de prueba.
15. Documentar modelos y relaciones en markdown.

## 🔵 Nivel Desafío (31–45)

1. Modelar tienda completa con `Categoria`, `Marca`, `Producto`, `Proveedor`.
2. Agregar modelo `Inventario` separado por producto.
3. Simular historial de cambios de precio.
4. Diseñar relación de producto con múltiples etiquetas.
5. Configurar relación muchos-a-muchos con `Tag`.
6. Crear consultas complejas por varias condiciones.
7. Crear datos por script en shell.
8. Estructurar admin para gestión eficiente.
9. Definir estrategia de borrado segura (`on_delete`).
10. Crear diagrama ER del esquema.
11. Preparar datos para siguiente clase CRUD.
12. Validar integridad de relaciones.
13. Probar eliminación de categoría con productos asociados.
14. Medir impacto de consultas frecuentes.
15. Entregar mini módulo de datos listo para producción inicial.

## 🏁 Proyecto de cierre de clase

Construir el módulo de datos para una tienda: categorías, productos, marcas y proveedores, con relaciones coherentes y
administración funcional.
