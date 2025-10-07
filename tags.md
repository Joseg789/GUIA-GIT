# Todo lo que debes saber sobre los tags en Git

## ¿Qué es un tag?

Un **tag** es una referencia que apunta a un commit específico. Se usa principalmente para marcar versiones importantes (por ejemplo, lanzamientos).

## Tipos de tags

- **Lightweight tag:** Solo apunta a un commit.
- **Annotated tag:** Incluye metadatos (autor, fecha, mensaje) y se almacena como un objeto en Git.

## Crear un tag

### Tag ligero

```bash
git tag nombre-del-tag
```

### Tag anotado

```bash
git tag -a nombre-del-tag -m "Mensaje del tag"
```

## Listar tags

```bash
git tag
```

Para buscar tags por patrón:

```bash
git tag -l "v1.*"
```

## Ver información de un tag anotado

```bash
git show nombre-del-tag
```

## Eliminar un tag local

```bash
git tag -d nombre-del-tag
```

## Subir tags al repositorio remoto

Por defecto, los tags no se suben con `git push`. Para subir todos los tags:

```bash
git push --tags
```

Para subir un tag específico:

```bash
git push origin nombre-del-tag
```

## Eliminar un tag remoto

```bash
git push --delete origin nombre-del-tag
```

## Usos comunes

- Marcar versiones de lanzamiento (`v1.0.0`, `v2.1.0`, etc.).
- Facilitar la recuperación de versiones específicas.
- Integración con herramientas de CI/CD.

## Buenas prácticas

- Usa tags anotados para versiones importantes.
- Sigue una convención de nombres (ejemplo: `v1.0.0`).
- Documenta los cambios en el mensaje del tag.

## Recursos adicionales

- [Documentación oficial de Git sobre tags](https://git-scm.com/book/en/v2/Git-Basics-Tagging)
- [SemVer: Versionado Semántico](https://semver.org/lang/es/)
