# 🗺️ Clase 03 · Diagramas de apoyo (POO)

[⬅️ Volver a la clase](Clase_03_POO_en_Python.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## Diagrama UML básico

```mermaid
classDiagram
    class Usuario {
        +nombre
        +correo
        +mostrar_perfil()
    }

    class Producto {
        +nombre
        +precio
        +mostrar_info()
    }

    class Pedido {
        +usuario
        +productos
        +agregar_producto(p)
        +calcular_total()
    }

    Usuario "1" --> "*" Pedido : realiza
    Pedido "1" --> "*" Producto : contiene
```

## Flujo de creación de pedido

```mermaid
flowchart LR
    A[Crear Usuario] --> B[Crear Productos]
    B --> C[Instanciar Pedido]
    C --> D[Agregar productos]
    D --> E[Calcular total]
    E --> F[Mostrar resumen]
```
