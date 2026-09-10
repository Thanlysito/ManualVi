# 01 · Modos y creación de archivos

## ¿Cómo funciona vi por dentro?

Lo primero que me costó entender de `vi` es que no es un editor "de un solo modo" como el Bloc de notas. Todo el tiempo estás en uno de dos estados, y si no sabes en cuál estás, terminas escribiendo comandos como si fueran texto (o peor, texto como si fueran comandos).

- **Modo comando**: es el modo por defecto al abrir el editor. Aquí las teclas no escriben letras, sino que ejecutan acciones: moverte, borrar, guardar, buscar, etc.
- **Modo inserción**: aquí sí escribes texto normal, como en cualquier editor. Se entra presionando `i` (u otras teclas parecidas) y se sale con `Esc`.

La regla mental que uso: **`Esc` siempre me devuelve a modo comando**, sin importar en qué lío me haya metido.

## Crear un archivo nuevo

Para abrir (o crear, si no existe) un archivo:

```bash
vi mi_archivo.txt
```

Si el archivo no existía, `vi` lo crea vacío y te deja en modo comando. Para empezar a escribir, hay que entrar a modo inserción primero.

## Entrar a modo inserción

| Comando | Qué hace |
|---|---|
| `i` | Inserta texto **antes** del cursor |
| `a` | Inserta texto **después** del cursor |
| `o` | Abre una línea nueva **debajo** y entra a inserción |
| `O` | Abre una línea nueva **arriba** y entra a inserción |

**Mi ejemplo:** al crear un archivo desde cero uso `i` apenas abro el editor, escribo todo el texto y luego `Esc` para salir del modo inserción.

## Guardar y salir (lo mínimo para no perder nada)

```
:wq
```

Guarda los cambios y cierra `vi`. Más detalles de esto en [07-guardar-y-salir.md](07-guardar-y-salir.md).

## La parte inferior de la pantalla no miente

Cuando abres un archivo, en la esquina inferior izquierda `vi` te muestra el nombre del archivo, el número de líneas y de caracteres, algo como:

```
"mi_archivo.txt" 3 lines, 97 characters
```

Es útil para confirmar que el archivo se guardó bien o que tiene el contenido que esperabas.

## Errores comunes (los que yo cometí)

- Empezar a escribir sin haber entrado a modo inserción → los caracteres se interpretan como comandos y el archivo queda hecho un desastre.
- Quedar atrapado en modo inserción sin saberlo → si presionas `Esc` varias veces no pasa nada malo, así que ante la duda, `Esc`.
