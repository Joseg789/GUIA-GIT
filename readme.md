# Sintaxis de Git para Gestionar Repositorios

## 1. Configuración Inicial

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@ejemplo.com"
git config --list
```

- Configura tu nombre y correo para los commits.

---

## 2. Crear y Clonar Repositorios

```bash
git init
```

- Inicializa un nuevo repositorio en el directorio actual.

```bash
git clone <url-del-repositorio>
```

- Clona un repositorio remoto en tu máquina local.

---

## 3. Estado y Seguimiento de Cambios

```bash
git status
```

- Muestra el estado de los archivos.

```bash
git add <archivo>
git add .
```

- Añade archivos al área de preparación (staging).

```bash
git diff
```

- Muestra diferencias entre archivos modificados y el último commit.

---

## 4. Confirmar Cambios (Commits)

```bash
git commit -m "Mensaje descriptivo"
```

- Guarda los cambios preparados con un mensaje.

```bash
git commit -am "Mensaje"
```

- Añade y confirma archivos ya seguidos por Git.

---

## 5. Historial y Revisión

```bash
git log
```

- Muestra el historial de commits.

```bash
git log --oneline --graph --all
```

- Historial resumido y visual.

---

## 6. Ramas (Branches)

```bash
git branch
```

- Lista ramas locales.

```bash
git branch <nombre-rama>
```

- Crea una nueva rama.

```bash
git checkout <nombre-rama>
```

- Cambia a otra rama.

```bash
git checkout -b <nombre-rama>
```

- Crea y cambia a una nueva rama.

---

## 7. Fusionar Cambios (Merge)

```bash
git merge <nombre-rama>
```

- Fusiona la rama especificada en la rama actual.

---

## 8. Repositorios Remotos

```bash
git remote add origin <url>
```

- Añade un repositorio remoto.

```bash
git remote -v
```

- Lista los repositorios remotos.

---

## 9. Sincronización con Remoto

```bash
git fetch
```

- Descarga cambios del remoto sin fusionar.

```bash
git pull
```

- Descarga y fusiona cambios del remoto.

```bash
git push
```

- Envía tus commits al remoto.

---

## 10. Deshacer Cambios

```bash
git checkout -- <archivo>
```

- Restaura un archivo al último commit.

```bash
git reset HEAD <archivo>
```

- Quita un archivo del área de preparación.

```bash
git revert <id-commit>
```

- Crea un nuevo commit que revierte uno anterior.

---

## 11. Eliminar Archivos y Ramas

```bash
git rm <archivo>
```

- Elimina un archivo y lo prepara para commit.

```bash
git branch -d <nombre-rama>
```

- Elimina una rama local.

---

## 12. Etiquetas (Tags)

```bash
git tag <nombre>
```

- Crea una etiqueta en el último commit.

```bash
git tag -a <nombre> -m "Mensaje"
```

- Crea una etiqueta anotada.

---

> **Consejo:** Usa `git help <comando>` para más detalles sobre cualquier comando.
