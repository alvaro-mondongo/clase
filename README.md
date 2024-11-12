# Introducción a Github
#### _por Alvaro Collado Piqueras_

## Introducción
Antes de nada, es importante tener una noción general de qué es Github. Ya sea porque el lector de este texto pueda no haber escuchado de la plataforma nunca, o para refrescar conceptos.
Github es una plataforma para almacenar código. Este código se almacena de una forma especial, registrando solo los cambios en el código/los ficheros y la fecha en que se han hecho.
Esta finalidad es muy útil para tener un repositorio centralizado de nuestro trabajo, o el de la empresa para la que trabajamos. Porque, como podrás deducir de la frase anterior, también
permite compartir el código con otras personas, así como registrar quien ha hecho los cambios y asignar roles con restricciones.
A continuación veremos en más profundidad sus características principales.

## Características
#### Almacenar código en un repositorio centralizado
Es decir, permite crear/subir documentos en linea y acceder a ellos en cualquier momento. Con la seguridad/comodidad añadida de que está gestionado y respaldado por los servidores de Github. 
El proceso para crear un repositorio y añadir contenido es:
1. Crear una cuenta / iniciar sesión
2. En la página principal, a la izquierda, hacer click en "New"
3. Rellenar los datos: repository name, con el nombre que le queramos dar; luego escoger entre "Public" (público) o "Private" (privado)
4. Hacer click en "Create repository"
5. En la página del repositorio podemos hacer click en "Add file" y subir los archivos
Características generales:
- En la página principal, encontraremos el listado de nuestros repositorios a la izquierda
- Es necesario tener acceso a internet
- Se puede acceder/administrar el repositorio a través de la web de Github, la consola de comandos, o aplicaciones que implementen la API de Github
- Los repositorios pueden ser eliminados en cualquier momento

   
#### Colaborar con otras personas
Este acceso en línea se puede extender a más personas, permitiendo así el trabajo en grupo. Una característica muy relevante para proyectos de código abierto y para empresas, que no está disponible simplemente por medio de Git.
El trabajo en grupo viene con ventajas como:
* Desarrollo en paralelo, de distintas partes del proyecto
* Asignación de roles con permisos personalizados
* Incremento exponencial de la productividad
* Contribuciones de personas ajenas al proyecto

## Comandos relevantes
1. git init - el comando necesario para inicializar un repositorio en nuestro ordenador
2. git add archivo - comando para añadir archivos a la cola de cambios
   git add . - añade todos los archivos que hayan sido modificados desde el ultimo git add
3. git commit - coje todos los cambios en la cola de espera y crea un grupo de cambios, con una fecha asignada
4. git push - une/finaliza los cambios del commit al proyecto
5. git status - devuelve información sobre los cambios que se han hecho en el directorio en el que estemos
6. git config - permite configurar el repositorio
7. git clone dirección - clona un repositorio desde una url (dirección)

## Resumen
Github es una herramienta muy útil para el trabajo en equipo de los programadores. Permite tener un repositorio en línea donde registrar cambios y peticiones, así como organizar a los miembros de un equipo por medio de roles, e incluso aceptar colaboraciones independientes de miembros externos al equipo.


## Bibliografía
- https://www.simplilearn.com/tutorials/git-tutorial/what-is-git
- https://www.datacamp.com/blog/what-is-github
- https://github.blog/developer-skills/github/top-12-git-commands-every-developer-must-know/
