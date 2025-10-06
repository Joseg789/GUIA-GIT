# Ramas en Git: Guía Completa

Las **ramas** en Git permiten desarrollar funcionalidades, corregir errores o experimentar de forma aislada del resto del proyecto. Son fundamentales para el trabajo colaborativo y el control de versiones.

---

## ¿Qué es una rama?

Una rama es una línea de desarrollo independiente. Por defecto, Git crea la rama `main` (o `master`). Puedes crear tantas ramas como necesites.

---

## Comandos básicos para gestionar ramas

### Ver ramas existentes

```bash
git branch
```

### Crear una nueva rama

```bash
git branch nombre-rama
```

### Cambiar de rama

```bash
git checkout nombre-rama
```

O, en versiones recientes:

```bash
git switch nombre-rama
```

### Crear y cambiar a una nueva rama

```bash
git checkout -b nombre-rama
```

O:

```bash
git switch -c nombre-rama
```

### Eliminar una rama

```bash
git branch -d nombre-rama
```

Para forzar la eliminación:

```bash
git branch -D nombre-rama
```

---

## Trabajar con ramas remotas

### Ver ramas remotas

```bash
git branch -r
```

### Subir una rama al repositorio remoto

```bash
git push origin nombre-rama
```

### Eliminar una rama remota

```bash
git push origin --delete nombre-rama
```

---

## Fusionar ramas (merge)

Para unir los cambios de una rama a otra:

1. Cambia a la rama de destino (por ejemplo, `main`):
   ```bash
   git checkout main
   ```
2. Fusiona la rama:
   ```bash
   git merge nombre-rama
   ```

---

## Rebase (reaplicar cambios)

El `rebase` reescribe el historial para aplicar los cambios de una rama sobre otra:

```bash
git checkout nombre-rama
git rebase main
```

---

## Editar el nombre de una rama

### Renombrar la rama actual

```bash
git branch -m nuevo-nombre
```

### Renombrar otra rama

```bash
git branch -m nombre-viejo nombre-nuevo
```

---

## Buenas prácticas

- Usa nombres descriptivos para las ramas.
- Trabaja en ramas separadas para cada funcionalidad o corrección.
- Elimina ramas que ya no uses.
- Sincroniza frecuentemente con el repositorio remoto.

---

## Recursos adicionales

- [Documentación oficial de Git](https://git-scm.com/doc)
- [Git Branching - Atlassian](https://www.atlassian.com/git/tutorials/using-branches)

---

¡Dominar las ramas te permitirá trabajar de forma más eficiente y segura en tus proyectos con Git!
