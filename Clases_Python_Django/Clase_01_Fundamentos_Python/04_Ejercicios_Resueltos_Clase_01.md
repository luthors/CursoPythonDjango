# ✅ Clase 01 · Ejercicios Resueltos (Selección)

[⬅️ Volver a la clase](Clase_01_Fundamentos_Python.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## Resuelto 1: Par o impar

```python
numero = int(input("Ingresa un número: "))

if numero % 2 == 0:
    print("El número es par")
else:
    print("El número es impar")
```

## Resuelto 2: Mayor de tres números

```python
a = float(input("Número A: "))
b = float(input("Número B: "))
c = float(input("Número C: "))

mayor = a
if b > mayor:
    mayor = b
if c > mayor:
    mayor = c

print("El mayor es:", mayor)
```

## Resuelto 3: Calculadora con operación elegida

```python
n1 = float(input("Número 1: "))
n2 = float(input("Número 2: "))
op = input("Operación (+, -, *, /): ")

if op == "+":
    print("Resultado:", n1 + n2)
elif op == "-":
    print("Resultado:", n1 - n2)
elif op == "*":
    print("Resultado:", n1 * n2)
elif op == "/":
    if n2 != 0:
        print("Resultado:", n1 / n2)
    else:
        print("No se puede dividir por cero")
else:
    print("Operación no válida")
```

## Resuelto 4: Menú básico

```python
print("1. Ver saludo")
print("2. Ver despedida")
print("3. Salir")

opcion = input("Selecciona una opción: ")

if opcion == "1":
    print("Hola, bienvenido/a")
elif opcion == "2":
    print("Gracias por practicar")
elif opcion == "3":
    print("Programa finalizado")
else:
    print("Opción inválida")
```

## Resuelto 5: Validador de edad y voto

```python
edad = int(input("Ingresa tu edad: "))

if edad >= 18:
    print("Puedes votar ✅")
else:
    faltan = 18 - edad
    print("Aún no puedes votar. Te faltan", faltan, "años")
```

## Resuelto 6: Descuento en compra

```python
precio = float(input("Precio original: "))
desc = float(input("Descuento (%): "))

monto_descuento = precio * (desc / 100)
precio_final = precio - monto_descuento

print("Descuento aplicado:", monto_descuento)
print("Precio final:", precio_final)
```

## Resuelto 7: Cajero simple

```python
saldo = 500000
print("1. Consultar saldo")
print("2. Depositar")
print("3. Retirar")
opcion = input("Elige una opción: ")

if opcion == "1":
    print("Saldo:", saldo)
elif opcion == "2":
    monto = int(input("Monto a depositar: "))
    if monto > 0:
        saldo += monto
        print("Nuevo saldo:", saldo)
    else:
        print("Monto inválido")
elif opcion == "3":
    monto = int(input("Monto a retirar: "))
    if monto <= 0:
        print("Monto inválido")
    elif monto > saldo:
        print("Fondos insuficientes")
    else:
        saldo -= monto
        print("Retiro exitoso. Saldo:", saldo)
else:
    print("Opción inválida")
```

## 🎯 Siguiente paso

Resuelve primero 10 ejercicios del archivo de práctica y luego compara tu solución con estos patrones.
