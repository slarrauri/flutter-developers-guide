# Dart Básico 
Si ya saber programar y esta guia te ayudara a comprender mejor los conceptos basicos de dart.

**Versions**
    - Dart 2.12
    - Flutter 2.2
  
**Enlaces de Interes**:
- [Efective Dart](https://dart.dev/guides/language/effective-dart): Buenas Practicas al usar Dart
- [Raywenderlich - Basic Dart](https://www.raywenderlich.com/22685966-dart-basics)

**Contenido**: 
- [Dart Básico](#dart-básico)
  - [Getting Started](#getting-started)
  - [Core Concepts](#core-concepts)
  - [Variables, Comentarios y Tipos de datos](#variables-comentarios-y-tipos-de-datos)
  - [Comentarios](#comentarios)
  - [Docs Commets](#docs-commets)
  - [Tipos  de Datos (Data Types)](#tipos--de-datos-data-types)
  - [Tipos de datos Básicos (Basic Data Types)](#tipos-de-datos-básicos-basic-data-types)
  - [el tipo dynamic](#el-tipo-dynamic)
  - [Boleanos (Booleans)](#boleanos-booleans)
  - [Operadores (Operators)](#operadores-operators)
  - [Operadores Aritméticos](#operadores-aritméticos)
  - [Operadores de Igualdad](#operadores-de-igualdad)
  - [Operadores de Comparación](#operadores-de-comparación)
  - [Operadores Lógicos](#operadores-lógicos)
  - [Textos (Strings)](#textos-strings)
  - [Escapando Strings](#escapando-strings)
  - [Inmutabilidad](#inmutabilidad)
  - [Nulidad (Nullability)](#nulidad-nullability)

## Getting Started

visit https://dart.dev/get-dart.

Why Dart?
Dart es parecido a  ``Java``, ``C#``, ``Swift`` y ``Kotlin``.

**Características**
- De tipeado Fuerte
- Con Inferencia de tipo de datos
- Con String expressions
- Multiparadigma, orientado a opjetos y funcional. 
- Con Null safety
- Multiplataforma Android, IOS, Web, Desktop (Win, Linux, Mac)

## Core Concepts
Los programas en __dart__ comienzan con una función llamada ``main`` como en  __C__, __Swift__ or __Kotlin__.


```dart
void main() {
 print("Hola Mundo"); 
}
```
Como puedes ver el el return type es void, significando que la función no retorna ningún valor. 

Dentro de la función  ``main`` se crea todo el código que sera la app. 
en esta caso utilizamos la funcion ``print()`` nativa de dart para __imprimir__ en pantalla el texto (string) "Hola Mundo"

A continuación veremos los siguientes conceptos

- Variables, comentarios y tipo de datos. 
- Tipos Básicos de Dart 
- operadores
- Strings
- Inmutabilidad
- NUlidad
- Condiciones y Break
- For Loops


## Variables, Comentarios y Tipos de datos

Ahora vamos a agregar una variable a nuestra funcion ``main`` y modificaremos la función print para que muestre nuestra variable. 

> [!IMPORTANT]
> Las sentencias en dart terminan con punto y coma (;)
> como en los lenguajes C o Java

```dart
var myAge = 35;  
```

Nos quedaria algo como esto:

```dart
void main() {
  var myAge = 42;
  print(myAge);
}
```

## Comentarios

Los comentarios en Dart son como en la mayoría de los lenguajes 
Los ``//`` representan una linea comentada y con ``/* ... */ `` podemos hacer bloques de texto comentado. 

Veamos un ejemplo: 

```Dart
// Este es un comentario de una linea.

print(myAge); // este tambien es un comentario de una linea

/*
Este es un comentario de multiples lineas. Son muy utiles para comentarios extensos
 */
```

## Docs Commets 

End ``Dart`` existen un tercer tipo de comentarios que son los usados para la documentación del código generado, estos comentarios comienzan con ``///``

Estos comentarios son muy útiles ya que nos permiten generar un documento en HTML con la documentación, para esto utilizamos la librería ``DartDoc``

Ejemplo: 
```Dart
/// Este es un comentario para documentar el código. 
```

## Tipos  de Datos (Data Types)

Dart es un lenguaje de tipado fuerte (statically typed) esto quiere decir que al momento de compilar el código Dart debe conocer el tipo de variable. El tipo de variable no puede cambiar cuando ejecuta el programa, como en C, Java, Swift, Kotlin, a diferencia de Python y Javascript, que son de tipado Débil (dynamically typed) esto quiere decir que las variables pueden contener distinto tipo de datos cuando se ejecuta el programa. 

>[!TIP] 
> Para saber el tipo de dato que tiene una variable puedes posicionar el puntero del mouse sobre la misma. 

``Dart`` puede inferir el tipo de dato de una variable cuando no se le asigna un tipo espesifico. 

Por ejemplo podemos declara la variable ``myAge`` con el tipo ``var`` y un valor de 42. Dart inferira el Data Type segun el valor asignado, en este caso sera un ``int``

```dart
var myAge = 42
```

## Tipos de datos Básicos (Basic Data Types)

Dart utiliza los siguientes tipos de datos: 

- `int`: numeros enteros. (42)
- `double`: numeros con decimales. (3.14)
- `bool`: bolleanos verdadero o falso (true o false)
- `string`: cadenas de texto ("Sebastian" + 'Larrauri')
- `dynamic`: Puede ser cualquiera de los tipos antes mencionados. (42/3.15/true/"Sebastian")
- 
- > [!TIP]
> `int` y `double` derivan the un tercer tipo llamdo `num`  
> `num` utiliza a su vez el tipo `dynamic` 

```dart
num numbers = 5; 

```
## el tipo dynamic
Las variables de tipo ``dynamic`` simulan a un lenguaje de tipado debil. 


Agreguemos estas lineas:
```Dart
// Probamos las variables Dinamicas
  dynamic numberOfView;

  numberOfView = 'No se han realizado Vistas';
  print(numberOfView);

  numberOfView = 1;
  print(numberOfView);
```
## Boleanos (Booleans)
Los boleanos son tipos de datos que pueden ir cambiando su valor entre: ``true`` o ``false``.

```dart
 // Boleanos
  bool areThereViews = false;
  print(areThereViews);

  // probemos cambia rel valor
  areThereViews = true;
  print(areThereViews);
```

## Operadores (Operators)
Dart tiene los operadores usuales tales como : 
- Aritméticos
- Igualdad
- incremento decremento
- comparación
- Lógicos

> [!NOTE]
> Operator overloading 
> https://en.wikipedia.org/wiki/Operator_overloading 

## Operadores Aritméticos

```dart
print(40 + 2); // 42

print(44 - 2); // 42

print(21 * 2); // 42

print(84 / 2); // 42.0
```
Para la división ``Dart`` infiere que el resultado sera un ``double``, por eso imprime 42.0 

Ademas usa los operadores aritméticos/asignación compuesto como por ejemplo: 

```dart
var value = 42.0;

value += 1; print(value); // 43.0

value -= 1; print(value); // 42.0

value *= 2; print(value); // 84.0

value /= 2; print(value); // 42.0

```
Estos operadores realizan dos tareas por ejemplo ``+=`` suma al valor de la derecha la cantidad de uno y luego asigna el resultado a la variable. 

un método abreviado de hacer lo mismo es ``++``

```dart
value = 42
value++;
print(value); // 43.0
```

Finalmente tenemos el operador modulo ``%`` que nos permite obtener el valor restante de una división. 

```dart
print(392 % 50); // 42
```

## Operadores de Igualdad

Dart cuenta con operadores de igualdad y desigualdad

```dart
print(42 == 43); // false

print(42 != 43); // true
```
## Operadores de Comparación 

Dart Utiliza los comparadores tipicos

- menor que
- mayor que
- menor e igual que
- mayor igual que

```dart
print(42 < 43); // true 
print(42 >= 43); // false
```

## Operadores Lógicos

Dart utiliza los operadores logicos clasicos como AND `&&` y OR `||`

```dart
print((41 < 42) && (42 < 43)); // true

print((41 < 42) || (42 > 43)); // true

```

El operador de negación es el símbolo de cierre de exclamación `!` y convierte lo verdadero en falso y lo falso en verdadero. 

```dart
print(!(41 < 42)); // false
```
> [!NOTE]
> Para una lista completa de los operadores disponibles inm dart visita: 
> https://dart.dev/guides/language/language-tour#operators 

## Textos (Strings)

Podemos ver los textos en dart ya que estan rodeados de comillas simples o dobles. 

```dart
var firstName = 'Albert';

String lastName = "Einstein";

```

Como en otros lenguajes puedes incrustrar el valor de una expresión en una cadena utilizando el símbolo de dolar ``${expresion]`` sila expresion es solo un identificador, se pueden omitir las llaves. 

```dart
var physicist = "$firstName $lastName likes the number ${84 / 2}";

print(physicist); // Albert Einstein

/*
$firstName and $lastName are replaced by the variable values. The returns the calculated result.
*/
```
## Escapando Strings
Escapar los textos nos sirve para mostrar los caracteres como `'` o `"` dentro de nuestros textos para hacerlos utilizamos `\`

Por ejemplo si tenes una linea de texto que representamos con comillas dobles y dentro del texto utilizamos comillas dobles. 

```dart
var quote = "Como dijo alguien alguna vez: \"la verdad es invisible a los ojos\" ";

print(quote);

// Como dijo alguien alguna vez: "la verdad es invisible a los ojos" 

```

Si se necesita mostrar los caracteres escapados se puede usar ``Raw Stings`` para hacerlo simplemente se agrega la letra ``r`` antes del ``string``

```dart
var rawString = r"If you can't explain it simply\nyou don't understand it well enough.";

print(rawString); 

// If you can't explain it simply\nyou don't understand it well enough.

```
En este ejemplo Dart trata a `\n` como si fuera texto normal. 

## Inmutabilidad 
Dart cuenta con las keywords ``const`` y ``final`` para valores que no cambian. 

usa ``const`` para variables que se conocen en tiempo de compilación y usar ``final`` para variables que no se conoce el valor y que el mismo una vez asignado no cambiara. 

```dart
const pi = 3.14;

print(pi); // 3.14
```
Dart infiere el ``type`` como ``double``

``final`` indica que la variable es inmutable y que no puede ser reasignado con otro valor. 

Podemos usar tanto ``final`` como ``const`` para las variables que no cambian, aunque ``final`` es mejor para valores que se crean cuando se corre el programa y ``const`` para constantes que ya se conocen. 

```dart
final planet = 'Jupiter';

// planet = 'Mars';

// error: planet can only be set once

final String moon = 'Europa';

print('$planet has a moon, $moon');

// Jupiter has a moon, Europa

```

## Nulidad (Nullability)

En el pasado Dart le daba a una varia sin valor el valor de ``null``
A partir de la version Dart 2.12, Dart se une a otros lenguajes como Swift o Kotlin para ser **non-nullable** por default

Adicionalmente Dart garantiza que los tipos non-nullable nunca contengan un valor ``null``, esto se conoces como **sound null safety**

Normalmente cuando se declara una variablew la misma debe iniciarse: 

```dart
String middleName = 'May';

print(middleName); // May
```
No todos tienen un segundo nombre por lo que tiene sentido hacer la variable **Nullable**. 

Para hacer una variable **Nullable** simplemente agrega ``?`` al final del tipo de variable: 

```dart
String? middleName = null;

print(middleName); // null
```

Por default el valor de una variable Nullable es ``null`` por lo que se puede simplificar la expresion a: 

```dart
String? middleName;

print(middleName); // null
```

Continue // TODO
