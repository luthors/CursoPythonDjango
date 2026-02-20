# 🧪 Clase 02 · Ejemplos Paso a Paso

[⬅️ Volver a la clase](Clase_02_Estructuras_y_Funciones.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## 1) Lista: agregar y mostrar elementos

```python
nombres = []
nombres.append("Ana")
nombres.append("Luis")

for nombre in nombres:
    print(nombre)
```

---

## 2) Diccionario: registrar usuario

```python
usuario = {
    "nombre": "Carlos",
    "correo": "carlos@mail.com",
    "activo": True
}

print(usuario["nombre"], usuario["correo"])
```

---

## 3) Función con parámetros y retorno

```python
def calcular_iva(precio, porcentaje=19):
    return precio * (porcentaje / 100)

iva = calcular_iva(100000)
print("IVA:", iva)
```

---

## 4) CRUD básico con funciones

```python
usuarios = []

def crear_usuario(nombre, correo):
    usuarios.append({"nombre": nombre, "correo": correo})

def listar_usuarios():
    if len(usuarios) == 0:
        print("No hay usuarios")
        return
    for i, u in enumerate(usuarios, start=1):
        print(i, u["nombre"], u["correo"])

def actualizar_usuario(indice, nombre, correo):
    if 0 <= indice < len(usuarios):
        usuarios[indice]["nombre"] = nombre
        usuarios[indice]["correo"] = correo
        print("Usuario actualizado ✅")
    else:
        print("Índice inválido ❌")

def eliminar_usuario(indice):
    if 0 <= indice < len(usuarios):
        eliminado = usuarios.pop(indice)
        print("Eliminado:", eliminado["nombre"])
    else:
        print("Índice inválido ❌")
```

---

## 5) Menú con `while`

```python
while True:
    print("\n1. Crear  2. Listar  3. Salir")
    opcion = input("Elige: ")

    if opcion == "1":
        nombre = input("Nombre: ")
        correo = input("Correo: ")
        crear_usuario(nombre, correo)
    elif opcion == "2":
        listar_usuarios()
    elif opcion == "3":
        print("Hasta luego")
        break
    else:
        print("Opción inválida")
```

---

## 6) Evitar errores de índice

```python
texto = input("Índice a eliminar: ")

if texto.isdigit():
    indice = int(texto) - 1
    eliminar_usuario(indice)
else:
    print("Debes ingresar un número válido")
```
