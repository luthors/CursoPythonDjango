# ✅ Clase 07 · Ejercicios Resueltos (Selección)

[⬅️ Volver a la clase](Clase_07_Autenticacion_y_Permisos.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## Resuelto 1: Login view

```python
from django.contrib.auth import login
from django.contrib.auth.forms import AuthenticationForm
from django.shortcuts import render, redirect

def login_view(request):
    form = AuthenticationForm(request, data=request.POST or None)
    if request.method == 'POST' and form.is_valid():
        login(request, form.get_user())
        return redirect('producto_list')
    return render(request, 'auth/login.html', {'form': form})
```

## Resuelto 2: Register view

```python
from django.contrib.auth.forms import UserCreationForm

def register_view(request):
    form = UserCreationForm(request.POST or None)
    if request.method == 'POST' and form.is_valid():
        user = form.save()
        login(request, user)
        return redirect('producto_list')
    return render(request, 'auth/register.html', {'form': form})
```

## Resuelto 3: Proteger create con login

```python
from django.contrib.auth.decorators import login_required

@login_required
def producto_create(request):
    form = ProductoForm(request.POST or None)
    if form.is_valid():
        producto = form.save(commit=False)
        producto.creado_por = request.user
        producto.save()
        return redirect('producto_list')
    return render(request, 'productos/form.html', {'form': form})
```

## Resuelto 4: Restricción por propietario en update

```python
from django.http import HttpResponseForbidden

@login_required
def producto_update(request, pk):
    producto = get_object_or_404(Producto, pk=pk)
    if producto.creado_por != request.user:
        return HttpResponseForbidden('No autorizado')
    form = ProductoForm(request.POST or None, instance=producto)
    if form.is_valid():
        form.save()
        return redirect('producto_list')
    return render(request, 'productos/form.html', {'form': form})
```

## Resuelto 5: Logout

```python
from django.contrib.auth import logout

def logout_view(request):
    logout(request)
    return redirect('login')
```
