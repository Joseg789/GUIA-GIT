# Todo lo que debes saber sobre `git clone`

## ¿Qué es `git clone`?

`git clone` es un comando de Git que permite copiar un repositorio remoto a tu máquina local. Descarga todos los archivos, historial de commits y ramas.

## Sintaxis básica

```bash
git clone <url-del-repositorio>
```

## Ejemplo

```bash
git clone https://github.com/usuario/repositorio.git
```

## Opciones útiles

- **Clonar en un directorio específico**

  ```bash
  git clone <url> <nombre-del-directorio>
  ```

- **Clonar solo una rama**

  ```bash
  git clone --branch <nombre-rama> <url>
  ```

- **Clonar sin historial (shallow clone)**
  ```bash
  git clone --depth 1 <url>
  ```

## ¿Qué sucede al clonar?

- Se crea una copia local del repositorio.
- Se configura el remoto llamado `origin`.
- Puedes empezar a trabajar con el código y hacer cambios.

## Recomendaciones

- Verifica que tienes permisos para clonar el repositorio.
- Usa SSH para mayor seguridad si tienes acceso.
- Después de clonar, puedes usar otros comandos como `git pull`, `git push`, etc.

## Recursos adicionales

- [Documentación oficial de git clone](https://git-scm.com/docs/git-clone)
- [Guía rápida de Git](https://rogerdudler.github.io/git-guide/index.es.html)
