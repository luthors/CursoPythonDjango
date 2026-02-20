# 🧰 Clase 06 · Estructura recomendada para CRUD

[⬅️ Volver a la clase](Clase_06_CRUD_Completo.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## Estructura mínima sugerida

```text
app/
├─ models.py
├─ forms.py
├─ views.py
├─ urls.py
├─ templates/
│  ├─ base.html
│  └─ productos/
│     ├─ list.html
│     ├─ form.html
│     └─ confirm_delete.html
```

## Archivos clave

- `models.py`: define entidad `Producto`.
- `forms.py`: define `ProductoForm`.
- `views.py`: funciones list/create/update/delete.
- `urls.py`: rutas por operación.
- `templates`: interfaz de usuario.

## Rutas sugeridas

- `/productos/` → listar
- `/productos/crear/` → crear
- `/productos/<id>/editar/` → actualizar
- `/productos/<id>/eliminar/` → eliminar
