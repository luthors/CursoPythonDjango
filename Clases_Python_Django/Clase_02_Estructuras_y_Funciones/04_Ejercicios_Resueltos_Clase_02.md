# ✅ Clase 02 · Ejercicios Resueltos (Selección)

[⬅️ Volver a la clase](Clase_02_Estructuras_y_Funciones.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## Resuelto 1: Promedio de notas

```python
def promedio(notas):
    if len(notas) == 0:
        return 0
    return sum(notas) / len(notas)

print(promedio([3.5, 4.0, 4.8]))
```

## Resuelto 2: Contar pares en lista

```python
def contar_pares(numeros):
    total = 0
    for n in numeros:
        if n % 2 == 0:
            total += 1
    return total

print(contar_pares([1, 2, 3, 4, 8]))  # 3
```

## Resuelto 3: Buscar usuario por nombre

```python
def buscar_usuario(usuarios, nombre):
    for u in usuarios:
        if u["nombre"].lower() == nombre.lower():
            return u
    return None

data = [{"nombre": "Ana", "correo": "a@mail.com"}]
print(buscar_usuario(data, "ana"))
```

## Resuelto 4: Actualizar usuario por índice

```python
def actualizar_usuario(usuarios, indice, nuevo_nombre):
    if 0 <= indice < len(usuarios):
        usuarios[indice]["nombre"] = nuevo_nombre
        return True
    return False

usuarios = [{"nombre": "Luis"}, {"nombre": "Marta"}]
ok = actualizar_usuario(usuarios, 1, "Martha")
print("Actualizado:", ok)
print(usuarios)
```

## Resuelto 5: Eliminar usuario con validación

```python
def eliminar_usuario(usuarios, indice):
    if 0 <= indice < len(usuarios):
        return usuarios.pop(indice)
    return None

usuarios = [{"nombre": "A"}, {"nombre": "B"}]
print(eliminar_usuario(usuarios, 0))
print(usuarios)
```

## Resuelto 6: Menú CRUD modular

```python
usuarios = []

def crear():
    nombre = input("Nombre: ")
    correo = input("Correo: ")
    usuarios.append({"nombre": nombre, "correo": correo})


def listar():
    if not usuarios:
        print("Sin registros")
        return
    for i, u in enumerate(usuarios, start=1):
        print(i, u["nombre"], u["correo"])


def ejecutar_menu():
    while True:
        print("\n1.Crear 2.Listar 3.Salir")
        op = input("Opción: ")
        if op == "1":
            crear()
        elif op == "2":
            listar()
        elif op == "3":
            break
        else:
            print("Opción inválida")


ejecutar_menu()
```

## Resuelto 7: Estadísticas simples de lista

```python
def estadisticas(numeros):
    if not numeros:
        return {"min": None, "max": None, "promedio": 0}
    return {
        "min": min(numeros),
        "max": max(numeros),
        "promedio": sum(numeros) / len(numeros)
    }

print(estadisticas([10, 20, 30, 40]))
```
