# 07 · Guardar y salir

Todos estos comandos se ejecutan desde **modo comando** (si estás insertando texto, primero `Esc`).

| Comando | Qué hace |
|---|---|
| `:wq` | Guarda (write) y cierra (quit) |
| `:x` | Guarda y cierra (solo escribe si hubo cambios) |
| `ZZ` | Guarda y cierra — sin usar `:`, es un atajo directo |
| `:w` | Guarda sin cerrar, para seguir editando |
| `:w!` | Fuerza guardar aunque el archivo sea de solo lectura, si es posible |
| `:q` | Cierra sin guardar (solo funciona si no hay cambios pendientes) |
| `:q!` | Cierra **descartando** cualquier cambio, aunque los haya |
| `:wq!` | Guarda forzado (sobre archivo de solo lectura) y cierra |
| `:e!` | Descarta los cambios y recarga el archivo desde el disco, sin salir |

## Cuál uso yo en cada caso

- **Terminé de editar y quiero guardar todo:** `:wq` (la más usada, sin duda).
- **Metí la pata, escribí cosas que no debía, y quiero volver a como estaba:** `:q!`.
- **Quiero guardar un avance sin cerrar el editor:** `:w`.
- **Quiero "empezar de nuevo" sin salir del editor:** `:e!`.

## Por qué existe `ZZ` si ya existe `:wq`

Ambos hacen lo mismo, pero `ZZ` no necesita `:` ni `Enter` extra — son solo dos teclas mayúsculas seguidas. Es un atajo, no un comando distinto. Con la práctica terminé usando `ZZ` más que `:wq` porque es más rápido de teclear.

## El error que más cometí al principio

Presionar `:q` cuando había cambios sin guardar y que `vi` se negara a cerrar. Eso no es un error del editor: es una protección para que no pierdas trabajo por accidente. La solución es decidir a conciencia entre `:wq` (si quiero guardar) o `:q!` (si quiero descartar).
