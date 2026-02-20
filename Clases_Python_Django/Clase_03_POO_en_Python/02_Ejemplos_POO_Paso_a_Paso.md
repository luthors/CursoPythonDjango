# 🧪 Clase 03 · Ejemplos POO Paso a Paso

[⬅️ Volver a la clase](Clase_03_POO_en_Python.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## 1) Primera clase y objeto

```python
class Persona:
    def __init__(self, nombre):
        self.nombre = nombre

    def presentarse(self):
        return f"Hola, soy {self.nombre}"

p = Persona("Luisa")
print(p.presentarse())
```

---

## 2) Clase Producto con lógica simple

```python
class Producto:
    def __init__(self, nombre, precio):
        self.nombre = nombre
        self.precio = precio

    def aplicar_descuento(self, porcentaje):
        self.precio = self.precio - (self.precio * porcentaje / 100)

teclado = Producto("Teclado", 120000)
teclado.aplicar_descuento(10)
print(teclado.precio)
```

---

## 3) Asociación entre Usuario y Pedido

```python
class Usuario:
    def __init__(self, nombre):
        self.nombre = nombre

class Pedido:
    def __init__(self, usuario, total):
        self.usuario = usuario
        self.total = total

u1 = Usuario("Carlos")
ped1 = Pedido(u1, 350000)
print(ped1.usuario.nombre, ped1.total)
```

---

## 4) Clase Pedido con lista de productos

```python
class Pedido:
    def __init__(self, usuario):
        self.usuario = usuario
        self.productos = []

    def agregar_producto(self, producto):
        self.productos.append(producto)

    def total(self):
        suma = 0
        for p in self.productos:
            suma += p.precio
        return suma
```

---

## 5) Encapsulamiento básico

```python
class CuentaBancaria:
    def __init__(self, saldo_inicial):
        self._saldo = saldo_inicial

    def depositar(self, monto):
        if monto > 0:
            self._saldo += monto

    def ver_saldo(self):
        return self._saldo
```

---

## 6) Herencia básica

```python
class Persona:
    def __init__(self, nombre):
        self.nombre = nombre

class Empleado(Persona):
    def __init__(self, nombre, cargo):
        super().__init__(nombre)
        self.cargo = cargo

e1 = Empleado("Ana", "Desarrolladora")
print(e1.nombre, e1.cargo)
```

---

## 7) Polimorfismo simple

```python
class Animal:
    def sonido(self):
        return "..."

class Perro(Animal):
    def sonido(self):
        return "Guau"

class Gato(Animal):
    def sonido(self):
        return "Miau"

animales = [Perro(), Gato()]
for a in animales:
    print(a.sonido())
```
