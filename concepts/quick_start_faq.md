# <a name="microsoft-graph-quick-start-faq"></a>P+F de inicio rápido de Microsoft Graph

Esta P+F trata preguntas y problemas que podrían surgir al ejecutar a través de uno de los [inicios rápidos de Microsoft Graph](https://developer.microsoft.com/en-us/graph/quick-start).

## <a name="what-do-the-quick-starts-do"></a>¿Qué hacen los inicios rápidos?

Los ejemplos de inicio rápido muestran cómo tener acceso a la potencia de Microsoft Graph. 

Con las API de REST de Microsoft anteriores había que autenticarse en cada servicio al que quería llamar. Microsoft Graph elimina esta complejidad para los desarrolladores unificando la autenticación y combinando todos los puntos de entrada de API en un punto de entrada de la API de Graph. Ahora, se autentica una vez y obtiene el poder de tener acceso a la información en múltiples aplicaciones y servicios. 

A modo de ilustración, el ejemplo de inicio rápido de Microsoft Graph tendrá acceso a 3 servicios diferentes con una sola autenticación: Cuenta Microsoft, OneDrive y Outlook. Cada inicio rápido extraerá información de los perfiles de los usuarios de la cuenta Microsoft, la combinará con la escritura de datos en OneDrive (una foto) y, después, generará un correo electrónico mediante Outlook (en el que se incluye un vínculo a la foto). 

Hay cuatro pasos en cada inicio rápido para obtener una aplicación de ejemplo que esté lista para ejecutarse:
- Seleccione la plataforma. 
- Obtenga el identificador de la aplicación (también conocido como Id. de cliente).
- Compile el ejemplo.
- Inicie sesión y envíe una foto por correo electrónico.

>Nota: Estos pasos no están diseñados para ser código listo para producción; solo son unos ejemplos gráficos sencillos de cómo puede realizar el mismo escenario en muchas plataformas y lenguajes de programación diferentes. Una vez que realice un inicio rápido, se recomienda que [comprenda completamente la autenticación](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-authentication-scenarios) para crear aplicaciones listas para producción.


## <a name="general-quick-start-sample-questions"></a>Preguntas de ejemplo de inicio rápido generales
Preguntas sobre la organización y el contenido del conjunto de ejemplos de inicio rápido.

### <a name="why-does-my-quick-start-contain-a-readme-file"></a>¿Por qué mi inicio rápido contiene un archivo Léame?

Cada inicio rápido registra una nueva aplicación y crea un archivo ZIP que contiene el contenido de un repositorio de GitHub. Actualiza los archivos en el repositorio por lo que no tiene que configurar la aplicación de ejemplo en el repositorio. Encontrará estos repositorios en la [organización de MicrosoftGraph](https://github.com/microsoftgraph?utf8=%E2%9C%93&q=connect) en GitHub.

No dude en mirar el repositorio asociado con cada inicio rápido, si hay problemas de archivos o siga las instrucciones en el archivo Léame para registrar su propia aplicación. Siga el vínculo **Darme solo el código de ejemplo** en el paso 2 de cada inicio rápido para ir al repositorio asociado.

### <a name="which-microsoft-api-features-do-the-quick-start-samples-show"></a>¿Qué funciones de la API de Microsoft muestran los ejemplos de inicio rápido?

El conjunto de ejemplos se mejora continuamente. Inspeccione el repositorio de ejemplo que le interese. A medida que se agregan funciones a su ejemplo favorito, se anuncia la incorporación a través del archivo Léame del ejemplo. La siguiente tabla muestra las funciones actuales de cada ejemplo.

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
Preguntas relacionadas con problemas de autenticación y autorización. 

### <a name="why-dont-any-of-the-quick-start-samples-show-advanced-authentication-use-cases"></a>¿Por qué no muestran todos los ejemplos de inicio rápido casos de uso de autenticación avanzada?

Los ejemplos de inicio rápido le ofrecen una introducción a la autenticación y a las llamadas a la API de Microsoft Graph. Al agregar la autenticación y las llamadas a la API de Graph a sus aplicaciones de producción, debe saber cómo se diseña para conseguir escenarios de autenticación avanzada relacionados con la seguridad y los problemas de acceso condicional.

Puede encontrar más información sobre los escenarios de autenticación avanzada para la biblioteca de autenticación que usa si visita las páginas del editor de la biblioteca de autenticación.

- [OAuth2Client para iOS y Android](https://github.com/nxtbgthng/OAuth2Client)
- [Passport para Node](http://passportjs.org/)
- [Iluminar Auth para PHP](https://github.com/illuminate/auth)
- [Flask para Python 3](https://pypi.python.org/pypi/Flask-OAuth2-Provider/0.2.1)
- [OmniAuth para Ruby](https://github.com/omniauth/omniauth)
- [Biblioteca de autenticación de Microsoft (MSAL) para .NET](https://github.com/AzureAD/microsoft-authentication-library-for-dotnet)
- [Biblioteca de autenticación de Microsoft para Android](https://github.com/AzureAD/microsoft-authentication-library-for-android)
- [Biblioteca de autenticación de Microsoft para JavaScript](https://github.com/AzureAD/microsoft-authentication-library-for-js)

## <a name="microsoft-graph-api"></a>API de Microsoft Graph
Preguntas frecuentes sobre la codificación de la API de Microsoft Graph

### <a name="i-didnt-get-an-email-and-i-see-no-errors-or-exceptions-why-didnt-this-work"></a>No recibí un correo electrónico y veo que no hay errores ni excepciones. ¿Por qué no funciona?

Si parece que el ejemplo envía un correo electrónico, pero no lo ve en la Bandeja de entrada, compruebe la carpeta de correo no deseado o spam. Si va a enviar el mensaje desde un arrendatario de prueba, el mensaje podría marcarse como spam.

### <a name="why-doesnt-the-email-sent-by-the-sample-have-my-profile-picture"></a>¿Por qué el correo electrónico enviado por el ejemplo no tiene mi foto de perfil?

- Esto suele ocurrir porque no se ha configurado el perfil con una foto de perfil de usuario. Si iniciado sesión con una cuenta de servicio de Microsoft (MSA), entonces, incluso si tiene una foto de perfil, no aparecerá en el correo electrónico. La API de Microsoft Graph no es compatible con las fotos de perfil de usuarios de cuentas MSA. <br/>La mayoría de los ejemplos de los inicios rápidos obtiene su imagen de perfil y la carga en el directorio raíz de su cuenta de OneDrive. Si inicia sesión con una cuenta de Microsoft (live.com, hotmail.com), Microsoft Graph actualmente no puede recuperar la imagen del perfil, por lo que se revertirá a la imagen del bocadillo de pensamiento.

- En el ejemplo de Node y los ejemplos de Objective C para iOS no adjuntan fotos de perfil de usuarios al mensaje de correo electrónico. 

## <a name="asp-net"></a>ASP .NET
Preguntas relacionadas con la codificación, compilación o ejecución del ejemplo de inicio rápido de ASP.NET.

## <a name="universal-windows-platform-uwp"></a>Plataforma universal de Windows (UWP)
Preguntas relacionadas con la codificación, compilación o ejecución del ejemplo de inicio rápido de UWP.

## <a name="xamarin"></a>Xamarin
Preguntas relacionadas con la codificación, compilación o ejecución del ejemplo de inicio rápido de Xamarin.

### <a name="why-wont-my--aspnet-uwp-or-xamarin-project-build"></a>¿Por qué no se compilará el proyecto ASP.NET, UWP o Xamarin?

Si un ejemplo que usa las bibliotecas de .NET no se puede compilar en Visual Studio, podría ejecutarse uno o varios de los proyectos contra el límite de longitud de 260 caracteres de la ruta de Windows . Las soluciones de Xamarin, en particular, son susceptibles a esto, especialmente proyectos de Android dentro de las soluciones Xamarin. Intente mover la solución a una ubicación cerca del directorio raíz o en él. 

## <a name="web-stack-samples"></a>Ejemplos de la pila de Web
Preguntas relacionadas con la codificación, compilación o ejecución del ejemplo de inicio rápido compiladas con tecnología web.

### <a name="how-do-i-know-if-my-local-computer-supports-a-local-web-server"></a>¿Cómo sé si mi equipo local es compatible con un servidor web local?
Los ejemplos de inicio rápido basados en la tecnología web proporcionan la lógica necesaria para iniciar y hospedar un servidor web local. Por ejemplo, el ejemplo php basado en el tiempo de ejecución de php 5.4.0+ incluye un [servidor web incorporado](http://php.net/manual/en/features.commandline.webserver.php) que va a usar para el desarrollo. No está pensado para usarse en un entorno de producción. 

Si ha descargado el ejemplo Node.js, lea esta [guía de introducción de Node.js](https://nodejs.org/en/docs/guides/getting-started-guide/) para obtener información sobre cómo iniciar el servidor web de Node. 

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

Si estas preguntas más frecuentes no tratan una pregunta que tiene o un problema que encontró con uno o varios de los inicios rápidos, informe de su pregunta o problema a [Desbordamiento de pila](https://stackoverflow.com/questions/tagged/microsoft-graph). 

Si el problema está relacionado con el ejemplo de código proporcionado por el inicio rápido, también puede presentar un problema en el repositorio de ejemplo GitHub. Puede encontrar el repositorio siguiendo el vínculo **Darme solo el código de ejemplo** en el paso 2 para cada inicio rápido.
