# Todo sobre `git diff` con ejemplos

## ¿Qué es `git diff`?

`git diff` es un comando que muestra las diferencias entre archivos o ramas en un repositorio Git. Permite ver qué líneas han cambiado antes de confirmar (`commit`) o entre diferentes commits, ramas, etc.

---

## Usos básicos

### 1. Ver cambios no confirmados (unstaged)

```bash
git diff
```

Muestra los cambios realizados en los archivos que aún no han sido añadidos al área de preparación (`staging area`).

---

### 2. Ver cambios preparados para commit (staged)

```bash
git diff --staged
```

Muestra las diferencias entre los archivos en el área de preparación y el último commit.

---

### 3. Comparar dos ramas

```bash
git diff rama1 rama2
```

Ejemplo:

```bash
git diff main feature-xyz
```

Muestra las diferencias entre las ramas `main` y `feature-xyz`.

---

### 4. Comparar dos commits

```bash
git diff commit1 commit2
```

Ejemplo:

```bash
git diff abc123 def456
```

Muestra los cambios entre los commits `abc123` y `def456`.

---

### 5. Ver diferencias en un archivo específico

```bash
git diff nombre_archivo
```

Ejemplo:

```bash
git diff README.md
```

---

### 6. Ver diferencias con formato resumen

```bash
git diff --stat
```

Muestra un resumen de los archivos modificados y el número de líneas añadidas/eliminadas.

---

### 7. Ver solo los nombres de archivos modificados

```bash
git diff --name-only
```

---

### 8. Ver diferencias en palabras, no líneas

```bash
git diff --word-diff
```

---

## Consejos útiles

- Puedes combinar opciones, por ejemplo:  
   `git diff --staged --stat`
- Usa `git difftool` para ver diferencias con herramientas gráficas.

---

## Recursos adicionales

- [Documentación oficial de git diff](https://git-scm.com/docs/git-diff)
- `git help diff` en la terminal
