# Tipos de datos avanzados

Python tiene varios tipos de datos que no son tan comunes en otros lenguajes, y entender cómo usarlos de forma correcta es esencial para escribir código eficiente.

## 1. Listas (list):

Las listas son colecciones ordenadas, lo que significa que los elementos tienen un orden específico. Son mutables, lo que significa que puedes modificar su contenido después de haberlas creado.

### Características de las listas:

- Son ordenadas: Los elementos tienen un índice asociado.
- Son mutables: Puedes modificar, agregar o eliminar elementos.
- Permiten duplicados: Puedes tener el mismo valor más de una vez en la lista.

### Operaciones comunes con listas:

```python
# Crear una lista
frutas = ["manzana", "plátano", "cereza"]
print(frutas)

# Acceder a un elemento (por índice)
print(frutas[0])  # 'manzana'

# Modificar un elemento
frutas[1] = "pera"
print(frutas)

# Agregar un elemento al final
frutas.append("kiwi")
print(frutas)

# Eliminar un elemento
frutas.remove("pera")  # Elimina la primera ocurrencia de 'pera'
print(frutas)

# Obtener el tamaño de la lista
print(len(frutas))  # 3

# Crear una lista con elementos repetidos
repetidos = [1, 1, 2, 2, 3]
print(repetidos)

```

### Usos recomendados:

- Cuando necesites mantener un orden específico de elementos.
- Cuando quieras tener elementos modificables o agregar/quitar elementos durante la ejecución.

## 2. Tuplas (tuple):

Las tuplas son colecciones ordenadas, pero a diferencia de las listas, son inmutables. Esto significa que una vez que las creas, no puedes cambiar, agregar o eliminar elementos.

### Características de las tuplas:

- Son ordenadas: Los elementos tienen un índice asociado.
- Son inmutables: No puedes cambiar su contenido después de crearlas.
- Permiten duplicados: Puedes tener el mismo valor más de una vez en la tupla.

### Operaciones comunes con tuplas:

```python
# Crear una tupla
colores = ("rojo", "verde", "azul")
print(colores)

# Acceder a un elemento
print(colores[1])  # 'verde'

# Las tuplas son inmutables, no puedes hacer esto:
# colores[1] = "amarillo"  # Esto causaría un error

# Las tuplas pueden contener elementos duplicados
numeros = (1, 1, 2, 3)
print(numeros)

```

### Usos recomendados:

- Cuando necesitas un conjunto de datos que no debe cambiar (inmutable).
- Cuando necesitas usar un valor como clave en un diccionario (debido a que las tuplas son inmutables y, por lo tanto, son hashable, a diferencia de las listas).
- Cuando el orden importa, pero no necesitas modificar la colección.

## 3. Diccionarios (dict):

Los diccionarios son colecciones de pares clave-valor. Son mutables, y puedes agregar, modificar o eliminar elementos fácilmente. A diferencia de las listas y tuplas, no son ordenados en versiones anteriores a Python 3.7, pero a partir de Python 3.7+, los diccionarios mantienen el orden de inserción.

### Características de los diccionarios:

- No son ordenados (en versiones anteriores a Python 3.7), pero mantienen el orden a partir de Python 3.7+.
- Son mutables: Puedes cambiar el valor asociado a una clave, agregar o eliminar claves.
- Las claves deben ser inmutables (por ejemplo, pueden ser cadenas, tuplas, pero no listas).
- No permiten duplicados en las claves: Cada clave debe ser única.

### Operaciones comunes con diccionarios:

```python
# Crear un diccionario
persona = {"nombre": "Juan", "edad": 30, "profesión": "ingeniero"}
print(persona)

# Acceder a un valor por su clave
print(persona["nombre"])  # 'Juan'

# Modificar un valor
persona["edad"] = 31
print(persona)

# Agregar una nueva clave-valor
persona["ciudad"] = "Madrid"
print(persona)

# Eliminar una clave
del persona["profesión"]
print(persona)

# Verificar si una clave existe
print("nombre" in persona)  # True

```

### Usos recomendados:

- Cuando necesitas asociar claves únicas a valores.
- Para representar información estructurada de manera flexible (por ejemplo, datos de una persona como nombre, edad, etc.).
- Cuando necesitas realizar búsquedas rápidas por clave.

## 4. Sets (set):

Un set es una colección desordenada de elementos únicos, es decir, no permite duplicados. Al igual que las listas y diccionarios, son mutables. Los sets son útiles cuando necesitas realizar operaciones de conjunto, como intersección, unión y diferencia.

### Características de los sets:

- Son desordenados: No se garantiza el orden de los elementos.
- Son mutables: Puedes agregar y eliminar elementos.
- No permiten duplicados: Si intentas agregar un elemento que ya está presente, no se agregará.

### Operaciones comunes con sets:

```python
# Crear un set
numeros = {1, 2, 3, 4, 5}
print(numeros)

# Agregar un elemento
numeros.add(6)
print(numeros)

# Intentar agregar un duplicado
numeros.add(3)  # No hace nada porque 3 ya está en el set
print(numeros)

# Eliminar un elemento
numeros.remove(4)  # Esto eliminará el 4
print(numeros)

# Realizar operaciones de conjunto
otro_set = {3, 4, 5, 6}
union = numeros | otro_set  # Unión
interseccion = numeros & otro_set  # Intersección
diferencia = numeros - otro_set  # Diferencia
print(union, interseccion, diferencia)

```

### Usos recomendados:

- Cuando no necesitas duplicados.
- Para realizar operaciones matemáticas de conjunto, como la unión, intersección y diferencia.
- Cuando quieres verificar la existencia de un elemento de manera rápida.

## Diferencias clave entre listas, tuplas, diccionarios y sets:

| Tipo de Dato | Ordenado | Mutable | Permite Duplicados | Ejemplo de Uso                                                                       |
| ------------ | -------- | ------- | ------------------ | ------------------------------------------------------------------------------------ |
| Lista        | Sí       | Sí      | Sí                 | Cuando necesitas un conjunto ordenado y modificable de elementos.                    |
| Tupla        | Sí       | No      | Sí                 | Cuando necesitas un conjunto inmutable de datos (ideal para claves en diccionarios). |
| Diccionario  | No       | Sí      | No (en las claves) | Para asociar claves únicas a valores.                                                |
| Set          | No       | Sí      | No                 | Cuando no necesitas duplicados y realizas operaciones de conjunto.                   |

### Conclusión:

Es importante elegir el tipo de dato adecuado en función de tus necesidades. Si necesitas mantener un orden específico, usa una lista o tupla. Si necesitas almacenar datos en pares clave-valor, utiliza un diccionario. Y si solo te interesan los elementos únicos sin preocuparte del orden, elige un set.
