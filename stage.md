# El Stage en Git

El **stage** (o área de preparación) es una parte fundamental del flujo de trabajo en Git. Aquí tienes todo lo que debes saber:

## ¿Qué es el stage?

- Es un área intermedia donde se preparan los cambios antes de confirmarlos (commit).
- Permite seleccionar exactamente qué cambios se incluirán en el próximo commit.

## Flujo básico

1. **Trabajas** en tus archivos.
2. **Agregas** los cambios al stage con `git add`.
3. **Confirmas** los cambios en el repositorio con `git commit`.

## Comandos principales

- `git status`: Muestra el estado de los archivos (modificados, en stage, sin seguimiento).
- `git add <archivo>`: Añade un archivo específico al stage.
- `git add .`: Añade todos los archivos modificados al stage.
- `git reset <archivo>`: Quita un archivo del stage (sin perder los cambios locales).
- `git diff`: Muestra las diferencias entre el working directory y el stage.
- `git diff --staged`: Muestra las diferencias entre el stage y el último commit.

## Ventajas del stage

- Permite hacer commits más organizados y específicos.
- Puedes preparar solo una parte de los cambios realizados.
- Facilita la revisión antes de confirmar.

## Ejemplo de uso

```bash
# Ver el estado actual
git status

# Añadir un archivo al stage
git add archivo.txt

# Confirmar los cambios preparados
git commit -m "Mensaje del commit"
```

## Resumen visual

```
Working Directory → Stage (git add) → Repository (git commit)
```

## Buenas prácticas

- Usa el stage para agrupar cambios lógicos.
- Revisa siempre con `git status` antes de hacer commit.
- Aprovecha `git add -p` para añadir partes específicas de un archivo.
