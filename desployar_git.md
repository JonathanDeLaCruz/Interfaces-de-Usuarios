# Deployar a producción con GIT

## Requisitos

* [git](https://git-scm.com/downloads)
* [Cuenta en github](https://github.com/)

* Crear el archivo .gitignore con el siguiente contenido

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

## Pasos para subir proyecto a github

### Repositorio sin el archivo README.md

1. Crear un nuevo repositorio en github

   * El nombre de repositorio agreguen el nombre de su proyecto
   * Repositorio público
   * No añadas el README file

2. Abrir tu proyecto en él con VSCode

3. Ejecuta los siguientes comando en la terminal

  * Creamos el archivo README.md con el nombre de nuestro proyecto

    `echo "# repositorio" >> README.md`

  * Inicializamos el repositorio local

    `git init`

  * Añadimos todos los archivos al repositorio local

    `git add .`

  * Con el comando -m añadimos un mensaje que sea lo más descriptivo posible para identificar los cambios realizados

    `git commit -m "Mi proyecto en github"`

  * Seleccionamos la rama main que es la rama que se crea por defecto en nuestro proyecto

    `git branch -M main`

  * Creamos la conexión con el repositorio remoto con la ruta de nuestro repositorio

    `git remote add origin https://github.com/Usuario/repositorio.git`

  * Subimos los archivos al servidor

    `git push -u origin main`

### Repositorio con el archivo README.md

1. Crear un nuevo repositorio en github

   * El nombre de repositorio agreguen el nombre de su proyecto
   * Repositorio público
   * Añade el README file

2. Abrir tu proyecto en él con VSCode

3. Ejecuta los siguientes comando en la terminal

  * Inicializamos el repositorio local

    `git init`

  * Añadimos todos los archivos al repositorio local

    `git add .`

  * Con el comando -m añadimos un mensaje que sea lo más descriptivo posible para identificar los cambios realizados

    `git commit -m "Mi proyecto en github"`

  * Seleccionamos la rama main que es la rama que se crea por defecto en nuestro proyecto

    `git branch -M main`

  * Creamos la conexión con el repositorio remoto con la ruta de nuestro repositorio

    `git remote add origin https://github.com/Usuario/repositorio.git`

  * Descargamos del repositorio remoto el archivo README.md

    `git pull origin main --allow-unrelated-histories`

  * Subimos los archivos al servidor

    `git push -u origin main`

## Deployar a producción con GIT

  1. Seleccionamos en github en nuestro repositorio en la opción **Settings**

  2. Seleccionamos la opción **Pages**

  3. En el apartado **Branch** seleccionamos en donde dice ***None*** la rama donde se encuentra nuestro proyecto, en este manual sería la rama **main**

  4. Seleccionamos la ubicación de nuestro archivo index.html, que se debe encontrarse en **/ (root)** y seleccionamos la opción ***Save***

  5. El proceso de desployar a producción nuestro proyecto puede tardar un par de minutos, esperamos y recargamos la vista.

  6. Nos aparecerá el mensaje **Your site is live at https://usuario.github.io/repositorio/** que será la URL de nuestro proyecto ya funcionando.

## Subir cambios

* Añadimos todos los archivos al repositorio local

    `git add .`
    
* Con el comando -m añadimos un mensaje que sea lo más descriptivo posible para identificar los cambios realizados

    `git commit -m "Mi proyecto en github"`
    
* Subimos los archivos al servidor

    `git push -u origin main`
