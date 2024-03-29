# Librería Python / Secuenciador alfanumérico

## Proyecto
[GitHub](https://github.com/Xaival/Libreria-Python-Secuencia-alfanumerica)

[PyPI](https://pypi.org/project/SecuenciaAlfanumerica/)

## Ejemplos
```python
NumDiccionario(["A", "B", "C"], [0, 4], 5)
# ['AAAAA', 'AAAAB', 'AAAAC', 'AAABA', 'AAABB']
```
```python
DiccionarioNum(["A", "B", "C"], ['AAAAA', 'AAAAC', 'AACAB'])
# [0, 2, 19]
```
```python
DiccionarioPredeter("01")
# ["0", "1"]
```

<br>

## Importar librería
`pip install SecuenciaAlfanumerica`

```python
# Importar todas las funciones
import SecuenciaAlfanumerica
```

<br>

## Devolver diccionario predeterminado
```python
from SecuenciaAlfanumerica import DiccionarioPredeter

# Llamar librería predeterminada
print(DiccionarioPredeter("AZ"))
# ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
```

<br>

## Convertir secuencia numérica a una alfabética
```python
from SecuenciaAlfanumerica import NumDiccionario

# Convertir numérico en lista caracteres
Diccionario = ["A", "B", "C"] # Array
Devolver = [0, 4] # Devolver del 1 al 5
Grupo = 5 # Devolver con 5 caracteres
print(NumDiccionario(Diccionario, Devolver, Grupo))
# ['AAAAA', 'AAAAB', 'AAAAC', 'AAABA', 'AAABB']
```

<br>

## Convertir secuencia alfabética a una numérica
```python
from SecuenciaAlfanumerica import DiccionarioNum

# Convertir lista a numérico
Diccionario = ["A", "B", "C"] # Diccionario de elementos
Resolver = ['AAAAA', 'AAAAC', 'AACAB'] # Elementos para resolver
print(DiccionarioNum(Diccionario, Resolver))
# [0, 2, 19]
```

<br>

## Partes
### Diccionario
Puedes llamar a un Diccionario predefinido o declararlo tú.

**Declarar diccionario no definido:** En vez de poner el identificador habria que inglesar un array ["a", "b", "c"]

**Diccionarios predefinidos**:
```
"01" - ["0", "1"]
"09" - ["0", "1", "2", "3", "4", "5", "6", "7", "8", "9"]
"AZ" - ["A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z"]
"AñZ" - ["A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "Ñ", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z"]
"az" - ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"]
"añz" - ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "ñ", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"]
"AZaz" - Diccionario = ["A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z", "a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"]
"AñZañz" - ["A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "Ñ", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z", "a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "ñ", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"]
"azAZ" - ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", "A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z"]
"añzAñZ" - ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "ñ", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", "A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "Ñ", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z"]
"0Z" - ["0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z"]
"0ñZ" - ["0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "Ñ", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z"]
"0z" - ["0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"]
"0ñz" - ["0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "ñ", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"]
"A0" - ["A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z", "0", "1", "2", "3", "4", "5", "6", "7", "8", "9"]
"Añ0" - ["A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "Ñ", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z", "0", "1", "2", "3", "4", "5", "6", "7", "8", "9"]
"a0" - ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", "0", "1", "2", "3", "4", "5", "6", "7", "8", "9"]
"añ0" - ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "ñ", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", "0", "1", "2", "3", "4", "5", "6", "7", "8", "9"]
```

<br>

### Devolver
Es el conjunto de valores el cual se va a convertir.

`[0, 4]` - Devolver del 1 al 5

`[4]` - Devolver 4

<br>

### Grupo
Cantidad mínima de caracteres del grupo. Si no se define se devolverá la máxima a la que llegue.

`5` - AAABA

`1` - BA

`Sin definir` - BA

<br>

### Resolver
Valores de los cuales se quiere saber la posición.

`['AAAAA', 'AAAAC', 'AACAB']` - `[1, 3, 19]`
