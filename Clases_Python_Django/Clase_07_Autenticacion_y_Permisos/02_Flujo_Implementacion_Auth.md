# 🧰 Clase 07 · Flujo de Implementación de Auth

[⬅️ Volver a la clase](Clase_07_Autenticacion_y_Permisos.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## Flujo recomendado

1. Configurar URLs de autenticación.
2. Crear vistas/templates de login y registro.
3. Añadir `@login_required` a vistas sensibles.
4. Validar propiedad del recurso en update/delete.
5. Agregar mensajes para feedback.

## Configuración base en `settings.py`

```python
LOGIN_URL = 'login'
LOGIN_REDIRECT_URL = 'producto_list'
LOGOUT_REDIRECT_URL = 'login'
```

## Rutas sugeridas

```python
path('login/', views.login_view, name='login')
path('logout/', views.logout_view, name='logout')
path('registro/', views.register_view, name='register')
```
