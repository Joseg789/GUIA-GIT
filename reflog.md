# Todo lo que debes saber sobre `git reflog`

## ¿Qué es `git reflog`?

`git reflog` es un comando que muestra el historial de referencias (logs) de los movimientos de HEAD y otras referencias en tu repositorio local. Permite ver cambios recientes, incluso aquellos que no aparecen en el historial normal (`git log`), como commits borrados, reseteos, merges, etc.

## ¿Para qué sirve?

- Recuperar commits perdidos tras un reset, rebase, o merge.
- Ver el historial de cambios de ramas y HEAD.
- Auditar acciones recientes en el repositorio.

## Comandos básicos

```bash
git reflog
```

Muestra el historial de movimientos de HEAD.

```bash
git reflog <branch>
```

Muestra el historial de una rama específica.

## Ejemplo de salida

```
e3a1b2c HEAD@{0}: commit: Añadido archivo README
a7c9d8e HEAD@{1}: reset: moving to HEAD~1
f4b3a2d HEAD@{2}: commit: Corrección de bug
```

## Recuperar un commit perdido

Si hiciste un `git reset --hard` y perdiste un commit, puedes recuperarlo:

1. Busca el commit en `git reflog`.
2. Haz checkout al commit perdido:
   ```bash
   git checkout <hash>
   ```
3. Opcional: crea una rama desde ese commit:
   ```bash
   git branch recuperar <hash>
   ```

## Limpiar el reflog

El reflog se limpia automáticamente después de 90 días, pero puedes hacerlo manualmente:

```bash
git reflog expire --expire=30.days refs/heads/main
git gc --prune=now
```

## Consideraciones

- El reflog es local, no se comparte entre repositorios.
- Es útil para recuperación y auditoría, pero no reemplaza el historial de commits.

## Recursos

- [Documentación oficial de git-reflog](https://git-scm.com/docs/git-reflog)
- [Guía práctica de Git](https://git-scm.com/book/es/v2)
