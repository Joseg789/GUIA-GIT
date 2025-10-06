# Todo lo que debes saber sobre `git add`

`git add` es un comando fundamental en Git que se utiliza para agregar cambios en los archivos al área de preparación (staging area). Esto es un paso previo antes de confirmar (commit) los cambios en el repositorio.

## ¿Para qué sirve `git add`?

- Prepara los archivos modificados, nuevos o eliminados para ser incluidos en el próximo commit.
- Permite seleccionar exactamente qué cambios quieres confirmar.

## Uso básico

```bash
git add <archivo>
```

Agrega un archivo específico al área de preparación.

```bash
git add .
```

Agrega todos los archivos modificados en el directorio actual y subdirectorios.

```bash
git add -A
```

Agrega todos los cambios (nuevos, modificados y eliminados) en el repositorio.

## Ejemplo de flujo de trabajo

1. Modificas o creas archivos en tu proyecto.
2. Ejecutas `git add archivo.txt` para preparar ese archivo.
3. Usas `git commit -m "Mensaje"` para guardar los cambios en el historial.

## Comandos útiles relacionados

- `git status`: Muestra el estado de los archivos y qué está en el área de preparación.
- `git reset <archivo>`: Quita un archivo del área de preparación.

## Resumen

`git add` te da control sobre qué cambios se incluirán en el próximo commit, permitiendo un flujo de trabajo organizado y preciso en tus proyectos con Git.

## añadir carpetas

git add <name_carpeta>

## añade todos los archivos de una carpeta con una extension especifica

`git add <name_carpeta>/*js`
