# Merges en Git

El **merge** en Git es el proceso de combinar los cambios de dos ramas diferentes en una sola. Es fundamental para integrar trabajo colaborativo y mantener la historia del proyecto.

## Tipos de Merge

### 1. Fast-forward Merge

Ocurre cuando la rama de destino no tiene commits adicionales respecto a la rama que se va a fusionar.

```bash
git checkout main
git merge feature-branch
```

Si `main` no tiene cambios nuevos, simplemente avanza el puntero.

### 2. Merge con commit de merge

Sucede cuando ambas ramas tienen commits diferentes. Git crea un commit especial de merge.

```bash
git checkout main
git merge feature-branch
```

Si hay cambios en ambas ramas, se crea un commit de merge.

### 3. Merge con conflictos

Si los mismos archivos han sido modificados en ambas ramas, Git genera un conflicto que debes resolver manualmente.

```bash
git merge feature-branch
# Git indica los archivos en conflicto
# Edita los archivos y resuelve los conflictos
git add archivo-en-conflicto
git commit
```

## Ejemplo Práctico

1. Crear y cambiar a una nueva rama:
   ```bash
   git checkout -b nueva-funcionalidad
   ```
2. Realizar cambios y hacer commit:
   ```bash
   git add .
   git commit -m "Agrega nueva funcionalidad"
   ```
3. Cambiar a la rama principal y hacer merge:
   ```bash
   git checkout main
   git merge nueva-funcionalidad
   ```

## Comandos útiles

- Ver ramas:
  ```bash
  git branch
  ```
- Ver historial de merges:
  ```bash
  git log --graph --oneline
  ```
- Cancelar un merge en proceso:
  ```bash
  git merge --abort
  ```

## Buenas prácticas

- Haz pull antes de mergear para evitar conflictos.
- Resuelve los conflictos revisando cuidadosamente los cambios.
- Usa mensajes claros en los commits de merge.

## Recursos

- [Documentación oficial de Git](https://git-scm.com/doc)
- [Pro Git Book](https://git-scm.com/book/es/v2)
