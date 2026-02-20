# 🧪 Clase 04 · Ejemplos Paso a Paso

[⬅️ Volver a la clase](Clase_04_Introduccion_Django.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## 1) Primera vista con `HttpResponse`

```python
# core/views.py
from django.http import HttpResponse

def inicio(request):
    return HttpResponse("Hola desde Django 🚀")
```

---

## 2) Enlazar vista en URLs de la app

```python
# core/urls.py
from django.urls import path
from . import views

urlpatterns = [
    path('', views.inicio, name='inicio'),
]
```

---

## 3) Incluir URLs de la app en el proyecto

```python
# mi_proyecto/urls.py
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('core.urls')),
]
```

---

## 4) Usar templates en vez de texto plano

```python
# core/views.py
from django.shortcuts import render

def acerca_de(request):
    return render(request, 'core/acerca_de.html')
```

```html
<!-- templates/core/acerca_de.html -->
<h1>Acerca de</h1>
<p>Primera página en Django con template.</p>
```

---

## 5) Tres páginas base del sitio

```python
# core/views.py
from django.shortcuts import render

def inicio(request):
    return render(request, 'core/inicio.html')

def acerca(request):
    return render(request, 'core/acerca.html')

def contacto(request):
    return render(request, 'core/contacto.html')
```

```python
# core/urls.py
from django.urls import path
from . import views

urlpatterns = [
    path('', views.inicio, name='inicio'),
    path('acerca/', views.acerca, name='acerca'),
    path('contacto/', views.contacto, name='contacto'),
]
```
