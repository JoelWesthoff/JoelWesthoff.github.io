# Sintaxis Básica de Python

## Indentación

En Python, la indentación no es solo para legibilidad; es obligatoria y define el bloque de código. Por convención, se usan 4 espacios por nivel de indentación.

```python
def mi_funcion():
    for i in range(5):
        print(i)  # Esta línea está indentada para que pertenezca al bucle for
```

## Comentarios

Python usa `#` para comentarios de una sola línea. Los comentarios de varias líneas no tienen una sintaxis específica, pero puedes usar `"""` para crear comentarios de bloque (aunque técnicamente son strings multilínea, no comentarios puros).

```python
# Esto es un comentario de una línea

"""
Este es un comentario de bloque.
Usualmente usado para documentar funciones y clases.
"""
```


## Variables y Asignación

No necesitas declarar el tipo de dato de una variable. Python es dinámico y fuerte, por lo que `x = 5` es una declaración válida sin necesidad de `int` u otro tipo de datos. Las convenciones de nombre en PEP 8 sugieren nombres en `snake_case` para variables y funciones, y `CamelCase` para clases.

```python
nombre_variable = "Hola"
nombre_clase = MiClase
```


## Estructuras Básicas de Control

Al igual que otros lenguajes, Python tiene `if`, `for`, y `while`, pero sin paréntesis ni llaves.

```python
if condicion:
    # Código aquí
elif otra_condicion:
    # Otro bloque de código
else:
    # Otro bloque
```


## PEP 8 - Estándares de Estilo de Código en Python

### 1. Nombres de Variables y Funciones

- Usa `snake_case` para variables y funciones (`nombre_variable`, `nombre_funcion`).
- Para constantes, usa `MAYÚSCULAS_CON_GUIONES_BAJOS`.
- Las clases deben seguir el formato `CamelCase` (`NombreClase`).

### 2. Espacios en Blanco

- Añade un espacio después de `,`, `:`, y `;`, pero no antes.
- Usa una línea en blanco para separar funciones y dos líneas en blanco para separar clases en módulos.

### 3. Longitud de Línea

Intenta limitar la longitud de línea a 79 caracteres. Para seguir esta regla, puedes dividir líneas largas usando `\` o paréntesis.

### 4. Comentarios y Docstrings

- Los comentarios deben ser concisos y claros.
- Usa docstrings (`"""Comentario"""`) para documentar clases, métodos y funciones.
- Los comentarios inline, si son necesarios, deben estar después de al menos dos espacios.

```python
def suma(a, b):
    """Devuelve la suma de dos números."""
    return a + b
```

### 5. Comparaciones

- Usa `is` para comparar con `None`: `if variable is None:`.
- Usa `==` para comparar valores.


## Ejercicio Breve

Para familiarizarnos con PEP 8, intenta escribir el siguiente código siguiendo estas recomendaciones de estilo:

```python
def saluda(nombre, edad):
    print(f"Hola, {nombre}, tienes {edad} años.")
```