# ✅ Clase 03 · Ejercicios Resueltos (Selección POO)

[⬅️ Volver a la clase](Clase_03_POO_en_Python.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## Resuelto 1: Clase Persona

```python
class Persona:
    def __init__(self, nombre):
        self.nombre = nombre

    def saludar(self):
        return f"Hola, soy {self.nombre}"

p = Persona("Laura")
print(p.saludar())
```

## Resuelto 2: Clase Producto con descuento

```python
class Producto:
    def __init__(self, nombre, precio):
        self.nombre = nombre
        self.precio = precio

    def aplicar_descuento(self, porcentaje):
        self.precio -= self.precio * porcentaje / 100

mouse = Producto("Mouse", 80000)
mouse.aplicar_descuento(15)
print(mouse.precio)
```

## Resuelto 3: Clase Pedido con total

```python
class Pedido:
    def __init__(self):
        self.productos = []

    def agregar(self, producto):
        self.productos.append(producto)

    def total(self):
        return sum(p.precio for p in self.productos)
```

## Resuelto 4: Encapsulamiento básico en cuenta

```python
class Cuenta:
    def __init__(self, saldo):
        self._saldo = saldo

    def depositar(self, monto):
        if monto > 0:
            self._saldo += monto

    def retirar(self, monto):
        if 0 < monto <= self._saldo:
            self._saldo -= monto

    def saldo_actual(self):
        return self._saldo

c = Cuenta(100000)
c.depositar(50000)
c.retirar(20000)
print(c.saldo_actual())
```

## Resuelto 5: Herencia con super()

```python
class Persona:
    def __init__(self, nombre):
        self.nombre = nombre

class Empleado(Persona):
    def __init__(self, nombre, cargo):
        super().__init__(nombre)
        self.cargo = cargo

e = Empleado("Juan", "QA")
print(e.nombre, e.cargo)
```

## Resuelto 6: Polimorfismo

```python
class Notificacion:
    def enviar(self):
        return "Enviando..."

class Email(Notificacion):
    def enviar(self):
        return "Email enviado"

class SMS(Notificacion):
    def enviar(self):
        return "SMS enviado"

canales = [Email(), SMS()]
for canal in canales:
    print(canal.enviar())
```

## Resuelto 7: Sistema mínimo Usuario-Producto-Pedido

```python
class Usuario:
    def __init__(self, nombre):
        self.nombre = nombre

class Producto:
    def __init__(self, nombre, precio):
        self.nombre = nombre
        self.precio = precio

class Pedido:
    def __init__(self, usuario):
        self.usuario = usuario
        self.productos = []

    def agregar_producto(self, producto):
        self.productos.append(producto)

    def total(self):
        return sum(p.precio for p in self.productos)

u = Usuario("Ana")
p1 = Producto("Teclado", 120000)
p2 = Producto("Mouse", 70000)

pedido = Pedido(u)
pedido.agregar_producto(p1)
pedido.agregar_producto(p2)

print("Cliente:", pedido.usuario.nombre)
print("Total:", pedido.total())
```
