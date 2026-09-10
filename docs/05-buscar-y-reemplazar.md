# 05 · Buscar y reemplazar

## Búsqueda simple

Para buscar una palabra o patrón dentro del archivo, en modo comando se escribe `/` seguido del texto a buscar:

```
/editor
```

Y se presiona `Enter`. El cursor salta a la primera coincidencia.

| Comando | Qué hace |
|---|---|
| `/palabra` | Busca hacia adelante |
| `?palabra` | Busca hacia atrás |
| `n` | Repite la búsqueda en la misma dirección |
| `N` | Repite la búsqueda en dirección contraria |

**Mi ejemplo:** en un archivo largo, en vez de bajar línea por línea con `j`, uso `/vi` para saltar directo a la siguiente vez que aparece la palabra "vi".

## Reemplazo con `:%s`

Este es el comando que más se parece a "buscar y reemplazar" de un editor de texto normal. La sintaxis general es:

```
:%s/patron/reemplazo/g
```

Desglosado:

- `:` entra al modo de comandos de línea (los que empiezan con dos puntos).
- `%` significa "en todo el archivo" (sin el `%`, solo afecta la línea actual).
- `s` es "substitute".
- `patron` es lo que se busca.
- `reemplazo` es por lo que se cambia.
- `g` (global) significa "todas las coincidencias en la línea", no solo la primera.

**Mi ejemplo:** para cambiar todas las apariciones de "vi" por "Vim" en todo el archivo:

```
:%s/vi/Vim/g
```

## Sobre los espacios y los corchetes

Una de mis dudas reales (documentada en Issues): si el patrón o el reemplazo incluyen espacios, **no hace falta escapar nada especial**, el `/` ya delimita claramente dónde empieza y termina cada parte. Donde sí hay que tener cuidado es con caracteres especiales de expresiones regulares (como `.`, `*`, `[`, `]`), que si aparecen literalmente en el texto que buscas, deben escaparse con `\` para que `vi` no los interprete como parte de un patrón.

## Reemplazo solo en una línea o rango

- `:s/patron/reemplazo/` → solo en la línea actual, primera coincidencia.
- `:5,10s/patron/reemplazo/g` → solo entre las líneas 5 y 10, todas las coincidencias.
