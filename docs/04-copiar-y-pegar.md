# 04 · Copiar y pegar (yank / paste)

En `vi`, "copiar" se llama **yank** (de ahí la tecla `y`), y "pegar" es **paste** (la tecla `p`).

## Copiar (yank)

|Comando|Qué hace|
|-|-|
|`yw`|Copia (yank word) desde el cursor hasta el final de la palabra|
|`yy`|Copia la línea completa|
|`3yy`|Copia 3 líneas a partir de la actual|

## Pegar (paste)

|Comando|Qué hace|
|-|-|
|`p`|Pega **después** de la posición del cursor (o debajo, si copiaste una línea)|
|`P`|Pega **antes** de la posición del cursor (o encima, si copiaste una línea)|

## Diferencia entre `p` y `P`

Esta fue una de mis dudas reales (ver Issues): la diferencia no es "qué" se pega, sino **dónde** se pega respecto al cursor.

* Si copié una **palabra** con `yw` y el cursor está sobre otra palabra, `p` la pega justo después del carácter donde está el cursor, y `P` la pega justo antes.
* Si copié una **línea completa** con `yy`, `p` la pega en la línea de abajo y `P` en la línea de arriba.

**Mi ejemplo:** con el cursor en la línea `Especially for those who master it.`, si antes copié esa misma línea con `yy`, al presionar `p` obtengo una copia duplicada justo debajo:

```
Especially for those who master it.
Especially for those who master it.
```

## Combinar con borrar

Algo que uso seguido: `dd` también deja la línea borrada disponible para pegar con `p`, como un "cortar y pegar". Es decir, no siempre necesitas `yy`; si vas a **mover** una línea de lugar, `dd` + `p` es más directo que copiar y luego borrar el original.

## Flujo típico que uso

1. `yy` sobre la línea que quiero duplicar o mover.
2. Navego con `j`/`k`/`nG` hasta la línea de referencia.
3. `p` o `P` según si quiero pegar debajo/después o encima/antes.



\## Mi ejemplo propio



En mi archivo de practica probe copiar la linea 'Welcome to the vi editor.' con yy, luego me movi hasta la ultima linea con G, y pegue la copia ahi con p. El resultado fue que la linea aparecio duplicada al final del archivo, sin afectar las demas lineas.

