# <a name="ios-samples-for-the-microsoft-graph-api"></a>Ejemplos de iOS para la API de Microsoft Graph
Este artículo presenta dos ejemplos de iOS que autentican a un usuario en Office 365 o en cuentas de servicio administradas (MSA) como usuarios consumidores de Outlook. Ambos ejemplos envían un correo electrónico a través del servicio de Outlook, pero uno de los ejemplos extiende la característica y obtiene la foto de perfil del usuario y la envía en el cuerpo del correo electrónico.

## <a name="ios-objective-c-connect-rest-sample"></a>Ejemplo de Connect REST con Objective C para iOS
En este ejemplo, se usa una biblioteca HTTPS estándar de iOS para realizar llamadas REST a Microsoft Graph. Usa la [biblioteca de autenticación de Microsoft (MSAL)](https://github.com/AzureAD/microsoft-authentication-library-for-objc/blob/dev/README.md) para autenticar a un usuario. La biblioteca de MSAL permite que su aplicación autentique a un usuario de Office 365 o de una cuenta de MSA. Aunque no podrá autenticar a un usuario de una instancia de Azure Active Directory local.

Puede enviar un correo electrónico con este ejemplo, pero no recupera la fotografía del usuario autenticado ni la inserta en el correo electrónico.

- [Introducción a Microsoft Graph en una aplicación de Objective C de iOS](ios_objectivec.md)

## <a name="ios-swift-connect-rest-sample"></a>Ejemplo de REST de conexión con Swift para iOS
En este ejemplo, se usa la biblioteca HTTP de Foundation y [PromiseKit](https://github.com/mxcl/PromiseKit/blob/master/README.md) para obtener acceso al punto de conexión de Microsoft Graph con operaciones de REST y con el modelo asincrónico de **Promesas**. Usa la [biblioteca de autenticación de Microsoft (MSAL)](https://github.com/AzureAD/microsoft-authentication-library-for-objc/blob/dev/README.md) para autenticar a un usuario. Esta biblioteca permite a su aplicación autenticar a un usuario de Office 365 o a un usuario de MSA.

En el ejemplo, se muestra cómo obtener acceso al perfil de Azure del usuario con Graph. También aprenderá a obtener la foto de perfil del usuario, cargarla al almacenamiento de OneDrive del usuario e insertarla en el cuerpo de un mensaje de correo electrónico de Outlook.

- [Introducción a Microsoft Graph en una aplicación de iOS](ios_swift.md)
