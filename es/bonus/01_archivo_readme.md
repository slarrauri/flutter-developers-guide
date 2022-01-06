# El Archivo Readme


En este documentos vamos a estar viendo las pautas y estructura para crear el archivo readme.md  de los proyectos Flutter. 

Intentaremos responder a las siguientes preguntas: 

- [El Archivo Readme](#el-archivo-readme)
  - [1. ¿Para que sirve?](#1-para-que-sirve)
  - [2. ¿Qué contiene?](#2-qué-contiene)
  - [3. ¿Cuál es su Estructura?](#3-cuál-es-su-estructura)
  - [4. Ejemplo de Archivo readme.md](#4-ejemplo-de-archivo-readmemd)

> [!NOTE]
>  1: Para escribir el archivo readme.md  utilizamos la nomenclatura de MarkDown

> [!NOTE]
>  2: el nombre del archivo debe escribirse con mayúsculas ej:  README.md 

> [!NOTE]
>  3: Algunas de las secciones pueden referir a documentación ya realizada, en tal caso, se coloca el enlace correspondiente.  

> [!NOTE]
>  4: lo recomendable es que el largo de cada reglón escrito no supere  los 80 caracteres. 

> [!NOTE]
>  5: Escribimos los textos en español, por ahora. Sin embargo términos de uso común pueden estar en ingles.  


## 1. ¿Para que sirve?

El objetivo del archivo readme es el de facilitar a los desarrolladores la documentación necesaria para utilizar y contribuir al desarrollo que se esta realizando. 

## 2. ¿Qué contiene?

Para tal fin, el archivo readme debe contener respuestas a las siguientes preguntas: 

¿Cómo Instalo el Proyecto?

¿Cómo ejecuto el Proyecto?

¿Cómo Contribuyo al Proyecto?

¿Cuál es la Estructura y Arquitectura del Proyecto?

¿Qué patrones de desarrollo utiliza? 

¿Hay ejemplos de uso? 

¿Dónde puedo usar la aplicación? 

¿Cómo generamos la documentación técnica del proyecto. 

¿Qué tipo de licencia tiene? 

¿Tiene dependencias externas? 

## 3. ¿Cuál es su Estructura?

Si bien hay diferentes estructuras que podemos utilizar en Pickers hemos optado por la siguiente: 

Nombre del proyecto: Generalmente el nombre de la aplicación

Descripción: Una descripción del proyecto que nos informe por que se realizo, que problemas resuelve, e información de alto nivel sobre el proyecto. Frameworks Versions. Store Links. 

Geting Started: En esta sección detallamos lo básico para instalar, ejecutar y contribuir al proyecto. 

Instalación: En esta sección definimos como configurar el entorno de desarrollo necesario para ejecutar el proyecto. 

Ejecución: Descripción de los pasos y configuraciones necesarias para ejecutar el proyecto en los diferentes ambientes disponibles. 

Contribución: Descripción de los procesos de contribución, por lo general GIT, GIT COMMITS, GIT FLOW, Guía de estilos y buenas practicas. 

In Deep: En esta sección describimos mas a fondo aspectos claves del proyectos: 

Estructura de la Aplicación

Arquitectura de la Aplicación

Manejadores de estado

Patrones de Diseño

Proceso CI/CD

Generar el Build

Documentación 

Datos de Color: En esta sección agregamos datos curiosos sobre el desarrollo, como por ejemplo cantidad de commits y MR realizados, cantidad de líneas de código escritas, si alguno de los devs se tiño el pelo, Eureka Momments y cosas por el estilo.

Para contar utilizamos Cloc:   

En los albores de la programación contar las líneas de código que escribía un desarrollador era la forma de medir su productividad. Claramente no fue la mejor, pero me parece divertida hoy en día. 

## 4. Ejemplo de Archivo readme.md  

Finalmente vamos a ver un ejemplo de un archivo readme con la estructura detallada anteriormente, el símbolo de dollar $ simboliza la entrada de un comando por consola. 
```markdown
# Ejemplo de README  
Este es un ejemplo de readme utilizando lo descripto anteriormente.
El prososito del mismo es servir de ejemplo y tambien como template  
a la hora de escribir estos archivos, esta seccion es la descripcion.   

## Getting Started  

  ### Prerequisitos  
  Para instalar y ejecutar correctamente este repositiorio  
  es necesario que cuentes con un IDE (Android Studios / VSCode / IntelliJ)  
  Flutter y Dart Instalados y configurados en la version: 
  - Flutter: v2.8
  - Dart: v2.15
  
  Puedes probar la app en: 
  IOS: 
  Android: 
  Web: 
  Windows:
  Linux:
  Mac: 
  
  ### Instalacion  
    1. Clona este repo. `$ git clone REPO_URL`  
    2. Run `$ flutter pub get` en el directorio principal de tu proyecto. 
    3. Run `$ flutter pub get` en el directorio de los paquetes externos. 
    
  ### Ejecucion 
  Contamos con diferentes ambientes para ejecutar nuestro proyecto. 
  Para ejecutar el proyecto en cada ambiente utiliza los siguientes comands de consola. 
  
  **IOS**
    - **QA**:   `$ flutter run --dart-define=environment=qa `  
    - **DEV**:  `$ flutter run --dart-define=environment=dev `  
    - **PROD**: `$ flutter run --dart-define=environment=prod `  
    
    **ANDORID**
    - QA   : `$ flutter run --flavor prod ` 
    - DEV  : `$ flutter run --flavor dev ` 
    - Prod : `$ flutter run --flavor prod ` 
    
     **WEB**
    - QA   : `$ flutter run --flavor prod ` 
    - DEV  : `$ flutter run --flavor dev ` 
    - Prod : `$ flutter run --flavor prod ` 
    
    **WEB**
    - QA   : `$ flutter run -d chrome --flavor prod ` 
    - DEV  : `$ flutter run -d chrome --flavor dev ` 
    - Prod : `$ flutter run -d chrome --flavor prod ` 
    
    **DESKTOP Windows**
    - QA   : `$ flutter run -d windows --flavor prod ` 
    - DEV  : `$ flutter run -d windows --flavor dev ` 
    - Prod : `$ flutter run -d windows --flavor prod `
  
  ### Contribucion
  Antes de comenzar a contribuir, te recomendamos te familizarices con: 
    1. [Nuestro Branch Model](https://www.example.com)
    2. [Guia de Estilos Flutter](https://www.example.com)
    3. [Buenas Practicas Flutter](https://www.example.com)
  
  ### In Deep
    1. Estructura de la Aplicación
    
    2. Arquitectura de la Aplicación
    
    3. Manejadores de estado
    
    4. Patrones de Diseño
  
    5. Proceso CI/CD
    
    6. Generar el Build
    
    7. Documentación
    
  ### Fun Facts
```

  
      


