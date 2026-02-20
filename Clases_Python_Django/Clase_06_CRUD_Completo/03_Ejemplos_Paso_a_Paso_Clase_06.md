# 🧪 Clase 06 · Ejemplos Paso a Paso

[⬅️ Volver a la clase](Clase_06_CRUD_Completo.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## 1) Formulario de modelo

```python
# forms.py
from django import forms
from .models import Producto

class ProductoForm(forms.ModelForm):
    class Meta:
        model = Producto
        fields = ['nombre', 'precio', 'categoria']
```

---

## 2) Listar productos

```python
# views.py
def producto_list(request):
    productos = Producto.objects.all()
    return render(request, 'productos/list.html', {'productos': productos})
```

---

## 3) Crear producto

```python
def producto_create(request):
    form = ProductoForm(request.POST or None)
    if form.is_valid():
        form.save()
        return redirect('producto_list')
    return render(request, 'productos/form.html', {'form': form})
```

---

## 4) Editar producto

```python
def producto_update(request, pk):
    producto = get_object_or_404(Producto, pk=pk)
    form = ProductoForm(request.POST or None, instance=producto)
    if form.is_valid():
        form.save()
        return redirect('producto_list')
    return render(request, 'productos/form.html', {'form': form})
```

---

## 5) Eliminar producto

```python
def producto_delete(request, pk):
    producto = get_object_or_404(Producto, pk=pk)
    if request.method == 'POST':
        producto.delete()
        return redirect('producto_list')
    return render(request, 'productos/confirm_delete.html', {'producto': producto})
```

---

## 6) URLs CRUD

```python
# urls.py
urlpatterns = [
    path('productos/', views.producto_list, name='producto_list'),
    path('productos/crear/', views.producto_create, name='producto_create'),
    path('productos/<int:pk>/editar/', views.producto_update, name='producto_update'),
    path('productos/<int:pk>/eliminar/', views.producto_delete, name='producto_delete'),
]
```
