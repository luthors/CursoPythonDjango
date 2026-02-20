# 🧰 Clase 05 · Comandos: Migraciones y Admin

[⬅️ Volver a la clase](Clase_05_Modelos_y_Base_de_Datos.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## Flujo mínimo recomendado

```bash
# 1) Crear migraciones según cambios en models.py
python manage.py makemigrations

# 2) Aplicar migraciones a la base de datos
python manage.py migrate

# 3) Crear usuario administrador
python manage.py createsuperuser

# 4) Levantar servidor
python manage.py runserver
```

## Comandos de inspección útiles

```bash
python manage.py showmigrations
python manage.py sqlmigrate app 0001
python manage.py shell
```

## Prueba rápida en shell

```python
from app.models import Categoria, Producto
c = Categoria.objects.create(nombre="Periféricos")
Producto.objects.create(nombre="Mouse", precio=75000, categoria=c)
print(Producto.objects.count())
```
