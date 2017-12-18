# <a name="microsoft-graph-quick-start-faq"></a>Preguntas frecuentes de inicio rápido de Microsoft Graph

En este documento de preguntas frecuentes encontrará respuestas a cuestiones relacionadas con los [inicios rápidos de Microsoft Graph](https://developer.microsoft.com/es-ES/graph/quick-start).

## <a name="what-do-the-quick-starts-do"></a>¿Qué hacen los inicios rápidos?

Los ejemplos de inicio rápido muestran cómo tener acceso a la potencia de Microsoft Graph. 

Si usa las API de REST de Office 365, debe autenticarse en cada servicio al que quiera llamar. Microsoft Graph elimina esta complejidad al unificar la autenticación y ofrecer acceso a todas las API a través de un único punto de entrada. Puede autenticarse una vez y obtener acceso a la información en múltiples aplicaciones y servicios. 

Los inicios rápidos de Microsoft Graph obtienen acceso a tres servicios con una autenticación: Cuenta Microsoft, OneDrive y Outlook. Cada inicio rápido obtiene acceso a la información de los perfiles de los usuarios de la cuenta Microsoft, escribe datos en OneDrive (una foto) y, después, genera un correo electrónico mediante Outlook (en el que se incluye un vínculo a la foto). 

Los inicios rápidos incluyen cuatro pasos:

- Seleccione la plataforma. 
- Obtenga el identificador de la aplicación (identificador del cliente)
- Compilación del ejemplo
- Inicie sesión y envíe una foto por correo electrónico.

Cuando complete el inicio rápido, tendrá una aplicación lista para ejecutarse.


## <a name="general-quick-start-sample-questions"></a>Preguntas de ejemplo de inicio rápido generales
En esta sección se responde a las preguntas sobre la organización y el contenido de los ejemplos de inicio rápido.

### <a name="why-does-my-quick-start-contain-a-readme-file"></a>¿Por qué mi inicio rápido contiene un archivo Léame?

Cada inicio rápido registra una nueva aplicación y crea un archivo ZIP que contiene el contenido de un repositorio de GitHub. Actualiza los archivos en el repositorio por lo que no tiene que configurar la aplicación de ejemplo en el repositorio. Encontrará estos repositorios en la [organización de MicrosoftGraph](https://github.com/microsoftgraph?utf8=%E2%9C%93&q=connect) en GitHub.

No dude en mirar el repositorio asociado con cada inicio rápido, si hay problemas de archivos o siga las instrucciones en el archivo Léame para registrar su propia aplicación. Para ir al repositorio, siga el vínculo **Just give me the sample code** (Darme solo el código de ejemplo) en el paso 2 de cada inicio rápido.

### <a name="which-microsoft-graph-features-do-the-quick-start-samples-use"></a>¿Qué funciones de Microsoft Graph usan los ejemplos de inicio rápido?

Actualizamos continuamente los ejemplos de inicio rápido. Para obtener las actualizaciones, vea el repositorio del ejemplo que le interesa. A medida que agreguemos características, actualizaremos el archivo Léame del ejemplo con la información nueva. En la tabla siguiente se muestran las funciones actuales de cada ejemplo.
 +<!-- Replace the check mark images with an actual character that can be read by a screen reader. Or you could add alt text to each instance of the image. -->

|Ejemplo|Autenticar|Obtener foto de perfil|Cargar foto en OneDrive|Compartir vínculo por correo electrónico|Adjuntar foto a correo electrónico|Enviar correo electrónico|
|-----:|-----:|-----:|------:|------:|------:|-----:|
|[Connect con Android](https://github.com/microsoftgraph/android-java-connect-sample)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|
|[Connect con Angular 2 ](https://github.com/microsoftgraph/angular-connect-sample)|![](./images/Check.PNG)| | | | |![](./images/Check.PNG)|
|[Connect REST con Angular 2 ](https://github.com/microsoftgraph/angular2-connect-rest-sample)|![](./images/Check.PNG)| | | | |![](./images/Check.PNG)|
|[Connect con ASP.NET](https://github.com/microsoftgraph/aspnet-connect-sample)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|
|[Connect para iOS: Swift](https://github.com/microsoftgraph/ios-swift-connect-sample)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|
|[Connect REST para iOS: Objective C](https://github.com/microsoftgraph/ios-objectivec-connect-rest-sample)|![](./images/Check.PNG)| | | | |![](./images/Check.PNG)|[](./images/Check.PNG)|
|[Connect REST para Node.js ](https://github.com/microsoftgraph/nodejs-connect-rest-sample)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)| |![](./images/Check.PNG)|
|[Connect REST para php](https://github.com/microsoftgraph/php-connect-rest-sample)|![](./images/Check.PNG)| | | | |![](./images/Check.PNG)|
|[Connect para php](https://github.com/microsoftgraph/php-connect-sample)|![](./images/Check.PNG)| | | | |![](./images/Check.PNG)|
|[Connect REST para Ruby](https://github.com/microsoftgraph/ruby-connect-rest-sample)|![](./images/Check.PNG)| | | | |![](./images/Check.PNG)|
|[Connect para UWP](https://github.com/microsoftgraph/uwp-csharp-connect-sample) |![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|
|[Connect para Xamarin](https://github.com/microsoftgraph/uwp-csharp-connect-sample)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|![](./images/Check.PNG)|

## <a name="authentication-and-authorization"></a>Autenticación y autorización
En esta sección se responde a preguntas relacionadas con problemas de autenticación y autorización. 

### <a name="why-dont-any-of-the-quick-start-samples-show-advanced-authentication-use-cases"></a>¿Por qué no muestran todos los ejemplos de inicio rápido casos de uso de autenticación avanzada?

Los ejemplos de inicio rápido le ofrecen una introducción a la autenticación y a las llamadas a la API de Microsoft Graph. Al agregar la autenticación y las llamadas a la API de Microsoft Graph a sus aplicaciones de producción, debe saber cómo se diseña para conseguir escenarios de autenticación avanzada relacionados con la seguridad y los problemas de acceso condicional.

Para encontrar más información sobre los escenarios de autenticación avanzada para la biblioteca de autenticación que usa, visite la página del editor de la biblioteca de autenticación:

- [OAuth2Client para iOS y Android](https://github.com/nxtbgthng/OAuth2Client)
- [Passport para Node](http://passportjs.org/)
- [Iluminar Auth para PHP](https://github.com/illuminate/auth)
- [Flask para Python 3](https://pypi.python.org/pypi/Flask-OAuth2-Provider/0.2.1)
- [OmniAuth para Ruby](https://github.com/omniauth/omniauth)
- [Biblioteca de autenticación de Microsoft (MSAL) para .NET](https://github.com/AzureAD/microsoft-authentication-library-for-dotnet)
- [Biblioteca de autenticación de Microsoft para Android](https://github.com/AzureAD/microsoft-authentication-library-for-android)
- [Biblioteca de autenticación de Microsoft para JavaScript](https://github.com/AzureAD/microsoft-authentication-library-for-js)

## <a name="microsoft-graph-api"></a>API de Microsoft Graph
En esta sección se responde a preguntas sobre la codificación de aplicaciones que usan las API de Microsoft Graph.

### <a name="i-didnt-get-an-email-and-i-dont-see-any-errors-or-exceptions-why-didnt-this-work"></a>No he recibido ningún correo electrónico y no veo errores ni excepciones. ¿Por qué no funciona?

Si parece que el ejemplo envía un correo electrónico, pero no lo ve en la Bandeja de entrada, compruebe la carpeta de correo no deseado o spam. Si va a enviar el mensaje desde un arrendatario de prueba, el mensaje podría marcarse como spam.

### <a name="why-doesnt-the-email-sent-by-the-sample-have-my-profile-picture"></a>¿Por qué el correo electrónico enviado por el ejemplo no tiene mi foto de perfil?

Esto suele ocurrir porque no se ha configurado el perfil con una foto de perfil de usuario. Si iniciado sesión con una cuenta Microsoft, incluso aunque tenga una foto de perfil, no aparecerá en el correo electrónico. La API de Microsoft Graph no es compatible actualmente con las fotos de perfil de usuarios de cuentas Microsoft. La mayoría de los ejemplos de los inicios rápidos obtiene su imagen de perfil y la carga en el directorio raíz de su cuenta de OneDrive. Si inicia sesión con una cuenta Microsoft (live.com, hotmail.com), Microsoft Graph actualmente no puede recuperar la foto de perfil, por lo que se revertirá a la imagen del bocadillo de pensamiento.

En los ejemplos de Node y Objective C para iOS no se adjuntan fotos de perfil de usuario al mensaje de correo. 

## <a name="aspnet"></a>ASP.NET
En esta sección se responde a preguntas relacionadas con la codificación, la compilación o la ejecución del ejemplo de inicio rápido de ASP.NET.

### <a name="why-wont-my-aspnet-project-build"></a>¿Por qué no se compila el proyecto ASP.NET?
Si un ejemplo que usa las bibliotecas de .NET no se puede compilar en Visual Studio, podría ejecutarse uno o varios de los proyectos contra el límite de longitud de 260 caracteres de la ruta de Windows . Intente mover la solución a una ubicación cerca del directorio raíz o en él. 

## <a name="universal-windows-platform-uwp"></a>Plataforma universal de Windows (UWP)
En esta sección se responde a preguntas relacionadas con la codificación, la compilación o la ejecución del ejemplo de inicio rápido de UWP.

### <a name="why-wont-my-uwp-project-build"></a>¿Por qué no se compila el proyecto UWP?
Si un ejemplo que usa las bibliotecas de .NET no se puede compilar en Visual Studio, podría ejecutarse uno o varios de los proyectos contra el límite de longitud de 260 caracteres de la ruta de Windows . Intente mover la solución a una ubicación cerca del directorio raíz o en él. 

## <a name="xamarin"></a>Xamarin
En esta sección se responde a preguntas relacionadas con la codificación, la compilación o la ejecución del ejemplo de inicio rápido de Xamarin.

### <a name="why-wont-my-xamarin-project-build"></a>¿Por qué no se compila el proyecto Xamarin?

Si un ejemplo que usa las bibliotecas de .NET no se puede compilar en Visual Studio, podría ejecutarse uno o varios de los proyectos contra el límite de longitud de 260 caracteres de la ruta de Windows . Las soluciones de Xamarin, en particular, son susceptibles a esto, especialmente proyectos de Android dentro de las soluciones Xamarin. Intente mover la solución a una ubicación cerca del directorio raíz o en él. 

## <a name="web-stack-samples"></a>Ejemplos de la pila web
En esta sección se responde a preguntas relacionadas con la codificación, la compilación o la ejecución de ejemplos de inicio rápido compilados con tecnología web.

### <a name="how-do-i-know-if-my-local-computer-supports-a-local-web-server"></a>¿Cómo sé si mi equipo local es compatible con un servidor web local?
Los ejemplos de inicio rápido basados en la tecnología web proporcionan la lógica necesaria para iniciar y hospedar un servidor web local. Por ejemplo, el ejemplo PHP basado en el tiempo de ejecución de PHP 5.4.0+ incluye un [servidor web integrado](http://php.net/manual/en/features.commandline.webserver.php) que usará para el desarrollo. No está pensado para usarse en un entorno de producción. 

Si ha descargado el ejemplo Node.js, lea la [guía de introducción de Node.js](https://nodejs.org/en/docs/guides/getting-started-guide/) para obtener información sobre cómo iniciar el servidor web de Node. 

Para el ejemplo de ASP.NET, Visual Studio 2015 y las versiones más recientes incluyen un servidor web de desarrollo que se inicia automáticamente al ejecutar el ejemplo. No es necesario configurar el proyecto de ejemplo para usar el servidor web. 

El [archivo Léame](https://github.com/microsoftgraph/ruby-connect-rest-sample/blob/master/README.md) del ejemplo connect de Ruby proporciona las instrucciones necesarias iniciar un servidor web local de Ruby. 

### <a name="if-a-web-platform-quick-start-provides-rest-and-sdk-samples-can-i-run-them-both-at-the-same-time"></a>Si un inicio rápido de plataforma web proporciona ejemplos SDK y REST, puedo ejecutar ambos al mismo tiempo?

Sí, puede ejecutar ambos ejemplos al mismo tiempo. Asegúrese de que uno de ellos no se está ejecutando en el puerto predeterminado. Esto significa que al iniciar el servidor web de prueba, debe especificar un número de puerto para al menos una versión del ejemplo.

### <a name="why-do-some-quick-starts-include-an-app-secret-and-others-dont"></a>¿Por qué algunos inicios rápidos incluyen un secreto de la aplicación y otros no?

Las aplicaciones de servidor web que necesitan realizar llamadas seguras a la API de Microsoft Graph requieren secretos de la aplicación. Por esta razón los inicios rápidos de ASP.NET MVC, Node.js, PHP y Ruby ofrecen un secreto de la aplicación.

### <a name="why-doesnt-the-angular-quick-start-give-me-an-app-secret-when-all-the-other-web-platform-quick-starts-do"></a>¿Por qué el inicio rápido de Angular no me da un secreto de la aplicación cuando todas las otras plataformas web de inicios rápidos lo hacen?

Un secreto de la aplicación es necesario solo para aplicaciones de servidor web.

### <a name="i-get-an-error-when-i-try-to-sign-in-and-authorize-the-sample-app-what-steps-can-i-take-to-fix-this"></a>Aparece un error al intentar iniciar sesión y autorizar la aplicación de ejemplo. ¿Qué puedo hacer para solucionar este problema? 

En primer lugar, intente ejecutar la aplicación de ejemplo en una ventana de InPrivate o Incognito. A veces la configuración de caché de explorador web puede causar que falle el paso de autorización, especialmente si inicia sesión con varias cuentas de Microsoft. Si eso no funciona, realice un seguimiento con nosotros en [Desbordamiento de pila](https://stackoverflow.com/questions/tagged/microsoft-graph). Asegúrese de etiquetar su pregunta con microsoft-graph y copie la información de error a la pregunta.

## <a name="didnt-find-what-you-need"></a>¿No encuentra lo que necesita?

Si estas preguntas frecuentes no resuelven su pregunta o problema relacionado con uno o varios de los inicios rápidos, notifíquelo en [Stack Overflow](https://stackoverflow.com/questions/tagged/microsoft-graph). Asegúrese de etiquetar su pregunta con microsoft-graph.

Si el problema está relacionado con el ejemplo de código proporcionado por el inicio rápido, también puede presentar un problema en el repositorio de ejemplo GitHub. Puede encontrar el repositorio siguiendo el vínculo **Darme solo el código de ejemplo** en el paso 2 para cada inicio rápido.
