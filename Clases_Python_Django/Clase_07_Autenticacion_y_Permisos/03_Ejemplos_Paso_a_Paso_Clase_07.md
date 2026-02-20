# 🧪 Clase 07 · Ejemplos Paso a Paso

[⬅️ Volver a la clase](Clase_07_Autenticacion_y_Permisos.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## 1) Login con `AuthenticationForm`

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

---

## 2) Registro con `UserCreationForm`

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

---

## 3) Logout

```python
from django.contrib.auth import logout

def logout_view(request):
    logout(request)
    return redirect('login')
```

---

## 4) Proteger vista con `@login_required`

```python
from django.contrib.auth.decorators import login_required

@login_required
def producto_create(request):
    ...
```

---

## 5) Permiso por propietario

```python
from django.http import HttpResponseForbidden

@login_required
def producto_update(request, pk):
    producto = get_object_or_404(Producto, pk=pk)
    if producto.creado_por != request.user:
        return HttpResponseForbidden("No autorizado")
    ...
```

---

## 6) Template de login mínimo

```html
<h1>Iniciar sesión</h1>
<form method="post">
  {% csrf_token %} {{ form.as_p }}
  <button type="submit">Entrar</button>
</form>
```
