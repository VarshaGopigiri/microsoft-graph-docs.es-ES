# <a name="microsoft-graph-quick-start-faq"></a>P+F de inicio rápido de Microsoft Graph

Esta P+F trata preguntas y problemas que podrían surgir al ejecutar a través de uno de los [inicios rápidos de Microsoft Graph](https://developer.microsoft.com/en-us/graph/quick-start).

## <a name="what-do-the-quick-starts-do"></a>¿Qué hacen los inicios rápidos?

Independientemente de la plataforma que elija, cada inicio rápido hace lo siguiente:

- Registra una nueva aplicación para el usuario en el [Portal de registro de la aplicación](https://apps.dev.microsoft.com). Por esta razón le pedimos que inicie sesión con una cuenta de Microsoft cuando se **obtenga un id. de la aplicación**. Si la aplicación requiere un secreto de la aplicación, el inicio rápido creará uno para usted. 
- Descarga una copia del código de ejemplo que se almacena en un repositorio de GitHub. Puede ver estos repositorios en la [organización de MicrosoftGraph](https://github.com/microsoftgraph?utf8=%E2%9C%93&q=connect) en GitHub.
- Inserta el id. de la aplicación nueva y donde es necesario el secreto de la aplicación, en un archivo de configuración en el código de ejemplo que se almacena en el repositorio de GitHub. No deseamos enviar información confidencial dentro de una solicitud de HTTP, por lo que le pedimos que copie el secreto de la aplicación después de crear la aplicación nueva y, a continuación, cópielo en un formulario en el inicio rápido antes de descargar una copia del ejemplo.
- Le pide descargar todo el ejemplo configurado. Después de descargar y descomprimir el código de ejemplo, tendrá una aplicación web o cliente que debería ejecutar, suponiendo que ha instalado los requisitos previos especificados (IDE, marcos de trabajo web, etc.) en el entorno de desarrollo.


## <a name="why-wont-my--aspnet-uwp-or-xamarin-project-build"></a>¿Por qué no se compilará el proyecto ASP.NET, UWP o Xamarin?

Si un ejemplo que usa las bibliotecas de .NET no se puede compilar en Visual Studio, podría ejecutarse uno o varios de los proyectos contra el límite de longitud de 260 caracteres de la ruta de Windows . Las soluciones de Xamarin, en particular, son susceptibles a esto, especialmente proyectos de Android dentro de las soluciones Xamarin. Intente mover la solución a una ubicación cerca del directorio raíz o en él. 

## <a name="if-a-web-platform-quick-start-provides-rest-and-sdk-samples-can-i-run-them-both-at-the-same-time"></a>Si un inicio rápido de plataforma web proporciona ejemplos SDK y REST, puedo ejecutar ambos al mismo tiempo?

Sí, puede ejecutar ambos ejemplos al mismo tiempo. Asegúrese de que uno de ellos no se está ejecutando en el puerto predeterminado. Esto significa que al iniciar el servidor web de prueba, debe especificar un número de puerto para al menos una versión del ejemplo.

## <a name="i-didnt-get-an-email-and-i-see-no-errors-or-exceptions-why-didnt-this-work"></a>No recibí un correo electrónico y veo que no hay errores ni excepciones. ¿Por qué no funciona?

Si parece que el ejemplo envía un correo electrónico, pero no lo ve en la Bandeja de entrada, compruebe la carpeta de correo no deseado o spam. Si va a enviar el mensaje desde un arrendatario de prueba, el mensaje podría marcarse como spam.

## <a name="i-get-an-error-when-i-try-to-sign-in-and-authorize-the-sample-app-what-steps-can-i-take-to-fix-this"></a>Aparece un error al intentar iniciar sesión y autorizar la aplicación de ejemplo. ¿Qué puedo hacer para solucionar este problema? 

En primer lugar, intente ejecutar la aplicación de ejemplo en una ventana de InPrivate o Incognito. A veces la configuración de caché de explorador web puede causar que falle el paso de autorización, especialmente si inicia sesión con varias cuentas de Microsoft. Si eso no funciona, realice un seguimiento con nosotros en [Desbordamiento de pila](https://stackoverflow.com/questions/tagged/microsoft-graph). Asegúrese de etiquetar su pregunta con microsoft-graph y copie la información de error a la pregunta.

## <a name="why-do-some-quick-starts-include-an-app-secret-and-others-dont"></a>¿Por qué algunos inicios rápidos incluyen un secreto de la aplicación y otros no?

Las aplicaciones de servidor web que necesitan realizar llamadas seguras a la API de Microsoft Graph requieren secretos de la aplicación. Por esta razón los inicios rápidos de ASP.NET MVC, Node.js, PHP y Ruby ofrecen un secreto de la aplicación.

## <a name="why-doesnt-the-angular-quick-start-give-me-an-app-secret-when-all-the-other-web-platform-quick-starts-do"></a>¿Por qué el inicio rápido de Angular no me da un secreto de la aplicación cuando todas las otras plataformas web de inicios rápidos lo hacen?

Un secreto de la aplicación es necesario solo para aplicaciones de servidor web.

## <a name="why-does-my-quick-start-contain-a-readme-file"></a>¿Por qué mi inicio rápido contiene un archivo Léame?

Cada inicio rápido registra una nueva aplicación y crea un archivo ZIP que contiene el contenido de un repositorio de GitHub. Actualiza los archivos en el repositorio por lo que no tiene que configurar la aplicación de ejemplo en el repositorio. Encontrará estos repositorios en la [organización de MicrosoftGraph](https://github.com/microsoftgraph?utf8=%E2%9C%93&q=connect) en GitHub.

No dude en mirar el repositorio asociado con cada inicio rápido, si hay problemas de archivos o siga las instrucciones en el archivo Léame para registrar su propia aplicación. Siga el vínculo **Darme solo el código de ejemplo** en el paso 2 de cada inicio rápido para ir al repositorio asociado.

## <a name="why-did-the-sample-give-me-an-image-containing-a-thought-bubble"></a>¿Por qué el ejemplo me proporciona una imagen que contiene un bocadillo de pensamiento?

La mayoría de los ejemplos de los inicios rápidos obtiene su imagen de perfil y la carga en el directorio raíz de su cuenta de OneDrive. Si inicia sesión con una cuenta de Microsoft (live.com, hotmail.com), Microsoft Graph actualmente no puede recuperar la imagen del perfil, por lo que se revertirá a la imagen del bocadillo de pensamiento. El ejemplo también usa esta imagen si su cuenta no tiene una imagen de perfil.

## <a name="why-do-you-provide-a-manage-your-apphttpsappsdevmicrosoftcom-link-after-i-get-an-app-id"></a>¿Por qué proporciona un vínculo ** [Administrar su aplicación](https://apps.dev.microsoft.com) ** después de obtener un id. de la aplicación?

Proporcionamos este vínculo porque el paso del id. de la aplicación registra una nueva aplicación para el usuario en el [Portal de registro de la aplicación](https://apps.dev.microsoft.com). Proporcionamos este vínculo para que pueda ver la configuración de esta aplicación, eliminar la aplicación o incluso actualizar la configuración de la aplicación después de ejecutar el ejemplo. 

## <a name="didnt-find-what-you-need"></a>¿No encuentra lo que necesita?

Si estas preguntas más frecuentes no tratan una pregunta que tiene o un problema que encontró con uno o varios de los inicios rápidos, informe de su pregunta o problema a [Desbordamiento de pila](https://stackoverflow.com/questions/tagged/microsoft-graph). 

Si el problema está relacionado con el ejemplo de código proporcionado por el inicio rápido, también puede presentar un problema en el repositorio de ejemplo GitHub. Puede encontrar el repositorio siguiendo el vínculo **Darme solo el código de ejemplo** en el paso 2 para cada inicio rápido.
