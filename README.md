Hacer un fork del repositorio:

    Visita la URL del proyecto: https://github.com/damiancastelao/ExamenCOD
    Haz clic en el botón "Fork" en la esquina superior derecha de la página para crear una copia del repositorio en tu cuenta de GitHub.

Clonar el repositorio en tu máquina local:

bash

git clone https://github.com/tu_usuario/ExamenCOD.git
cd ExamenCOD

Crear la rama readme:

bash

git checkout -b readme

Crear y editar el archivo Readme.md:

    Utiliza un editor de texto o IDE para crear y editar el archivo Readme.md en la rama readme, anotando los pasos, comandos y justificación de decisiones.

Volver a la rama main:

bash

git checkout main

Fusión (merge) sin incluir el último commit de la rama interface:

bash

git merge --no-commit --no-ff interface

Revertir el último commit de la rama interface:

bash

git reset HEAD~1

Añadir y confirmar los cambios para la fusión:

bash

git add .
git commit -m "Fusión de cambios de interface sin el último commit"

Etiquetar el último commit con v1.0:

bash

    git tag v1.0

    Actualizar el gitignore y añadirlo al commit v1.0:
        Edita el archivo .gitignore para completarlo según tus necesidades.

bash

git add .gitignore
git commit --amend

    Hacer push y crear la release:

    bash

git push origin main --tags

Crear una release en GitHub:

    Visita tu repositorio en GitHub.
    Ve a la pestaña "Releases".
    Haz clic en "Create a new release".
    Llena la información necesaria y selecciona la etiqueta v1.0.
    Publica la release.
