# Documentación de la Release v1.0

## Introducción

Este proyecto tiene como objetivo realizar la **Release v1.0** del código disponible. La tarea consiste en seguir una serie de pasos que incluyen la creación de ramas, revisión de código, fusión de cambios y etiquetado de la versión  final. Todo el proceso se ha documentado en este archivo `README.md`.  

### Repositorio original:  
[https://github.com/damiancastelao/ExamenCOD](https://github.com/damiancastelao/ExamenCOD)  

## Pasos tomados para la versión v1.0  

### 1. **Fork del Repositorio**  
El primer paso consistió en realizar un **fork** del repositorio original proporcionado para tener nuestra propia   copia en GitHub. Esto es necesario para trabajar de forma independiente y luego hacer un Pull Request.  

- Realicé el fork del repositorio original en GitHub.  

### 2. **Clonación del Repositorio Forked**  
Después de hacer el fork, cloné el repositorio a mi máquina local para comenzar a trabajar en él.  

git clone https://github.com/tu-usuario/ExamenCOD.git  
cd ExamenCOD  

### 3. Creación de Ramas  

Para seguir las instrucciones del examen, creé las siguientes ramas:  

    main: Rama principal que solo contendrá commits etiquetados como releases.  
    datos: Rama para la clase de conexión a la base de datos.  
    interface: Rama para la parte gráfica del proyecto.  
    readme: Rama donde documenté todos los pasos que realicé durante el proceso.  

Para crear las ramas, utilicé los siguientes comandos:  

git checkout -b main  
git checkout -b datos  
git checkout -b interface  
git checkout -b readme  

### 4. Creación del README.md en la Rama readme  

En la rama readme, creé este archivo README.md para documentar todos los pasos realizados y las decisiones tomadas durante el desarrollo de la versión v1.0.  

Este archivo contiene información sobre el proceso, los problemas encontrados y las soluciones aplicadas.  

### 5. Revisión del Código en la Rama interface    

Al revisar la rama interface, descubrí que el último commit contenía código innecesario para la versión final. Para evitar que ese commit fuera incluido en la versión final, decidí revertirlo utilizando el siguiente comando:  

git checkout interface  
git revert HEAD  

Luego, realicé un commit con el mensaje "Revertido el último commit innecesario de la rama interface".  

### 6. Fusión de Ramas  

Una vez que se hicieron todos los ajustes, fusioné las ramas datos e interface en la rama main para integrar los cambios necesarios para la release.  

Para fusionar las ramas, utilicé los siguientes comandos:  

git checkout main  
git merge datos  
git merge interface  

### 7. Etiqueta del Commit con v1.0  

Una vez fusionadas las ramas en main, etiqueté el commit final con v1.0 para indicar que esta es la versión estable y lista para release. Utilicé el siguiente comando para crear la etiqueta:  

git tag -a v1.0 -m "Versión final v1.0"  

### 8. Push de la Rama main y la Etiqueta v1.0  

Después de realizar la fusión y etiquetar el commit, subí los cambios a GitHub:  

git push origin main  
git push origin v1.0  

### 9. Creación y Cierre de Issues  

A lo largo del proceso, se crearon varios issues relacionados con problemas encontrados en el código, como el último commit innecesario en la rama interface. Los issues fueron cerrados una vez que se resolvieron los problemas y se realizaron los commits correspondientes.  

### 10. Pull Request  

Finalmente, realicé un Pull Request desde mi repositorio forked hacia el repositorio original para fusionar las ramas main, datos e interface y así preparar la release.  

La descripción del Pull Request incluyó información detallada sobre los cambios realizados, como la fusión de ramas y el revertido del último commit en la rama interface.  

### 11. Revisión Final y Release  

Una vez realizada la fusión y verificados los cambios, la versión v1.0 del proyecto estuvo lista para su release. El código fue revisado y todo se encuentra documentado en este archivo README.md.  
Justificación de Decisiones  

    Revertir el último commit de la rama interface: Decidí no incluir el último commit de la rama interface porque contenía código que no era necesario para la versión final del proyecto. Este commit fue revertido para asegurarnos de que no se incluyera en la versión final.  

    Uso de ramas específicas: Creé ramas específicas para las distintas funcionalidades:  
        La rama datos contenía exclusivamente el código relacionado con la conexión a la base de datos.  
        La rama interface contenía el código para la parte gráfica.  
        La rama main es la rama final que contiene el código listo para release.  

    Uso de etiquetas: Etiqué el commit final como v1.0 para indicar que esta es la versión estable y lista para su liberación.  
