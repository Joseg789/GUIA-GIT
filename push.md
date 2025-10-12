# Git Push: Todo lo que Debes Saber

`git push` es el comando que se utiliza para subir los cambios locales de tu repositorio a un repositorio remoto (por ejemplo, GitHub, GitLab, Bitbucket).

## Sintaxis Básica

```bash
git push <remote> <branch>
```

- `<remote>`: El nombre del repositorio remoto (por defecto suele ser `origin`).
- `<branch>`: El nombre de la rama que quieres subir.

## Ejemplo Básico

```bash
git push origin main
```

Sube los cambios de la rama `main` al repositorio remoto llamado `origin`.

## Ejemplo con Nueva Rama

```bash
git checkout -b feature/nueva-funcionalidad
git push origin feature/nueva-funcionalidad
```

Crea una nueva rama y la sube al remoto.

## Subir Todas las Ramas

```bash
git push --all origin
```

Sube todas las ramas locales al remoto.

## Subir Etiquetas (Tags)

```bash
git push origin --tags
```

Sube todas las etiquetas al remoto.

## Forzar el Push

```bash
git push --force origin main
```

Forza el push sobrescribiendo los cambios en el remoto (¡Úsalo con precaución!).

## Push Automático con Configuración de Upstream

Si es la primera vez que subes una rama:

```bash
git push -u origin nombre-de-la-rama
```

La opción `-u` configura la rama remota como upstream, facilitando futuros `git push` y `git pull`.

## Verificar Remotos

```bash
git remote -v
```

Muestra los repositorios remotos configurados.

## Errores Comunes

- **Rechazo por cambios en el remoto:**  
   Solución: Haz un `git pull` antes de hacer push.
- **Permisos insuficientes:**  
   Verifica tus credenciales o acceso al repositorio.

## Resumen

- `git push` sube tus cambios al remoto.
- Especifica el remoto y la rama.
- Usa `-u` para configurar upstream.
- Usa `--force` solo si sabes lo que haces.

## Recursos

- [Documentación oficial de Git](https://git-scm.com/docs/git-push)
- [Guía de GitHub sobre push](https://docs.github.com/es/push)
