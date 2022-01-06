# Git & Git Flow
En este documento se explica la metodología Git y Git Flow a utilizar por el equipo de desarrollo Flutter.  

En la misma veremos el formato a utilizar para escribir los commits y crear branchs.  

Es importante mantener esta estructura ya que se utiliza para generar el versionado y changelog del proyecto. 

- [Git & Git Flow](#git--git-flow)
  - [Convenciones de estilo](#convenciones-de-estilo)
  - [Branches](#branches)
  - [Branch Permanentes](#branch-permanentes)
  - [Branch Temporales](#branch-temporales)
  - [Commits](#commits)
  - [Git Flow](#git-flow)

## Convenciones de estilo
Los nombres de directorios, ramas, etiquetas, commits deben cumplir con el siguiente formato:

**Idioma**: Inglés.
**Largo del mensaje**: hasta 80 caracteres. 

**Branch folder**: ``lowercase`` ej: feature/
**Branch Name**: ``kebab-case `` ej: feature/branch-name
**Tags**: ``lowercase`` ej: v0.0.0
**Commits**: ``lowercase`` ej: docs(core): add new feature login

> [!IMPORTANT]
> los textos de commit y los nombres de las branchs deben ser legibles y descriptivos.
 
## Branches
Veamos ahora cómo nombraremos nuestras branchs. 

Tenemos dos tipos de branchs permanentes y temporales, estas últimas se borran al Mergearse con una branch permanente. 

Los nombres de las branches estarán formados por una categoría o folder, seguida del nombre de la funcionalidad o tarea en la cual se está trabajando.

## Branch Permanentes
Dentro de las branchs permanentes la categoría representa el estado dentro del flujo de desarrollo y estas son: 

**Categorías Branchs Permanentes**

``master o main``: Dentro de esta rama se encuentra el código que actualmente esta producción y es una rama protegida. Solo se puede integrar código en esta rama que provenga de alguna subrama de qa, hotfix o develop, siendo esta ultima generalmente la más utilizada. 

``qa o test``: Rama que está siendo testeada por QA. Las diferentes versiones estarán marcadas con un tag de formato “v0.0.0” 

``demo``: Rama con funcionalidades para demostraciones, los nombres de esta rama están formados por la versión o funcionalidad/tarea que se desea mostrar. . ej: demo/3.7.2 - demo/login 
Las subramas que no se están utilizando dentro de demo pueden borrarse, debiendo mantener siempre al menos una versión, generalmente la última. 

``develop o development``: Es la rama principal del proyecto en desarrollo y es desde donde se crean las ramas temporales y las permanentes. Al mismo tiempo las ramas temporales se integran en esta rama.

> [!IMPORTANT]
> Al iniciar un nuevo proyecto en git se debe crear al menos la rama develop o development.


## Branch Temporales
Estas branch deben crearse desde la branch develop, ya que es la branch que contiene el código actualizado y que ya ha pasado por “Code Review” 

Dentro de las branchs temporales la categoría representa la acción que se está realizando dentro del proyecto y es usada para formar las categorías del archivo changelog.md

El nombre de la branch debe estar formado por la tarea o funcionalidad en la cual se está trabajando. 

**Categorías Branchs Temporales**:
``feature, add, new/``: Rama para el desarrollo de nuevas funcionalidades y/o código nuevo que se integre en el desarrollo. ej: add/list-of-users
``bugfix/``: Rama para solucionar Bugs. ej: bugfix/login-redirect-to-user-list
``fix/``: Rama para solucionar, errores en general. 
ej: fix/logout
``hotfix/``: Rama donde se solucionan problemas críticos. Esta rama puede integrarse directamente en master o main por el líder técnico del equipo. 
ej: hotfix/sum-of-cost-by-month
``change/``: Rama para cambios en funcionalidades existentes.
ej: change/list-of-users
``deprecate/``: Rama para indicar que una característica o funcionalidad está obsoleta y que se eliminará en las próximas versiones.
ej: depracate/like-button
``security/``: Rama para solucionar vulnerabilidades de seguridad.
ej: security/input-card-number
``remove/``: para remover código que ya estaba en producción. 
ej: remove/like-button
``merge/``: Una Rama para resolver conflictos en el código. Esta Rama no se Mergea en ninguna rama permanente y no es tenida en cuenta para la realización del changelog.
ej: merge/conflict-list-of-users
``experimental/``: Rama para hacer pruebas y experimentos. Esta Rama no se integra en ninguna rama permanente y no es tenida en cuenta para la realización del changelog.
ej: experimental/logo-animation
``build/``:Una Rama para crear y trackear Builds.  Esta Rama no se integra en ninguna rama permanente y no es tenida en cuenta para la realización del changelog. Por lo general no se usa.
ej: build/0.7.3 
``release/``:Rama para hacer un seguimiento de las Releases. Esta Rama no se integra en ninguna rama permanente y no es tenida en cuenta para la realización del changelog. Por lo general no se usa.
ej: release/0.7.3

> [!NOTE]
> Los nombres de las branch los pueden crear según los nombres de las tareas que se están realizando, agregando la categoría correspondiente. Por ejemplo: feature/singup

> [!IMPORTANT]
> Las ramas merge, experimental, build y release, no se integran en ninguna rama permanente, en el caso de merge o experimental, se deberá crear otra rama utilizando la categoría y nombre acorde. 


## Commits
Los nombres de los commits están compuestos por un tipo, un scope y un texto descriptivo. 

- El tipo representa ¿Que acción se realizó en el código?
- El scope representa ¿ Dónde se realizo en la estructura de carpetas?
- El texto explica ¿Que es lo que se hizo?

ej: add(login/ui): update the text of login buttons 

NOTA: El texto debe ser descriptivo de lo que se hizo y legible. 

**Tipos de Commits**
- ``add``: Código Nuevo que se agrega al repo. 
- ``change`` ``update``: Cambio que se realiza en el codigo.
- ``fix``, ``hotfix`` ``bugfix``: Corrección que se realizo en el Código.   
- ``docs``: Cambio en la documentación. (sin cambio de código)  
- ``refactor``: Refactor en el Código
- ``deprecate``: Código que esta destinado a desaparecer, pero que aun se usa. 
- ``delete``: Código que se elimino del repositorio. 
- ``style``: Cambios en el codigo que mejoran su lectura.  

**Scopes de Commits**
El scope está definido por la arquitectura que se utilice en el proyecto, siendo la principal BLOC, posteriormente se agregarán otras arquitecturas. 


**Atom Commits**. 
Los commits deben contener pocos cambios, siendo lo usual, un commit por cambios en un archivo. 

En este video les voy a estar mostrando como realizar commits efectivos, fáciles de gestionar y  legibles por cualquier miembro del equipo, incluso aquellos sin conocimientos técnicos. 

Commits Efectivos: https://www.youtube.com/watch?v=js0MMkg4VkA 

**Breaking Change**
Finalmente tenemos un tipo especial de commit que sirve para identificar cuando el código que se agrega rompe la compatibilidad con versiones anteriores del proyecto. 

Por ejemplo puede ocurrir que un endpoint deje de existir y haya que cambiarlo, este cambio hará que las versiones anteriores del desarrollo dejen de funcionar. 

Los commits que cumplan con esta condición son marcados como Breaking Change utilizando el texto BREAKING CHANGE, después del texto del commit. 	

Ejemplo Breaking Change: 

change(models): change multiple var types. BREAKING CHANGE


## Git Flow
Git Flow representa el flujo de trabajo a realizar para integrar el código generado en la rama de producción del proyecto. 

Git Flow:  https://www.youtube.com/watch?v=4_tKNcBv6LM  

Resumen:
En caso de que no exista se crea la branch develop o development
Creamos la rama temporal en la cual vamos a trabajar siguiendo la nomenclatura antes mencionada por ejemplo agregamos una nueva feature add/reset-password
Realizamos el trabajo y comiteamos según corresponda siguiendo la nomenclatura para los commits.  
Realizamos el Merge Request a Develop, asignando a la persona que realizará el Code Review.
Realizamos el Code Review.
Se acepta o rechaza el MR en caso de ser rechazado se explican los motivos.


MR Aceptado
Se integra en Develop. 
Se crea la Rama para qa. 


1. MR Rechazado
Vuelve al autor para su corrección y repite el flujo desde el paso 3. 


QA Aceptado
Se integra en Master y de ser necesario se crean las ramas para demostraciones. 
QA Rechazado
Vuelve al autor para su corrección y repite el flujo desde el paso 3.


Fin del Flujo Git-Flow






