# Rebase Interactivo en Git

El **rebase interactivo** es una herramienta poderosa para reescribir el historial de commits en Git. Permite modificar, combinar, eliminar o reorganizar commits antes de integrarlos en otra rama.

## ¿Cuándo usar rebase interactivo?

- Limpiar el historial antes de hacer un merge.
- Editar mensajes de commits.
- Combinar varios commits en uno solo (squash).
- Eliminar commits innecesarios.
- Reordenar commits.

## ¿Cómo iniciar un rebase interactivo?

```bash
git rebase -i HEAD~N
```

Donde `N` es el número de commits hacia atrás que quieres editar.

## Acciones comunes en el editor

Al ejecutar el comando, se abre un editor con una lista de commits y acciones posibles:

- `pick`: Mantener el commit tal cual.
- `reword`: Cambiar el mensaje del commit.
- `edit`: Modificar el contenido del commit.
- `squash`: Combinar el commit con el anterior.
- `fixup`: Igual que squash, pero descarta el mensaje del commit.
- `drop`: Eliminar el commit.

Ejemplo:

```
pick 123abc Primer commit
reword 456def Segundo commit
squash 789ghi Tercer commit
```

## Ejemplo paso a paso

1. Inicia el rebase interactivo:
   ```bash
   git rebase -i HEAD~3
   ```
2. Elige las acciones en el editor.
3. Guarda y cierra el editor.
4. Si elegiste `edit`, realiza los cambios y usa:
   ```bash
   git commit --amend
   git rebase --continue
   ```
5. Si hay conflictos, resuélvelos y continúa:
   ```bash
   git add .
   git rebase --continue
   ```

## Precauciones

- **No uses rebase interactivo en ramas compartidas**: Puede causar problemas a otros colaboradores.
- Haz backup antes de reescribir historial importante.

## Recursos útiles

- [Documentación oficial de Git](https://git-scm.com/book/es/v2/Git-Tools-Reescribiendo-Historia)
- `git help rebase`
