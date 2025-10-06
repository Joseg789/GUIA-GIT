# Guía de `git log` con ejemplos

`git log` es el comando principal para ver el historial de commits en un repositorio de Git. Permite explorar los cambios realizados, quién los hizo y cuándo.

## Uso básico

```bash
git log
```

Muestra la lista de commits en orden cronológico inverso.

## Opciones comunes

### 1. Limitar la cantidad de commits

```bash
git log -n 5
```

Muestra solo los últimos 5 commits.

### 2. Mostrar en una sola línea

```bash
git log --oneline
```

Cada commit aparece en una sola línea (hash corto + mensaje).

### 3. Mostrar el historial de un archivo específico

```bash
git log -- <archivo>
```

Ejemplo:

```bash
git log -- README.md
```

### 4. Mostrar diferencias (diff) entre commits

```bash
git log -p
```

Incluye los cambios realizados en cada commit.

### 5. Formato personalizado

```bash
git log --pretty=format:"%h - %an, %ar : %s"
```

- `%h`: hash corto
- `%an`: autor
- `%ar`: tiempo relativo
- `%s`: mensaje

### 6. Mostrar gráfico de ramas

```bash
git log --oneline --graph --all
```

Visualiza el historial y las ramas como un gráfico ASCII.

### 7. Filtrar por autor

```bash
git log --author="Nombre"
```

### 8. Buscar por mensaje

```bash
git log --grep="palabra clave"
```

## Ejemplo combinado

```bash
git log --oneline --graph --decorate --all
```

Muestra el historial de todas las ramas, con referencias y en formato gráfico.

---

Consulta la [documentación oficial](https://git-scm.com/docs/git-log) para más detalles.
