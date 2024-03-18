# Examen de recuperacion - Ramas

1. Fork y Clone del repositorio:

Accedo al repositorio original en GitHub.
Clic en el botón "Fork" para crear una copia del repositorio y ejecuto en local:
`git clone https://github.com/<tu_usuario>/<nombre_repositorio>.git`

2. Crear la rama "readme" y el Readme.md:

Creo una nueva rama llamada "readme" con el comando `git checkout -b readme`
Creo un archivo Readme.md en la raíz del proyecto.
En el archivo Readme.md, anoto los pasos que voy realizando en el ejercicio.

3. Unir las ramas Interface y Datos en main:

Cambio a la rama main con el comando `git checkout main`

Cambio a la rama Datos con el comando `git checkout Datos`
Fusiono la rama Datos en la rama main con el comando `git merge --squash --no-commit datos`

Me cambio a la rama Interface con el comando `git checkout Interface` y me doy cuenta de 
que el último commit no lo quiero añadir:

revierto el commit que deseo eliminar con el comando `git reset --hard HEAD~1`

El comando vuelve al commit anterior al HEAD y elimina los posteriores.

Ahora sí, fusiono las ramas Interface y datos en la rama main con el comando `git merge squash no-commit nombre-rama`

4. Etiquetar el último commit como v1.0:

Ejecuto un commit para delimitar el fusionado y 
creo una etiqueta para el último commit con el comando `git tag -a v1.0 -m "version 1.0"`

5. Completar el gitignore y añadirlo al commit v1.0:

Antes de hacer nada me doy cuenta de que el gitignore hay que añadirlo,
lo completo y lo añado al ultimo commit:

`git commit --amend` -> modifico el mensaje de commit a "...gitignore hecho"
Subo los cambios al repositorio remoto con el comando git push origin v1.0

6. Actualizar la release:

En la página de GitHub del repositorio, voy a la sección "Releases".
clic en "Create", selecciono el tag 1.0 y le pongo nombre a la release.

Por ultimo, termino y lanzo el readme a origin
