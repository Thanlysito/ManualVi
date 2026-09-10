# 06 · Formas de insertar texto

Ya vimos en [01-modos-y-creacion.md](01-modos-y-creacion.md) que hay que entrar a modo inserción para escribir. Pero `vi` tiene varias formas de entrar a ese modo, y cada una te deja el cursor en un lugar distinto — elegir la correcta ahorra movimientos.

## Las cuatro puertas de entrada a modo inserción

| Comando | Dónde empieza a insertar |
|---|---|
| `i` | Justo **antes** del cursor |
| `a` | Justo **después** del cursor (append) |
| `o` | En una **línea nueva debajo** de la actual |
| `O` | En una **línea nueva arriba** de la actual |

## Cuándo uso cada una

- **`i`**: cuando quiero corregir o agregar algo exactamente donde está el cursor, por ejemplo insertar una palabra olvidada al inicio de una línea.
- **`a`**: cuando quiero seguir escribiendo justo después de donde estoy parado, por ejemplo continuar una palabra o frase.
- **`o`**: cuando necesito una línea nueva completa debajo, sin tener que ir manualmente al final de la línea actual primero.
- **`O`**: lo mismo pero arriba, útil para agregar un título o encabezado antes de un párrafo ya escrito.

**Mi ejemplo:** partiendo de:

```
Welcome to the vi editor.
It is a very powerful text editor.
Especially for those who master it.
```

Si pongo el cursor en la primera línea y presiono `o`, se abre una línea vacía debajo de "Welcome..." lista para escribir, sin mover ni una palabra del resto del texto.

## Diferencia entre `o` e `i`, `a`

La diferencia clave: `i` y `a` insertan **dentro de la misma línea** donde está el cursor. `o` y `O` crean **una línea completamente nueva**. Confundir esto es una de las dudas más comunes al empezar (y una de las que yo documenté en Issues).

## Salir de modo inserción

Sin importar cómo entraste, siempre se sale igual: `Esc`.
