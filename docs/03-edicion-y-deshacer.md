# 03 · Edición y deshacer

## Borrar texto

| Comando | Qué hace |
|---|---|
| `x` | Borra un carácter bajo el cursor |
| `dw` | Borra (delete word) desde el cursor hasta el final de la palabra |
| `2dw` | Borra dos palabras seguidas |
| `dd` | Borra la línea completa |

**Mi ejemplo:** si tengo la línea `It is a very powerful text editor.` y quiero quitar la palabra "very", pongo el cursor sobre la `v` y ejecuto `dw`. El resultado queda: `It is a powerful text editor.`

## El patrón número + comando

Igual que con la navegación, casi todos los comandos de edición aceptan un número delante para repetirlos:

- `4x` borra 4 caracteres seguidos.
- `3dd` borra 3 líneas completas.

Es más rápido que repetir el mismo comando varias veces a mano.

## Deshacer y rehacer

| Comando | Qué hace |
|---|---|
| `u` | Deshace la última operación |
| `4u` | Deshace las últimas 4 operaciones |
| `Ctrl+r` | Rehace lo que se deshizo (no todas las versiones de `vi` lo soportan igual) |

**Mi ejemplo:** después de borrar 4 caracteres con `xxxx`, si me arrepiento, `4u` los recupera todos de una vez, sin tener que presionar `u` cuatro veces.

## Por qué probar y deshacer es la mejor forma de aprender

Una de las cosas que más me sirvió fue perder el miedo a "romper" el archivo: como `u` casi siempre puede deshacer lo último que hice, pude probar comandos de borrado sin preocuparme de perder contenido real. Recomiendo practicar sobre un archivo de prueba (como el de la carpeta [`ejercicios/`](../ejercicios/mi-archivo-practica.txt)) antes de usarlos en algo importante.

## Diferencia entre `x`, `dw` y `dd`

Esta fue una de mis dudas reales, documentada en los Issues del repositorio:

- `x` borra de a un **carácter**.
- `dw` borra de a una **palabra** (desde donde está el cursor hasta el final de la palabra).
- `dd` borra la **línea completa**, sin importar dónde esté el cursor dentro de ella.
