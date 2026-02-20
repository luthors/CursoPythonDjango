# 💻 Clase 11 · Ejemplos de IA en Flujo de Desarrollo

<!-- markdownlint-configure-file {"MD024": {"siblings_only": true}} -->

[⬅️ Volver a la clase](Clase_11_IA_y_Prompt_Engineering.md) | [📦 Módulo](README.md)
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## Caso 1: Depurar error en función Python

### Prompt

```text
Actúa como desarrollador Python senior.
Tengo esta función y falla cuando recibe None.
Objetivo: hacerla robusta sin cambiar la firma.
Entrega: parche mínimo + ejemplo de prueba.
```

### Resultado esperado

- Validación de entrada.
- Manejo explícito de `None`.
- Prueba rápida con assert.

## Caso 2: Generar documentación técnica

### Prompt

```text
Resume esta función en formato docstring Google Style.
Incluye Args, Returns, Raises y ejemplo.
```

### Resultado esperado

- Docstring clara y útil para mantenimiento.

## Caso 3: Refactor con restricciones

### Prompt

```text
Refactoriza este bloque para reducir complejidad ciclomática.
No cambies comportamiento ni nombres públicos.
Entrega el código final y explica los cambios.
```

### Resultado esperado

- Funciones más pequeñas.
- Mejor legibilidad.
- Misma salida funcional.
