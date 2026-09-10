# 📝 Manual vi editor — Guía de bolsillo hecha aprendiendo

![vi](https://img.shields.io/badge/editor-vi-brightgreen)
![Linux](https://img.shields.io/badge/OS-Linux-blue)
![Estado](https://img.shields.io/badge/estado-en%20progreso-yellow)

Mi propio manual del editor `vi`, documentado a medida que lo iba aprendiendo en el curso de Seminario - Linux. Pensado para que cualquiera pueda clonarlo y practicar los mismos comandos que yo practiqué.

## 📚 Tabla de contenido

1. [Modos y creación de archivos](docs/01-modos-y-creacion.md)
2. [Navegación básica y saltos](docs/02-navegacion.md)
3. [Edición y deshacer](docs/03-edicion-y-deshacer.md)
4. [Copiar y pegar](docs/04-copiar-y-pegar.md)
5. [Buscar y reemplazar](docs/05-buscar-y-reemplazar.md)
6. [Formas de insertar texto](docs/06-insertar-texto.md)
7. [Guardar y salir](docs/07-guardar-y-salir.md)

## ❓ ¿Qué es vi?

`vi` es un editor de texto en modo terminal que viene instalado por defecto en prácticamente cualquier sistema Unix o Linux. A diferencia de un editor gráfico como Bloc de notas o gedit, no hay clics ni menús: todo se hace con el teclado, moviéndote entre un **modo comando** (para navegar, borrar, guardar) y un **modo inserción** (para escribir texto normal).

Al principio se siente incómodo, porque el editor no reacciona como uno esperaría — escribir sin estar en modo inserción puede borrar o mover cosas en lugar de agregar texto. Pero una vez que se automatiza el cambio entre modos, resulta muy rápido para editar archivos sin soltar el teclado ni depender de un mouse, algo clave cuando se trabaja por SSH en un servidor remoto sin entorno gráfico.

Lo aprendí siguiendo la Guía de laboratorio #6 del curso, y este repositorio es mi forma de convertir esas notas de práctica en una referencia reutilizable, con mis propios ejemplos.

## 🧾 Cheat sheet — comandos que más uso

| Comando | Qué hace | Mi ejemplo |
|---|---|---|
| `i` / `a` | Entra a modo inserción (antes / después del cursor) | `i` para corregir el inicio de una línea |
| `Esc` | Sale de modo inserción, vuelve a modo comando | Lo uso ante cualquier duda de en qué modo estoy |
| `dw` | Borra una palabra | `dw` sobre "very" la elimina |
| `dd` | Borra la línea completa | `3dd` borra 3 líneas seguidas |
| `u` | Deshace la última operación | `4u` deshace las últimas 4 |
| `yy` / `p` | Copia una línea / la pega | `yy` + `p` duplica la línea actual |
| `/patron` | Busca dentro del archivo | `/editor` salta a la palabra "editor" |
| `:%s/a/b/g` | Reemplaza "a" por "b" en todo el archivo | `:%s/vi/Vim/g` |
| `:wq` | Guarda y sale | Lo uso al terminar de editar |

## 🚀 Cómo practicar tú mismo

```bash
git clone https://github.com/TU-USUARIO/NOMBRE-DEL-REPO.git
cd NOMBRE-DEL-REPO
vi ejercicios/mi-archivo-practica.txt
```

Con el archivo abierto, sigue los ejemplos de cada sección en `docs/` en orden: primero practica moverte (02), luego borrar y deshacer (03), después copiar/pegar (04) y buscar/reemplazar (05). El archivo de ejercicios está pensado justo para eso, sin miedo a "romper" nada importante.

## 🙌 Créditos

- Basado en la **Guía de laboratorio #6 — El editor vi**, material de apoyo del curso.
- Actividad y rúbrica: **Laboratorio 7 — Documenta, versiona y publica lo que aprendes**.
- Docente: **Bayron Jesit Ospina Cifuentes** — bayron.ospinaci@amigo.edu.co
- Curso: Seminario - Linux, FUNLAM.
