# Guía de Estilos Flutter/Dart

En este documento veremos las convenciones en nombres, estilos, idioma para escribir nuestro código Flutter / Dart.

## Idioma: 
Utilizaremos el idioma inglés, dado que es el idioma universal de la programación y ciertos procesos de auditoría requieren este idioma.


## Convenciones Nombres
Los nombres deberán de cumplir el siguiente formato:

**Directorios y Carpetas**: Minúsculas separadas por guión bajo (snake_case)  
**Archivos**: Minúsculas separadas por guión bajo (snake_case)  
**Archivos Changelog and Readme**: Todo en Mayúsculas (UPPERCASE)  
**Classes, enums, typedefs, extensions**: Primera letra de cada palabra en Mayúsculas (UpperCamelCase)   

Ejemplo: 
```dart
class MainScreen { ... }
enum MainItem { .. }
typedef Predicate<T> = bool Function(T value);
extension MyList<T> on List<T> { ... }
```

**Variables, constants, parameters, and named parameters**: Primera palabra en minúsculas subsiguientes primera letra de cada palabra en Mayúsculas (lowerCamelCase)   

```dart
var item;
const bookPrice = 3.14;
final urlScheme = RegExp('^([a-z]+):');
void sum(int bookPrice) {
 // ...
}
```

**Libraries, packages, directories, and source files usar**: lowercase_with_underscores. 
Ejemplos: 

```dart
library firebase_dynamic_links;
import 'socket/socket_manager.dart';
```

## Bloc Naming Conventions
**Eventos**
Los eventos deben nombrarse en tiempo pasado. 
Los eventos son cosas que ya han ocurrido desde la perspectiva del bloque. 

```dart
//SI
CounterStarted CounterIncremented CounterDecremented CounterIncrementRetried

//NO
Initial CounterInitialized Increment DoIncrement IncrementCounter
```


**Estados** 
Los estados deben ser sustantivos
Un estado es solo una impresión en un momento determinado.
El nombre de los estados deben terminar en algunas de las siguientes opciones.
`Initial | Success | Failure | InProgress`  


```dart
//SI
CounterInitial CounterLoadInProgress CounterLoadSuccess CounterLoadFailure

//NO
Initial Loading Success Succeeded Loaded Failure Failed
```


## Documentación
Para generar documentación usamos dartdoc. Esto genera una página web con la documentación dentro del código del proyecto. 

Para que dartdoc funcione, todos los comentarios que sean parte de la documentación deben iniciar con ///

Como comentar Clases:

```dart
/// Clase para el manejo de todas las rutas del proyecto
class Routes {

}
```
Las Clases se comentan arriba desde donde empieza a definirse. 
Los metodos Igual
Los Widget se docuentan en la primer linea dentro del widget, para seguir un mismom paro comcumentamos por fuera y usamos template. 



**Activar DartDocs**
Para activar dartdoc ejecutar en la terminal:

```dart
pub global activate dartdoc
// o esta otra opción: 
dart pub global activate dartdoc
```

**Generate Docs**
Para generar la documentación ejecutar este comando: 

```dart
dartdoc
```
Esto genera dentro del directorio . doc/api

Para dar estilo a la documentación se puede usar: Markdown

**Ver Documentación**
Para visualizar la documentación 

```dart
pub global activate dhttpd
dhttpd --path doc/api
```



