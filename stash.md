## ¿Para qué usamos `git stash` y por qué debemos usarlo?

Usamos `git stash` para guardar temporalmente los cambios que aún no queremos confirmar, permitiéndonos cambiar de rama o realizar otras tareas sin perder el trabajo en progreso. Es útil cuando necesitamos pausar lo que estamos haciendo y volver a un estado limpio del repositorio, asegurando que nuestros cambios no se mezclen accidentalmente con otros desarrollos. Así, podemos retomar fácilmente el trabajo guardado cuando lo necesitemos.

## ¿Qué es `git stash`?

`git stash` te permite guardar temporalmente los cambios en tu área de trabajo (working directory) y en el área de preparación (staging area) para que puedas cambiar de rama sin perder tu trabajo.

## Comandos básicos

### Guardar cambios

```bash
git stash
```

Guarda los cambios no confirmados y limpia el área de trabajo.

### Guardar con mensaje

```bash
git stash save "mensaje descriptivo"
```

Agrega una descripción al stash.

### Listar stashes

```bash
git stash list
```

Muestra todos los stashes guardados.

### Aplicar el último stash

```bash
git stash apply
```

Aplica el stash más reciente sin eliminarlo de la lista.

### Aplicar un stash específico

```bash
git stash apply stash@{n}
```

Aplica el stash número `n`.

### Eliminar el último stash después de aplicar

```bash
git stash pop
```

Aplica y elimina el stash más reciente.

### Eliminar un stash específico

```bash
git stash drop stash@{n}
```

Elimina el stash número `n`.

### Eliminar todos los stashes

```bash
git stash clear
```

Borra todos los stashes.

## Stash de archivos no rastreados o ignorados

- Para incluir archivos no rastreados:
  ```bash
  git stash -u
  ```
- Para incluir archivos ignorados:
  ```bash
  git stash -a
  ```

## Ver el contenido de un stash

```bash
git stash show stash@{n}
```

Para ver detalles completos:

```bash
git stash show -p stash@{n}
```

## Buenas prácticas

- Usa mensajes descriptivos para identificar fácilmente cada stash.
- Aplica y elimina los stashes que ya no necesitas para evitar confusiones.
- Recuerda que los stashes son temporales y pueden perderse si no se gestionan adecuadamente.

## Ejemplo de flujo de trabajo

1. Guardar cambios antes de cambiar de rama:
   ```bash
   git stash
   git checkout otra-rama
   ```
2. Recuperar los cambios:
   ```bash
   git stash pop
   ```

---

**Referencia oficial:** [Git Documentation - Stash](https://git-scm.com/docs/git-stash)
