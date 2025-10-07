# Rebase en Git

## ¿Qué es `git rebase`?

`git rebase` es una herramienta para integrar cambios de una rama en otra, reescribiendo el historial de commits. Permite mantener un historial lineal y limpio.

## ¿Cuándo usar rebase?

- Para actualizar una rama feature con los últimos cambios de la rama principal (`main` o `master`).
- Para evitar merges innecesarios y conflictos complejos.
- Antes de fusionar una rama feature, para que el historial sea más claro.

## Tipos de rebase

### 1. Rebase simple

```bash
git checkout feature
git rebase main
```

Esto mueve los commits de `feature` encima de los últimos commits de `main`.

### 2. Rebase interactivo

Permite editar, reordenar, combinar o eliminar commits.

```bash
git rebase -i HEAD~n
```

Donde `n` es el número de commits a revisar.

## Resolución de conflictos

Si hay conflictos durante el rebase:

1. Git pausará el proceso y mostrará los archivos en conflicto.
2. Resuelve los conflictos manualmente.
3. Usa:
   ```bash
   git add <archivo_resuelto>
   git rebase --continue
   ```
4. Si necesitas abortar:
   ```bash
   git rebase --abort
   ```

## Precauciones

- **No hagas rebase en ramas compartidas**: Reescribe el historial y puede causar problemas a otros colaboradores.
- **Usa rebase solo en tu trabajo local** antes de hacer push.

## Diferencias entre merge y rebase

| Merge                       | Rebase                   |
| --------------------------- | ------------------------ |
| Crea un commit de merge     | Reescribe el historial   |
| Historial ramificado        | Historial lineal         |
| No modifica commits previos | Modifica commits previos |

## Comandos útiles

- Iniciar rebase:
  ```bash
  git rebase <rama_base>
  ```
- Rebase interactivo:
  ```bash
  git rebase -i <commit>
  ```
- Continuar rebase:
  ```bash
  git rebase --continue
  ```
- Abortar rebase:
  ```bash
  git rebase --abort
  ```

## Recursos

- [Documentación oficial de Git](https://git-scm.com/docs/git-rebase)
- [Atlassian Git Tutorials](https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase)
