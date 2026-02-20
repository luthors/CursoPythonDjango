# 🧪 Clase 01 · Ejemplos Paso a Paso

[⬅️ Volver a la clase](Clase_01_Fundamentos_Python.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## 1) Saludo interactivo

```python
nombre = input("¿Cómo te llamas? ")
print(f"Hola, {nombre}. ¡Bienvenido/a al curso!")
```

**Qué practica:** `input`, variables, `print`.

---

## 2) Calculadora básica

```python
a = float(input("Número 1: "))
b = float(input("Número 2: "))

print("Suma:", a + b)
print("Resta:", a - b)
print("Multiplicación:", a * b)
print("División:", a / b)
```

**Qué practica:** conversión de datos y operadores.

---

## 3) Validación de mayoría de edad

```python
edad = int(input("Edad: "))

if edad >= 18:
    print("Puedes ingresar ✅")
else:
    print("Acceso restringido ❌")
```

**Qué practica:** condicionales.

---

## 4) Verificar número par o impar

```python
n = int(input("Ingresa un número: "))

if n % 2 == 0:
    print("Es par")
else:
    print("Es impar")
```

**Qué practica:** operador módulo `%` + decisión.

---

## 5) Menú simple

```python
print("1. Saludar")
print("2. Mostrar fecha (texto)")
print("3. Salir")
opcion = input("Elige una opción: ")

if opcion == "1":
    print("Hola 👋")
elif opcion == "2":
    print("Hoy es un gran día para programar")
elif opcion == "3":
    print("Hasta luego")
else:
    print("Opción inválida")
```

**Qué practica:** ramas múltiples con `if/elif/else`.

---

## 6) Manejo básico de errores de entrada

```python
texto = input("Ingresa un número entero: ")

if texto.isdigit():
    numero = int(texto)
    print("El doble es:", numero * 2)
else:
    print("Entrada inválida. Debes ingresar solo dígitos.")
```

**Qué practica:** validación previa para evitar errores.

---

## 7) Mini cajero (versión inicial)

```python
saldo = 100000
opcion = input("1. Consultar  2. Depositar  3. Retirar: ")

if opcion == "1":
    print("Saldo actual:", saldo)
elif opcion == "2":
    monto = int(input("Monto a depositar: "))
    saldo = saldo + monto
    print("Nuevo saldo:", saldo)
elif opcion == "3":
    monto = int(input("Monto a retirar: "))
    if monto <= saldo:
        saldo = saldo - monto
        print("Retiro exitoso. Saldo:", saldo)
    else:
        print("Fondos insuficientes")
else:
    print("Opción no válida")
```

**Qué practica:** flujo completo de entrada, procesamiento y salida.
