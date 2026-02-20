# 🧰 Clase 11 · Guía de Prompts para Programación

[⬅️ Volver a la clase](Clase_11_IA_y_Prompt_Engineering.md) | [📦 Módulo](README.md)
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## Estructura recomendada de prompt

1. **Rol:** “Actúa como desarrollador Python senior”.
2. **Contexto:** proyecto, archivo, función y objetivo.
3. **Tarea precisa:** qué debe hacer exactamente.
4. **Restricciones:** no cambiar API, no usar librerías extra, mantener estilo.
5. **Salida esperada:** formato concreto (pasos, diff, tests, explicación breve).

## Plantillas útiles

### 1) Debug

```text
Actúa como mentor Python.
Contexto: {archivo/función}
Error: {mensaje exacto}
Objetivo: corregir sin cambiar comportamiento externo.
Entrega: causa raíz, parche mínimo, prueba de validación.
```

### 2) Refactor

```text
Refactoriza esta función para mejorar legibilidad y mantener la misma salida.
Restricciones: no cambiar nombre público, no añadir dependencias.
Entrega: código final + explicación en 5 puntos.
```

### 3) Generar tests

```text
Genera tests unitarios para esta función.
Incluye: caso feliz, caso borde, caso inválido.
Usa pytest y nombres descriptivos.
```

## Antipatrones de prompt

- Pedir “hazlo mejor” sin contexto.
- No definir restricciones técnicas.
- Aceptar respuesta sin ejecutar pruebas.
- Usar código generado sin revisión de seguridad.
