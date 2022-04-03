# El Archivo Changelog

En esta sección vamos a estar viendo para que sirve el archivo changelog, como crearlo, actualizarlo y como nos ayuda en nuestro desarrollo y detención de bugs. 

- [El Archivo Changelog](#el-archivo-changelog)
  - [¿Para que sirve el changelog?](#para-que-sirve-el-changelog)
  - [El Formato del Changelog](#el-formato-del-changelog)
  - [Escructura](#escructura)
  - [Ejemplo CHANGELOG.md:](#ejemplo-changelogmd)

## ¿Para que sirve el changelog? 
La principal funcionalidad del Changelog es llevar un control de los cambios que se realizaron al proyecto. Esto nos ayuda a tener un control sobre lo que hemos realizado e integrado en el proyecto. 

El changelog se construirá utilizando los Merge Request que se integren al proyecto y se actualizara cada vez que se haga un nuevo build productivo o de test. 

## El Formato del Changelog
Cada nueva actualización al changelog debe contener el numero de version de la app, la fecha en que se realizo y el listado de branch mergeadas al proyecto. 

## Escructura 
Cada rama creada contiene una categoría que se relaciona con una sección del changelog, según la siguiente estructura: 

- **Added**: Para funcionalidades nuevas. Esta sección contendrá el listado de los nombres de la Rama feature, add, new. 
- **Changed**: Para los cambios en las funcionalidades existentes. Esta sección contendrá el listado de los nombres de la Rama change, refactor.
- **Fixed**: Para corrección de errores. Esta sección contendrá el listado de los nombres de la Ramas bugfix, fix, hotfix.
- **Removed**: Para las características en desuso que se eliminaron en esta versión. Esta sección contendrá el listado de los nombres de la Rama remove.
- **Security**: En caso de vulnerabilidades. Esta sección contendrá el listado de los nombres de la Rama security.
- **Deprecated**: Para indicar que una característica o funcionalidad está obsoleta y que se eliminará en las próximas versiones. Esta sección contendrá el listado de los nombres de la Rama deprecated.

## Ejemplo CHANGELOG.md: 

```markdown
# ChangeLog

## v0.29.0+0 - 06/12/2021
    - add/upload-images
    
## v0.28.0+0 - 29/11/2021
    - add/back-arrow-ar
    - fix/auth-login-message' into
    
## v0.27.0+0 - 25/11/2021
    - add/consumir-servicios-stepper
```