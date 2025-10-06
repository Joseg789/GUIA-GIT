# Todo sobre los Commits en Git

## ¿Qué es un commit?

Un **commit** en Git es un registro de los cambios realizados en el repositorio. Cada commit guarda el estado del proyecto en un momento específico.
es como una fotografia del estado actual de nuestro proyecto
el cual nos permite mevernos en la linea de tiempo de desarrollo de nuestros proyectos

## ¿Cómo hacer un commit?

1. **Agregar archivos al área de preparación (staging):**
   ```bash
   git add archivo.txt
   ```
   O para todos los archivos modificados:
   ```bash
   git add .
   ```
2. **Crear el commit:**
   ```bash
   git commit -m "Mensaje descriptivo del cambio"
   ```

## Buenas prácticas para los commits

- Escribe mensajes claros y descriptivos.
- Haz commits pequeños y frecuentes.
- Relaciona cada commit con una sola funcionalidad o corrección.

## Ver el historial de commits

```bash
git log
```

Opciones útiles:

- `git log --oneline` (resumen)
- `git log --stat` (con archivos modificados)

## Modificar el último commit

```bash
git commit --amend
```

## Deshacer commits

- **Deshacer cambios antes de hacer commit:**
  ```bash
  git checkout -- archivo.txt
  ```
- **Eliminar el último commit (sin perder cambios):**
  ```bash
  git reset --soft HEAD~1
  ```
- **Eliminar el último commit (perdiendo cambios):**
  ```bash
  git reset --hard HEAD~1
  ```

## Compartir commits

Para enviar tus commits a un repositorio remoto:

```bash
git push origin rama
```

## Consultar detalles de un commit específico

```bash
git show <hash-del-commit>
```

---

**Resumen:**  
Los commits son la base del control de versiones en Git. Permiten registrar, documentar y compartir los cambios realizados en un proyecto de forma segura y ordenada.
