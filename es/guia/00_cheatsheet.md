# 00. Flutter Technical Documentation CheatSheet

Este archivo sirve para consulta rápida sobre formato de nombres, branch, commits y estimación de tareas.

Sino estas familizarizado te recomendamos leer las guias completas antes de comenzar a utilizar este CheatSheet. 

// TODO: Agregar los enlaces a las guias completas. 

## Formato Nombres

Como escribir:

- Directorios y carpetas: ``snake_case``  
- Archivos: ``snake_case``  
- Archivos Changelog.md y Readme.md: ``UPPERCASE``  
- Tipo de Branch: ``lowercase``  
- Prefijos Branch: ``kebab-case``  
- Clases, Enums, TypeDef, extentiones: ``UpperCamelCase``  
- Funciones y Métodos: ``lowerCamelCase``  
- Variables, Argumentos, Propiedades: ``lowerCamelCase``  

Para un descripción completa mira la Guía de Estilos Flutter


## Tipos de Commits

Prefijos que utilizamos al realizar commits.

- ``add``: Código Nuevo que se agrega al repo. 
- ``change`` ``update``: Cambio que se realiza en el codigo.
- ``fix``, ``hotfix`` ``bugfix``: Corrección que se realizo en el Código.   
- ``docs``: Cambio en la documentación. (sin cambio de código)  
- ``refactor``: Refactor en el Código
- ``deprecate``: Código que esta destinado a desaparecer, pero que aun se usa. 
- ``delete``: Código que se elimino del repositorio. 
- ``style``: Cambios en el codigo que mejoran su lectura.  

## Scope de Commits

El Scope de los commits varia dependiendo de la arquitectura del proyecto, pero en líneas generales, el Scope es brindado por el nombre de los directorios que contienen los archivos modificados.

## Prefijos de Branches

### Permanentes
- master/ main/
- qa/
- test/
- production/
- development/ develop/

### Temporales
- feature/ 
- bugfix/ 
- fix/ 
- hotfix/
- change/ 
- update/
- remove/
- merge/
- experimental/
- build/
- release/
- deprecate/
- security/
- performance/
- cicd/


## Estimación de Tareas
Para la estimacion de tareas nos basamos en la planning poker. 
El cual utiliza la sucesion de Fibonachi


| Estimacion | Descripcion           | 
|:----------:|:----------------------|
| 0          | Tarea trivial         | 
| 1          | Poco mas de medio día | 
| 2          | Poco mas de un día    | 
| 3          | Casi dos días         | 
| 5          | Poco mas de 3 días    | 
| 8          | Una semana            | 
| 13         | Una semana y media    | 
| 21         | Dos semanas o mas     | 