# <a name="ios-samples-for-the-microsoft-graph-api"></a>Ejemplos de iOS para la API de Microsoft Graph
Este artículo presenta dos ejemplos de iOS que autentican a un usuario en Office 365 o en cuentas de servicio administradas (MSA) como usuarios consumidores de Outlook. Ambos ejemplos envían un correo electrónico a través del servicio de Outlook, pero uno de los ejemplos extiende la característica y obtiene la foto de perfil del usuario y la envía en el cuerpo del correo electrónico.

## <a name="ios-objective-c-connect-rest-sample"></a>Ejemplo de Connect REST con Objective C para iOS
En este ejemplo se usa una biblioteca HTTPS estándar de iOS para realizar llamadas REST a Microsoft Graph. Usa la biblioteca de autenticación de Microsoft (MSAL) para autenticar a un usuario. La biblioteca MSAL permite que su aplicación autentique a un usuario de Office 365 o de una cuenta MSA. Aunque no podrá autenticar a un usuario de una instancia de Azure Active Directory local.

Puede enviar un correo electrónico con este ejemplo, pero no recupera la fotografía del usuario autenticado ni la inserta en el correo electrónico.

- [Introducción a Microsoft Graph en una aplicación de Objective C de iOS](ios_objectivec.md)

## <a name="ios-swift-sonnect-sample"></a>Ejemplo de iOS Swift Sonnect
En este ejemplo se usa la biblioteca de cliente de Microsoft Graph para que Objective C tenga acceso a los puntos de conexión de Microsoft Graph. La autenticación de usuarios está controlada por la biblioteca de terceros [NXOAuth2Client](https://github.com/nxtbgthng/OAuth2Client). Esta biblioteca permite autenticar a un usuario de una instancia de Azure Active Directory local en su aplicación, pero no puede autenticar a los usuarios de MSA.

El ejemplo muestra cómo tener acceso al perfil de Azure del usuario mediante Graph. También aprenderá a obtener la foto de perfil del usuario, cargarla al almacenamiento de OneDrive del usuario e insertarla en el cuerpo de un mensaje de correo electrónico de Outlook.

- [Introducción a Microsoft Graph en una aplicación de iOS](ios_swift.md)
