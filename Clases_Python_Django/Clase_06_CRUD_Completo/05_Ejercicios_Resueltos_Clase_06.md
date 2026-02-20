# ✅ Clase 06 · Ejercicios Resueltos (Selección)

[⬅️ Volver a la clase](Clase_06_CRUD_Completo.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## Resuelto 1: `ProductoForm`

```python
from django import forms
from .models import Producto

class ProductoForm(forms.ModelForm):
    class Meta:
        model = Producto
        fields = ['nombre', 'precio', 'categoria']
```

## Resuelto 2: Vista list + create

```python
from django.shortcuts import render, redirect
from .models import Producto
from .forms import ProductoForm

def producto_list(request):
    productos = Producto.objects.all()
    return render(request, 'productos/list.html', {'productos': productos})

def producto_create(request):
    form = ProductoForm(request.POST or None)
    if form.is_valid():
        form.save()
        return redirect('producto_list')
    return render(request, 'productos/form.html', {'form': form})
```

## Resuelto 3: Vista update + delete

```python
from django.shortcuts import get_object_or_404

def producto_update(request, pk):
    producto = get_object_or_404(Producto, pk=pk)
    form = ProductoForm(request.POST or None, instance=producto)
    if form.is_valid():
        form.save()
        return redirect('producto_list')
    return render(request, 'productos/form.html', {'form': form})


def producto_delete(request, pk):
    producto = get_object_or_404(Producto, pk=pk)
    if request.method == 'POST':
        producto.delete()
        return redirect('producto_list')
    return render(request, 'productos/confirm_delete.html', {'producto': producto})
```

## Resuelto 4: URLs CRUD

```python
from django.urls import path
from . import views

urlpatterns = [
    path('productos/', views.producto_list, name='producto_list'),
    path('productos/crear/', views.producto_create, name='producto_create'),
    path('productos/<int:pk>/editar/', views.producto_update, name='producto_update'),
    path('productos/<int:pk>/eliminar/', views.producto_delete, name='producto_delete'),
]
```

## Resuelto 5: Template listado básico

```html
<h1>Productos</h1>
<a href="{% url 'producto_create' %}">Crear producto</a>
<ul>
  {% for p in productos %}
  <li>
    {{ p.nombre }} - {{ p.precio }}
    <a href="{% url 'producto_update' p.id %}">Editar</a>
    <a href="{% url 'producto_delete' p.id %}">Eliminar</a>
  </li>
  {% empty %}
  <li>No hay productos.</li>
  {% endfor %}
</ul>
```
