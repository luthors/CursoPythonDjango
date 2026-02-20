# 🧪 Clase 05 · Ejemplos Paso a Paso

[⬅️ Volver a la clase](Clase_05_Modelos_y_Base_de_Datos.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## 1) Definir modelos básicos

```python
# app/models.py
from django.db import models

class Categoria(models.Model):
    nombre = models.CharField(max_length=100)

    def __str__(self):
        return self.nombre

class Producto(models.Model):
    nombre = models.CharField(max_length=120)
    precio = models.DecimalField(max_digits=10, decimal_places=2)
    categoria = models.ForeignKey(Categoria, on_delete=models.CASCADE)

    def __str__(self):
        return self.nombre
```

---

## 2) Registrar modelos en admin

```python
# app/admin.py
from django.contrib import admin
from .models import Categoria, Producto

admin.site.register(Categoria)
admin.site.register(Producto)
```

---

## 3) Crear datos con ORM

```python
from app.models import Categoria, Producto

cat = Categoria.objects.create(nombre="Laptops")
Producto.objects.create(nombre="Ultrabook", precio=3500000, categoria=cat)
```

---

## 4) Consultar y filtrar datos

```python
productos = Producto.objects.all()
caros = Producto.objects.filter(precio__gte=1000000)

for p in caros:
    print(p.nombre, p.precio)
```

---

## 5) Modelo adicional relacionado

```python
class Marca(models.Model):
    nombre = models.CharField(max_length=100)

class Producto(models.Model):
    nombre = models.CharField(max_length=120)
    precio = models.DecimalField(max_digits=10, decimal_places=2)
    categoria = models.ForeignKey(Categoria, on_delete=models.CASCADE)
    marca = models.ForeignKey(Marca, on_delete=models.PROTECT)
```
