# ✅ Clase 04 · Ejercicios Resueltos (Selección)

[⬅️ Volver a la clase](Clase_04_Introduccion_Django.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## Resuelto 1: Vista `inicio` con `HttpResponse`

```python
# core/views.py
from django.http import HttpResponse

def inicio(request):
    return HttpResponse("Bienvenido al sitio")
```

## Resuelto 2: URL en app

```python
# core/urls.py
from django.urls import path
from . import views

urlpatterns = [
    path('', views.inicio, name='inicio'),
]
```

## Resuelto 3: Incluir URL de app en proyecto

```python
# proyecto/urls.py
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('core.urls')),
]
```

## Resuelto 4: Render con template

```python
# core/views.py
from django.shortcuts import render

def acerca(request):
    return render(request, 'core/acerca.html', {'titulo': 'Acerca de'})
```

```html
<!-- templates/core/acerca.html -->
<h1>{{ titulo }}</h1>
<p>Esta página usa templates de Django.</p>
```

## Resuelto 5: Herencia de templates

```html
<!-- templates/base.html -->
<!DOCTYPE html>
<html>
  <body>
    <nav>
      <a href="/">Inicio</a>
      <a href="/acerca/">Acerca</a>
      <a href="/contacto/">Contacto</a>
    </nav>
    {% block contenido %}{% endblock %}
  </body>
</html>
```

```html
<!-- templates/core/inicio.html -->
{% extends 'base.html' %} {% block contenido %}
<h1>Inicio</h1>
{% endblock %}
```

## Resuelto 6: Vista con parámetro en URL

```python
# core/urls.py
path('saludo/<str:nombre>/', views.saludo, name='saludo')
```

```python
# core/views.py
def saludo(request, nombre):
    return render(request, 'core/saludo.html', {'nombre': nombre})
```

```html
<!-- templates/core/saludo.html -->
<h1>Hola, {{ nombre }} 👋</h1>
```
