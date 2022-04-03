# Materiales para las Stores y algo mas. 

Aqui encontraras una recopilacion de las cosas que necesitas antes de deployar el desarrollo en las stores. 

- [Materiales para las Stores y algo mas.](#materiales-para-las-stores-y-algo-mas)
  - [Cuentas y Credenciales](#cuentas-y-credenciales)
  - [Para Iniciar el Desarrollo](#para-iniciar-el-desarrollo)
  - [Stores Information](#stores-information)
    - [Google Play](#google-play)
    - [Apple Store](#apple-store)

## Cuentas y Credenciales
1. Credenciales de acceso a cuenta de Firebase, para integrar Analytics y Crashlytics y Notificacionies Push: En el caso que sea necesario ser necesario.  

2. Credenciales de acceso a cuenta de Google Cloud, para generar las api key necesarias para integrar los servicios de google. En el caso que sea necesario ser necesario .  

3. Agregar cuenta de los Devs a las cuentas de Apple Store y Google Play con los permisos necesarios, para poder generar los certificados y hacer la publicación en las stores correspondientes. En el caso que sea necesario ser necesario.  


## Para Iniciar el Desarrollo

**Nombre del Paquete**: (no se puede cambiar una vez que se publica en la tienda)
Este nombre es un identificador único. Generalmente esta conformado por el dominio de la aplicación invertido, seguido del nombre de la aplicación. 

Ejemplo: 
```dart
ar.com.nombredelsitioweb.nombredelaapp
```
**Launch Screen Assets**
Imagen, logo o animación Lotie para agregar a la pantalla de Inicio de la App.

**Launch Icon**
Icono para abrir la aplicación. 
Para generar los iconos se puede usar: 
- https://appicon.co/
- https://appiconmaker.co/ 
- https://easyappicon.com/

## Stores Information

### Google Play

**Nombre App**
Es el nombre con el que figura en la tienda. (no se puede cambiar)hasta 50 caracteres.  

**Descripción corta**
Una descripción de la app corta, hasta 80 caracteres.   

**Descripción larga**
Descripción detallada de la aplicación. hasta 4000 caracteres.   

**Icono de la aplicación**
(resolución 512x512 siendo un archivo PNG de 32 bits) 

**Capturas de Pantalla**
Dependiendo el alcance de la aplicacion se necesitaran capturas de pantallas de todos los tipos de dispositivos. 

    - Mobiles: Srchivo JPEG o PNG de 24 bits(sin alfa). Mínimo 2 capturas, Máximo 8.
    - Tablets: ¿?

**Tipo de Aplicacion**
Hay que elgir entre dos tipos: 
    - Aplicación
    - Juego

**Categorias**
Dependiendo el tipo de aplicacion se mostraran diferentes categorias para seleccionar. 

**Etiquetass**
Estad etiquetas son las palabras claves por las que podrá ser indexada la aplicación en las búsquedas y estadísticas.

**Datos Empresa**
    - Empresa o individuo que va a subir esta aplicación al Store. 
    - Sitio web. 
    - Correo Electrónico de contacto. 
    - Teléfono de contacto. 
    - Sitio web de la política de privacidad(Opcional obligatorio si la app registra usuarios, debe ser una pagina HTML) 

### Apple Store
**Nombre App**  
Es el nombre con el que figura en la tienda. (no se puede cambiar)hasta 50 caracteres.  

**Descripción corta**  
Una descripción de la app corta, hasta 80 caracteres.   

**Descripción larga**  
Descripción detallada de la aplicación. hasta 4000 caracteres.  

**Categorias Primaria**  
Dependiendo el tipo de aplicacion se mostraran diferentes categorias para seleccionar. 
Books, Business, 
Education, Entertainment, Finance, Games, Health & Fitness, Lifestyles, Medical, Music, Navigation, News, Photo & Video, Productivity, Reference, Social Networking, Sports,Travel, Utilities, Weather

**Categoria Secundaria**  
Idem Anterior

**Capturas de Pantalla**  
Dependiendo el alcance de la aplicacion se necesitaran capturas de pantallas de todos los tipos de dispositivos. 

    - Mobiles: Necesitaremos al menos 3 imágenes de 1242 x 2208 (iPhone 5.5) y 3 imágenes de 2688 x 1242 (iPhone 6.5 inch), que sean screenshots de la App. 
    - Tablets: ¿?
- 

**Un Texto Promocional**   
El texto promocional le permite informar a sus visitantes de la App Store sobre cualquier característica actual de la aplicación sin requerir un envío actualizado.
Este texto aparecerá sobre su descripción en la App Store para clientes con dispositivos con iOS 11 o posterior y macOS 10.13 o posterior.


**Keywords**  
Incluya una o más palabras clave que describan su aplicación. Las palabras clave hacen que los resultados de búsqueda de App Store sean más precisos. 
Separe las palabras clave con una coma.

**Url de soporte**  
Una URL con información de soporte para su aplicación. Esta URL estará visible en la App Store

**Marketing Url**  
 el cual es opcional. (na URL con información de soporte para su aplicación. Esta URL estará visible en la App Store.
 
**Copyright**  
El nombre de la persona o entidad que posee los derechos exclusivos de su aplicación, precedido por el año en que se obtuvieron los derechos (por ejemplo, "2008 Acme Inc."). No proporcione una URL.

**App User Test Information**  
Este es un nombre de usuario y contraseña que podemos usar para iniciar sesión en su aplicación, por lo que podemos revisar todas sus funciones. 
Si los usuarios inician sesión usando las redes sociales, proporcione información para una cuenta que podamos usar. 
Las credenciales deben ser válidas y activas durante la duración de la revisión. 

Es necesario crear una cuenta Demo en el ambiente de PROD. Que pueda ser usada por Apple para realizar la revisión.

**Información de Contacto**  
La persona de su organización a la que se debe contactar si el equipo de Revisión de aplicaciones tiene alguna pregunta o necesita información adicional 
  - Nombre completo
  - Número de Contacto directo
  - Email 

**Información adicional**  
sobre su aplicación que puede ayudar durante el proceso de revisión. Incluya la información que pueda ser necesaria para probar su aplicación, como la configuración específica de la aplicación.


**Datos Empresa**
    - Empresa o individuo que va a subir esta aplicación al Store. 
    - Sitio web. 
    - Correo Electrónico de contacto. 
    - Teléfono de contacto. 
    - Sitio web de la política de privacidad(Opcional obligatorio si la app registra usuarios, debe ser una pagina HTML) 
