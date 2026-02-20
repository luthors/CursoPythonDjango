# ✅ Clase 11 · Ejercicios Resueltos

<!-- markdownlint-configure-file {"MD024": {"siblings_only": true}} -->

[⬅️ Volver a la clase](Clase_11_IA_y_Prompt_Engineering.md) | [📦 Módulo](README.md)
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## Resuelto 1 · Prompt de depuración

### Entrada

```python
def precio_total(precio, iva):
    return precio + precio * iva
```

### Prompt

```text
Encuentra riesgos de esta función y mejora robustez sin cambiar su intención.
```

### Solución sugerida

```python
def precio_total(precio, iva):
    if precio is None or iva is None:
        raise ValueError("precio e iva son obligatorios")
    if precio < 0:
        raise ValueError("precio no puede ser negativo")
    return precio + precio * iva
```

## Resuelto 2 · Prompt para tests

### Prompt

```text
Genera tests pytest para precio_total con caso feliz, inválido y borde.
```

### Resultado (ejemplo)

```python
import pytest

from app.utils import precio_total


def test_precio_total_caso_feliz():
    assert precio_total(100, 0.19) == 119


def test_precio_total_none():
    with pytest.raises(ValueError):
        precio_total(None, 0.19)
```

## Resuelto 3 · Prompt de documentación

### Prompt

```text
Genera docstring tipo Google para precio_total.
```

### Resultado esperado

Docstring breve, precisa y con ejemplos de uso.
