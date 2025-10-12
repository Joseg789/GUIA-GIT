# Git Pull con Rebase

## ¿Qué es `git pull --rebase`?

`git pull --rebase` es una variante del comando `git pull` que, en vez de hacer un merge automático de los cambios remotos con los locales, reescribe el historial local aplicando tus commits encima de los últimos cambios del repositorio remoto.

## ¿Por qué usar `git pull --rebase`?

- Mantiene un historial más limpio y lineal.
- Evita commits de merge innecesarios.
- Facilita la revisión y el seguimiento de cambios.

## ¿Cómo funciona?

1. Descarga los cambios remotos.
2. Rebasa tus commits locales encima de los nuevos commits remotos.
3. Si hay conflictos, debes resolverlos y continuar el rebase con `git rebase --continue`.

## Comandos básicos

```bash
git pull --rebase
```

- Rebasa tus cambios locales sobre los remotos.

```bash
git pull --rebase origin main
```

- Rebasa tus cambios locales sobre la rama `main` del remoto `origin`.

## Resolución de conflictos

Si ocurre un conflicto durante el rebase:

1. Resuelve el conflicto en los archivos afectados.
2. Marca los archivos como resueltos:
   ```bash
   git add <archivo>
   ```
3. Continúa el rebase:
   ```bash
   git rebase --continue
   ```
4. Si necesitas abortar el rebase:
   ```bash
   git rebase --abort
   ```

## Consideraciones

- No uses rebase en ramas compartidas si otros colaboradores están trabajando sobre ellas.
- Antes de hacer push después de un rebase, puede ser necesario usar `git push --force-with-lease`.

## Diferencia entre `merge` y `rebase`

| Merge                 | Rebase              |
| --------------------- | ------------------- |
| Crea commits de merge | Historial lineal    |
| Fácil de usar         | Reescribe historial |
| Puede ser confuso     | Más limpio          |

## Ejemplo de flujo de trabajo

```bash
git fetch origin
git pull --rebase origin main
# Resuelve conflictos si aparecen
git push
```

## Recursos adicionales

- [Documentación oficial de Git](https://git-scm.com/docs/git-pull)
- [Pro Git Book - Rebasing](https://git-scm.com/book/en/v2/Git-Branching-Rebasing)
