# 02 · Navegación básica y saltos

Toda la navegación en `vi` se hace en **modo comando**. Si estás en modo inserción, estas teclas escriben letras en lugar de mover el cursor — el primer síntoma de que "algo salió mal" suele ser justo este.

## Movimiento carácter por carácter

| Tecla | Función |
|---|---|
| `h` | Cursor un carácter a la izquierda |
| `l` | Cursor un carácter a la derecha |
| `j` | Cursor una línea abajo |
| `k` | Cursor una línea arriba |

Se pueden pensar como un diamante: `h` y `l` a los lados, `j` y `k` arriba/abajo (curiosamente `j` parece una flecha hacia abajo si la miras con atención).

## Movimiento por palabras

| Tecla | Función |
|---|---|
| `w` | Salta al inicio de la siguiente palabra |
| `e` | Salta al final de la palabra actual |
| `b` | Salta al inicio de la palabra anterior |

**Mi ejemplo:** para llegar rápido a una palabra específica en una línea larga, prefiero `w` repetido en vez de moverme letra por letra con `l`.

## Moverse dentro de la línea

| Tecla | Función |
|---|---|
| `0` | Inicio de la línea actual |
| `$` | Final de la línea actual |

## Saltos entre líneas

| Comando | Función |
|---|---|
| `1G` | Salta a la primera línea |
| `nG` | Salta a la línea número `n` |
| `G` (con `Shift`) | Salta a la última línea |

**Mi ejemplo:** `3G` me lleva directo a la línea 3 sin tener que contar cuántas veces presionar `j`.

## Combinando número + movimiento

Casi cualquier comando de movimiento acepta un número delante para repetirlo. Por ejemplo, `8l` mueve el cursor 8 caracteres a la derecha, y `3j` baja 3 líneas. Esto se vuelve muy útil cuando ya conoces el archivo y quieres llegar rápido a un punto exacto.

## Qué hacer si te pierdes

Si presionas una tecla que no reconoces y terminas en modo inserción sin querer:

1. Presiona `Esc` para volver a modo comando.
2. Si además modificaste algo sin querer, `:q!` sale sin guardar.
3. Vuelve a abrir el archivo con `vi mi_archivo.txt` y sigue desde ahí.
