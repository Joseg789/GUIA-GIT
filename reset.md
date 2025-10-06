# Todo lo que debes saber sobre `git reset`

## ¿Qué es `git reset`?

`git reset` es un comando de Git que se utiliza para deshacer cambios en el historial de commits, el área de preparación (staging area) y/o el directorio de trabajo.

## Modos principales de `git reset`

### 1. `--soft`

- **Sintaxis:** `git reset --soft <commit>`
- **Efecto:** Mueve el puntero de la rama al commit especificado. Los cambios posteriores quedan en el área de staging.
- **Uso común:** Deshacer commits recientes pero mantener los cambios listos para volver a commitear.

### 2. `--mixed` (por defecto)

- **Sintaxis:** `git reset --mixed <commit>` o simplemente `git reset <commit>`
- **Efecto:** Mueve el puntero de la rama y actualiza el área de staging. Los cambios quedan en el directorio de trabajo como archivos modificados.
- **Uso común:** Quitar archivos del área de staging pero conservar los cambios en el directorio de trabajo.

### 3. `--hard`

- **Sintaxis:** `git reset --hard <commit>`
- **Efecto:** Mueve el puntero de la rama, actualiza el área de staging y el directorio de trabajo. **Se pierden los cambios no guardados.**
- **Uso común:** Descartar completamente los cambios realizados después de un commit específico.

## Ejemplos prácticos

```bash
git reset --soft HEAD~1
# Elimina el último commit, pero mantiene los cambios en staging

git reset HEAD~1
# Elimina el último commit, los cambios quedan como archivos modificados

git reset --hard HEAD~1
# Elimina el último commit y todos los cambios realizados después de ese commit
```

## Precauciones

- **`--hard` es destructivo:** Los cambios no guardados se perderán.
- Si ya has compartido los commits (push), evita usar `reset` en ramas públicas; prefiere `git revert`.

## Diferencias con otros comandos

- **`git revert`:** Crea un nuevo commit que deshace los cambios, sin modificar el historial.
- **`git checkout` y `git restore`:** Se usan para restaurar archivos o moverse entre ramas, pero no alteran el historial de commits como `reset`.

## Resumen visual

| Modo    | Historial | Staging | Working Dir |
| ------- | --------- | ------- | ----------- |
| --soft  | ✔️        | ✔️      | ✔️          |
| --mixed | ✔️        | ❌      | ✔️          |
| --hard  | ✔️        | ❌      | ❌          |

✔️ = mantiene cambios, ❌ = descarta cambios

---

**Recomendación:** Antes de usar `git reset --hard`, asegúrate de no perder trabajo importante.
