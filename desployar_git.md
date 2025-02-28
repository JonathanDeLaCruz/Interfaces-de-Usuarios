# Deployar a Producción con GIT

## Requisitos

* [Git](https://git-scm.com/downloads)
* [Cuenta en GitHub](https://github.com/)

### Crear el archivo `.gitignore` con el siguiente contenido:

```
node_modules/
package-lock.json
.DS_Store
npm-debug.log*
yarn-debug.log*
yarn-error.log*
.vscode/
.idea/
Thumbs.db
.env
```

## Pasos para subir un proyecto a GitHub

### Repositorio sin el archivo `README.md`

1. Crear un nuevo repositorio en GitHub:
   * Asigna el nombre de tu proyecto como nombre del repositorio.
   * Establece el repositorio como **público**.
   * No añadas el archivo `README.md`.

2. Abre tu proyecto en **VS Code**.

3. Ejecuta los siguientes comandos en la terminal:

   * Crea el archivo `README.md` con el nombre de tu proyecto:
     ```sh
     echo "# repositorio" >> README.md
     ```
   * Inicializa el repositorio local:
     ```sh
     git init
     ```
   * Añade todos los archivos al repositorio local:
     ```sh
     git add .
     ```
   * Agrega un mensaje descriptivo para identificar los cambios realizados:
     ```sh
     git commit -m "Mi proyecto en GitHub"
     ```
   * Selecciona la rama `main` (creada por defecto en el proyecto):
     ```sh
     git branch -M main
     ```
   * Crea la conexión con el repositorio remoto usando la URL de tu repositorio:
     ```sh
     git remote add origin https://github.com/Usuario/repositorio.git
     ```
   * Sube los archivos al servidor:
     ```sh
     git push -u origin main
     ```

### Repositorio con el archivo `README.md`

1. Crear un nuevo repositorio en GitHub:
   * Asigna el nombre de tu proyecto como nombre del repositorio.
   * Establece el repositorio como **público**.
   * Añade el archivo `README.md`.

2. Abre tu proyecto en **VS Code**.

3. Ejecuta los siguientes comandos en la terminal:

   * Inicializa el repositorio local:
     ```sh
     git init
     ```
   * Añade todos los archivos al repositorio local:
     ```sh
     git add .
     ```
   * Agrega un mensaje descriptivo para identificar los cambios realizados:
     ```sh
     git commit -m "Mi proyecto en GitHub"
     ```
   * Selecciona la rama `main` (creada por defecto en el proyecto):
     ```sh
     git branch -M main
     ```
   * Crea la conexión con el repositorio remoto usando la URL de tu repositorio:
     ```sh
     git remote add origin https://github.com/Usuario/repositorio.git
     ```
   * Descarga del repositorio remoto el archivo `README.md`:
     ```sh
     git pull origin main --allow-unrelated-histories
     ```
   * Sube los archivos al servidor:
     ```sh
     git push -u origin main
     ```

## Deployar a producción con GitHub Pages

1. En **GitHub**, accede a tu repositorio y selecciona la opción **Settings**.
2. Desplázate hasta la sección **Pages**.
3. En el apartado **Branch**, selecciona la rama donde se encuentra tu proyecto (en este caso, `main`).
4. En la ubicación del archivo `index.html`, selecciona **/ (root)** y haz clic en **Save**.
5. El proceso de despliegue puede tardar unos minutos. Espera y recarga la página.
6. Una vez completado, aparecerá el mensaje:
   ```
   Your site is live at https://usuario.github.io/repositorio/
   ```
   Esta será la URL de tu proyecto en producción.

## Subir cambios

Cada vez que realices cambios en tu proyecto, sigue estos pasos para subirlos a GitHub:

* Añade todos los archivos al repositorio local:
  ```sh
  git add .
  ```
* Agrega un mensaje descriptivo para identificar los cambios realizados:
  ```sh
  git commit -m "Actualización de proyecto"
  ```
* Sube los archivos al servidor:
  ```sh
  git push -u origin main
  ```

