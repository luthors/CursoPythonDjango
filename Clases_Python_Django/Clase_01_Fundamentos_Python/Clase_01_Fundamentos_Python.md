# 🐍 Clase 01: Fundamentos de Programación con Python

[🏠 Volver al índice](../README.md)
[➡️ Siguiente clase](../Clase_02_Estructuras_y_Funciones/Clase_02_Estructuras_y_Funciones.md)

## 🎯 Tema

Introducción a Python y lógica básica de programación.

## 🧭 Objetivo general

Que el estudiante comprenda y aplique los pilares de programación inicial:

- Entrada de datos (`input`)
- Procesamiento (variables + operadores)
- Decisiones (`if/elif/else`)
- Salida de información (`print`)
- Identificación y corrección de errores comunes

## 🎯 Objetivos específicos

Al finalizar la clase, el estudiante podrá:

1. Definir con sus palabras qué es variable, condicional, input, output y error.
2. Escribir programas básicos con interacción por consola.
3. Tomar decisiones lógicas en código con condicionales.
4. Detectar errores comunes y corregirlos.

## 🧠 Explicación

En esta clase aprendes a comunicarte con el computador usando instrucciones simples. Verás cómo guardar datos en
variables, pedir información al usuario y tomar decisiones con condicionales.

La lógica base que practicarás es:

```text
Input → Procesamiento → Decisión → Output
```

## 🧱 Estructura de la clase

- **Objetivo:** escribir programas básicos que reciban datos y respondan correctamente.
- **Conceptos clave:** `print()`, `input()`, variables, tipos de datos, operadores, `if/elif/else`.
- **Práctica guiada:** calculadora + validador de edad + mini menú.
- **Reto:** cajero automático simple.

## 🗂️ Contenido enriquecido de la Clase 1

Para profundizar esta clase tienes material separado por enfoque:

- [📚 Glosario fundamental](01_Glosario_Fundamental.md)
- [🧪 Ejemplos paso a paso](02_Ejemplos_Paso_a_Paso.md)
- [🧩 Banco amplio de ejercicios](03_Ejercicios_Clase_01.md)
- [✅ Ejercicios resueltos (selección)](04_Ejercicios_Resueltos_Clase_01.md)

## 📊 Gráfico conceptual

```mermaid
flowchart TD
    A[Entrada con input()] --> B[Procesar lógica]
    B --> C{Condición}
    C -->|Verdadero| D[Mostrar resultado 1]
    C -->|Falso| E[Mostrar resultado 2]
    E --> F[Revisar errores y mejorar]
    D --> F
```

## 💻 Código de ejemplo

```python
nombre = input("¿Cuál es tu nombre? ")
edad = int(input("¿Cuál es tu edad? "))

if edad >= 18:
    print(f"Hola {nombre}, eres mayor de edad ✅")
else:
    print(f"Hola {nombre}, eres menor de edad 🧒")
```

## 🧩 Definiciones rápidas (resumen)

- **Variable:** contenedor con nombre para guardar datos.
- **Input:** datos que ingresan al programa (usuario/teclado).
- **Output:** datos que el programa muestra (pantalla/consola).
- **Condicional:** estructura para decidir qué camino seguir.
- **Error:** problema de sintaxis o lógica que impide el resultado esperado.

> Para definiciones completas y ejemplos por cada concepto, revisa el [glosario](01_Glosario_Fundamental.md).

## 🛠️ Práctica sugerida

1. Crear una calculadora de 2 números.
2. Validar si un usuario puede votar.
3. Crear un menú con 3 opciones y salida.

## 🏋️ Práctica ampliada recomendada

- Resolver ejercicios **1 al 15** del [banco de ejercicios](03_Ejercicios_Clase_01.md).
- Resolver **5 ejercicios** del nivel intermedio.
- Resolver **3 ejercicios** del nivel desafío.
- Revisar soluciones modelo en [resueltos](04_Ejercicios_Resueltos_Clase_01.md) solo después de intentar.

## ⏱️ Sugerencia de ritmo para clase de 2 horas

- 20 min: conceptos base y demostración.
- 35 min: práctica guiada en vivo.
- 45 min: ejercicios por niveles.
- 20 min: retroalimentación + cierre.

## 🧪 Criterios de evaluación rápida

- **Comprensión conceptual (30%)**: define correctamente los conceptos.
- **Implementación (40%)**: el código corre y resuelve el problema.
- **Lógica (20%)**: decisiones correctas con condicionales.
- **Orden y claridad (10%)**: nombres de variables y mensajes claros.

## ✅ Checklist

- [ ] Entiendo qué es una variable.
- [ ] Puedo usar `if/else`.
- [ ] Puedo pedir datos con `input()`.
- [ ] Mi programa ejecuta sin errores.
- [ ] Intenté ejercicios de los tres niveles.
- [ ] Puedo explicar al menos 5 errores comunes de principiante.

---

## 🚀 Entregable de la Clase 1

Subir un archivo `clase1_reto.py` con:

1. Menú interactivo.
2. Validación de entrada numérica.
3. Módulo de mayoría de edad.
4. Calculadora básica.
5. Mensajes claros para casos válidos e inválidos.
