# Buenas Practicas Flutter

En este documento se detallan las buenas prácticas que el equipo de desarrollo debe implementar en la escritura de código.

Sin nada más que agregar, ¡A darle Átomos!

- [Buenas Practicas Flutter](#buenas-practicas-flutter)
  - [Pubspec File](#pubspec-file)
  - [readme File](#readme-file)
  - [Changelog File](#changelog-file)
  - [Control de Versiones](#control-de-versiones)
  - [Imports](#imports)
  - [Tipos de Variables](#tipos-de-variables)
  - [Condicionales](#condicionales)
  - [AS / IS](#as--is)
  - [Spreed Collection](#spreed-collection)
  - [Escapando Strings Largos](#escapando-strings-largos)
  - [NULL Values](#null-values)
  - [Arrow Functions](#arrow-functions)
  - [Debuging](#debuging)
  - [Extract Method](#extract-method)
  - [List Builder](#list-builder)
  - [Arquitectura BLOC](#arquitectura-bloc)


## Pubspec File
En este archivo se debe agregar la version de Flutter que esta usando el proyecto. Esto es opcional en algunas versiones de FLutter y en otras no se puede realizar, cuando no se pueda, agregarlo como un comentario.

```yaml
(...)
dependencies:
  flutter:
    sdk: flutter ^2.0.0
  (...)
```

## readme File
El proyecto debe contar con un archivo readme.md

## Changelog File
El proyecto debe contar con un archivo changelog.md

## Control de Versiones

Para el control de versiones utilizamos Git con metodología basada en Git-Flow y la nomenclatura a utilizar está basado en el Versionado Semántico

**Nomenclatura**: X.Y.Z+B

|Column1  |Column2  |Column3  |
|:--:|---------|---------|
|X   |Mayor    | Suma 1 cuando se integra una branch que contenga un commit del tipo, ``BREAKING CHANG(!)``|
|Y   |Minor    | Suma 1 cuando se integra una branch del tipo: feature, new, add|
|Z   |Patch    | Suma 1 cuando se integra otro tipo de branch.|
|B   |Build    | Suma uno con cada nuevo build que se libera en producción, es el número por el cual las Stores de Google y Apple, gestionan las apps.|

## Imports

Usar rutas relativas dentro del directorio: `/lib`

```dart
import '../../../utils/dialog_utils.dart';

import './utils/snackbar_utils.dart';

// Para importar paquetes usar import

import 'package:flutter/material.dart';
```


## Tipos de Variables
Declaraciones de Variables Especificar el `Type`, evitar usar `var`

```dart
//SI

int item = 10;

final Car bar = Car_()_;

String name = 'john';

const int timeOut = 20;

//NO

var item = 10;

final car = Car_()_;

const timeOut = 2000;
```

## Condicionales

Usar `if condition` en vez de `conditional expression` muchas veces tenemos que renderizar un widget según la plataforma. Si la expresión condicional retorna null nunca se mostrará el widget.

```dart
//SI
Widget getText_(BuildContext context) {_
return Row_(_
    children:[
    Text_("Hello")_,
  if (Platform.isAndroid) Text_("Android")_
  ]
  );
}

//NO
Widget getText_(BuildContext context) {_
return Row_(_
    children: [
      Text_("Hello")_,
  Platform.isAndroid ? Text_("Android")_ : null,
  Platform.isAndroid ? Text_("Android")_ : SizeBox_()_,
  Platform.isAndroid ? Text_("Android")_ : Container_()_,
  ]
  );
}
```


## AS / IS
Evitar usar `as` usar** `is`

```dart
//SI

if (item is Animal)

item.name = 'Lion';

//NO

(item as Animal).name = 'Lion';
```


## Spreed Collection

Operador `spreed collection` Se usa para agregar una lista con valores a otra.

```dart
//SI

var y = [4,5,6];

var x = [1,2,...y];

//NO

var y = [4,5,6];

var x = [1,2];

x.addAll(y);
```

## Escapando Strings Largos

raw string Opcional: Sirve para no tener que escapar caracteres.

```dart
var s = r'This is demo string \ and $';
```

## NULL Values
Valores null En dart los valores null son iniciados automáticamente.
```dart
//SI

int _item;

//NO

int _item = null;
```


## Arrow Functions

The => (arrow) Para funciones que contienen solo una expresión.

```dart
//SI

get width => right - left;

Widget getProgressBar_()_ => CircularProgressIndicator_(_

valueColor: AlwaysStoppedAnimation_<Color>(Colors.blue)_,

);

//NO

get width {

return right - left;

}

Widget getProgressBar_() {_

return CircularProgressIndicator_(_

valueColor: AlwaysStoppedAnimation_<Color>(Colors.blue)_,

);

}
```

## Debuging
Usar debugPrint()

`print()` y `debugPrint()` se usa para imprimir en la consola Aveces al usar `print()` la salida es demasiado grande y Android descarta algunas lineas, para evitar esto usar: `debugPrint ()`.

## Extract Method
```dart

```
Separar widgets en widgets mas pequeños.

Cuando se llama a `setState()`, todos los widgets descendientes se reconstruyen.

Por lo tanto, Dividir el widget en widget mas pequeños hace que `setState()` llame a la parte de la UI que necesita cambiar.


## List Builder

Use ListView.builder para listas largas

Cuando trabaje con listas infinitas o listas muy grandes, Por lo general, es recomendable utilizar un constructor de `ListView` para mejorar el rendimiento.

El constructor `ListView` predeterminado construye la lista completa a la vez.

`ListView.builder` crea una lista diferida, cuando el usuario se desplaza hacia abajo en la lista,

```dart
Scaffold(

appBar: CustomAppBar(title: "Verify Code"), // Sub Widget

body: Container(

child: Column(

crossAxisAlignment: CrossAxisAlignment.start,

children: <Widget>[

TimerView( // Sub Widget

key: _timerKey,

resendClick: () {})

],

),

),

)
```
## Arquitectura BLOC 

``providers``: Cambios que se apliquen dentro de esa capa.
``models``: Cambios que apliquen dentro de ese directorio.
``repositories``: Cambios que se apliquen dentro de ese directorio.
``modules``: Cambios que se apliquen dentro de esta layer.
``designs``: Cambios que se apliquen dentro de ese layer.
``core``:  Cambios que se hagan en el core de la aplicación. 
``tests``: cambios que se hagan en los directorios test.