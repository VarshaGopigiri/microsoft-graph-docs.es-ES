# <a name="get-started-with-microsoft-graph-in-a-xamarin-forms-app"></a>Introducción a Microsoft Graph en una aplicación de Xamarin Forms

> **¿Desea compilar aplicaciones para clientes empresariales?** Es posible que la aplicación no funcione si su cliente empresarial activa características de seguridad de movilidad empresarial como el <a href="https://azure.microsoft.com/documentation/articles/active-directory-conditional-access-device-policies/" target="_newtab">acceso condicional al dispositivo</a>. En casos así, es posible que no tenga constancia de esta activación y que sus clientes obtengan errores. 

En este artículo se describen las tareas necesarias para obtener un token de acceso desde el punto de conexión de [Azure AD v2.0](https://developer.microsoft.com/graph/docs/concepts/converged_auth) y llamar a Microsoft Graph. Le guiará por el código del [Ejemplo Connect de Microsoft Graph para Xamarin Forms](https://github.com/microsoftgraph/xamarin-csharp-connect-sample) para explicar los conceptos principales que se deben implementar en una aplicación que use Microsoft Graph. El artículo también describe cómo obtener acceso a Microsoft Graph mediante la [Biblioteca cliente de Microsoft Graph](http://www.nuget.org/packages/Microsoft.Graph/).

Esta es la aplicación que va a crear.

| UWP | Android | iOS |
| --- | ------- | ----|
| <img src="images/UWP.png" alt="Connect sample on UWP" width="100%" /> | <img src="images/Droid.png" alt="Connect sample on Android" width="100%" /> | <img src="images/iOS.png" alt="Connect sample on iOS" width="100%" /> |

**¿No desea compilar una aplicación?** Use el [inicio rápido de Microsoft Graph](https://developer.microsoft.com/graph/quick-start) para ponerlo todo en funcionamiento de manera rápida o descargue el [Ejemplo Connect de Microsoft Graph para Xamarin Forms](https://github.com/microsoftgraph/xamarin-csharp-connect-sample) en el que se basa este artículo.

## <a name="prerequisites"></a>Requisitos previos

Para comenzar, necesitará: 

- Una [cuenta Microsoft](https://www.outlook.com/) o una [cuenta profesional o educativa](https://docs.microsoft.com/es-ES/office/developer-program/office-365-developer-program-faq#account-types)
- Visual Studio 2015 
- [Xamarin para Visual Studio](https://www.xamarin.com/visual-studio)
- Windows 10 ([modo de desarrollo habilitado](https://msdn.microsoft.com/library/windows/apps/xaml/dn706236.aspx))
- [Proyecto inicial de conexión de Microsoft Graph para Xamarin Forms](https://github.com/microsoftgraph/xamarin-csharp-connect-sample/tree/master/starter). Esta plantilla contiene varias clases a las que agregará código. También contiene vistas completas y cadenas de recursos. Para obtener este proyecto, clone o descargue el [Ejemplo Connect de Microsoft Graph para Xamarin Forms](https://github.com/microsoftgraph/xamarin-csharp-connect-sample) y abra la solución **XamarinConnect** de la carpeta **starter**. 

Si desea ejecutar el proyecto de iOS en este ejemplo, necesitará lo siguiente:

- El SDK de iOS más reciente
- La versión de Xcode más reciente
- Mac OS X Sierra (10.12) y versiones posteriores 
- [Xamarin.iOS](https://docs.microsoft.com/visualstudio/mac/installation)
- Un [agente Xamarin Mac conectado a Visual Studio](https://developer.xamarin.com/guides/ios/getting_started/installation/windows/connecting-to-mac/)


## <a name="register-the-app"></a>Registrar la aplicación
 
1. Inicie sesión en el [Portal de registro de aplicaciones](https://apps.dev.microsoft.com/) mediante su cuenta personal, profesional o educativa.
2. Seleccione **Agregar una aplicación**.
3. Escriba un nombre para la aplicación y seleccione **Crear**.
    
    Se muestra la página de registro, indicando las propiedades de la aplicación.
 
4. En **Plataformas**, seleccione **Agregar plataforma**.
5. Seleccione **Aplicación nativa**.
6. Copie el valor del identificador de la aplicación y el valor personalizado redirección URI (en el encabezado **Aplicación nativa** encabezado) que se crea automáticamente cuando agrega la plataforma de **Aplicación nativa**. Este identificador URI debe contener el valor de identificador de la aplicación y estar en este formulario: `msal[Application Id]://auth` Deberá escribir estos valores en la aplicación de ejemplo.

    El id. de la aplicación es un identificador único para su aplicación. 

7. Seleccione **Guardar**.

## <a name="configure-the-project"></a>Configurar el proyecto

1. Abra el archivo de la solución para el proyecto inicial en Visual Studio.
2. Abra el archivo **App.cs** del proyecto **XamarinConnect (Portable)** y localice el campo `ClientId`. Reemplace el marcador de posición identificador de la aplicación por el identificador de la aplicación que haya registrado.

    ```
    public static string ClientID = "ENTER_YOUR_CLIENT_ID";
    public static string RedirectUri = "msal" + ClientID + "://auth";
    public static string[] Scopes = { "User.Read", "Mail.Send", "Files.ReadWrite" };
    ```
    El valor `Scopes` almacena los ámbitos de permisos de Microsoft Graph que la aplicación deberá solicitar cuando el usuario se autentique. Tenga en cuenta que el constructor de clases `App` usa el valor ClientID para crear una instancia de la clase `PublicClientApplication` de MSAL. Más adelante, usará esta clase para autenticar el usuario.
    
    ```
    IdentityClientApp = new PublicClientApplication(ClientID);
    ```

3. Abra el archivo UserDetailsClient.iOS\info.plist en un editor de texto. Lamentablemente no puede editar este archivo en Visual Studio. Busque el elemento `<string>msalENTER_YOUR_CLIENT_ID</string>` en `CFBundleURLSchemes` clave.

4. Reemplace `ENTER_YOUR_CLIENT_ID` por el valor del id. de aplicación que ha obtenido al registrar la aplicación. Asegúrese de conservar `msal` antes del identificador de aplicación. El valor de cadena resultante debe parecerse al siguiente: `<string>msal[application id]</string>`.

5. Abra el archivo UserDetailsClient.Droid\Properties\AndroidManifest.xml. Busque este elemento: `<data android:scheme="msalENTER_YOUR_CLIENT_ID" android:host="auth" />`.

6. Reemplace `ENTER_YOUR_CLIENT_ID` por el valor del id. de aplicación que ha obtenido al registrar la aplicación. Asegúrese de conservar `msal` antes del identificador de aplicación. El valor de cadena resultante debe parecerse al siguiente: `<data android:scheme="msal[application id]" android:host="auth" />`.

## <a name="send-an-email-with-microsoft-graph"></a>Enviar un correo electrónico con Microsoft Graph

Abra el archivo MailHelper.cs en su proyecto inicial. Este archivo contiene código que crea y envía correos electrónicos. Consiste en un único método (``ComposeAndSendMailAsync``) que crea y envía una solicitud POST al punto de conexión **https://graph.microsoft.com/v1.0/me/microsoft.graph.SendMail**. 

El método ``ComposeAndSendMailAsync`` toma tres valores de cadena (``subject``, ``bodyContent`` y ``recipients``) que se le pasan mediante el archivo MainPage.xaml.cs. Las cadenas ``subject`` y ``bodyContent`` se almacenan, junto con todas las demás cadenas de la interfaz de usuario, en el archivo AppResources.resx. La cadena ``recipients`` proviene del cuadro de dirección en la interfaz de la aplicación. 

**Usar declaraciones**

Asegúrese de que tiene estas declaraciones al principio del archivo:

```
using System;
using System.Collections.Generic;
using System.Linq;
using System.Reflection;
using System.Threading.Tasks;
using Microsoft.Graph;
```

La primera tarea dentro del método ``ComposeAndSendMailAsync`` consiste en obtener la fotografía del usuario actual de Microsoft Graph. Esta línea llama al método sin stub `GetCurrentUserPhotoStreamAsync`:

```
            // Get current user photo
            Stream photoStream = await GetCurrentUserPhotoStreamAsync();
```

El método `GetCurrentUserPhotoStreamAsync` completo tiene un aspecto similar a este:

```
        // Gets the stream content of the signed-in user's photo. 
        // This snippet doesn't work with consumer accounts.
        public async Task<Stream> GetCurrentUserPhotoStreamAsync()
        {
            Stream currentUserPhotoStream = null;

            try
            {
                var graphClient = AuthenticationHelper.GetAuthenticatedClient();
                currentUserPhotoStream = await graphClient.Me.Photo.Content.Request().GetAsync();

            }

            // If the user account is MSA (not work or school), the service will throw an exception.
            catch (ServiceException)
            {
                return null;
            }

            return currentUserPhotoStream;

        }
```

Si el usuario no tiene ninguna foto, esta lógica obtiene otro archivo de imagen que se haya incluido en el proyecto:

```
            // If the user doesn't have a photo, or if the user account is MSA, we use a default photo

            if (photoStream == null)
            {
                var assembly = typeof(MailHelper).GetTypeInfo().Assembly;
                photoStream = assembly.GetManifestResourceStream("XamarinConnect.test.jpg");
            }
```

Ahora que tenemos una secuencia de imagen, podemos cargar el archivo en OneDrive llamando al método sin stub `UploadFileToOneDriveAsync`:

```
            MemoryStream photoStreamMS = new MemoryStream();
            // Copy stream to MemoryStream object so that it can be converted to byte array.
            photoStream.CopyTo(photoStreamMS);

            DriveItem photoFile = await UploadFileToOneDriveAsync(photoStreamMS.ToArray());
```

El método `UploadFileToOneDriveAsync` completo tiene un aspecto similar a este:

```
        // Uploads the specified file to the user's root OneDrive directory.
        public async Task<DriveItem> UploadFileToOneDriveAsync(byte[] file)
        {
            DriveItem uploadedFile = null;

            try
            {
                var graphClient = AuthenticationHelper.GetAuthenticatedClient();
                MemoryStream fileStream = new MemoryStream(file);
                uploadedFile = await graphClient.Me.Drive.Root.ItemWithPath("me.png").Content.Request().PutAsync<DriveItem>(fileStream);

            }


            catch (ServiceException)
            {
                return null;
            }

            return uploadedFile;
        }
```

También podemos usar esta secuencia para crear un objeto `MessageAttachmentsCollectionPage` que se pueda pasar junto al mensaje:

```
            MessageAttachmentsCollectionPage attachments = new MessageAttachmentsCollectionPage();
            attachments.Add(new FileAttachment
            {
                ODataType = "#microsoft.graph.fileAttachment",
                ContentBytes = photoStreamMS.ToArray(),
                ContentType = "image/png",
                Name = "me.png"
            });
```

Podemos obtener un vínculo para compartir para el archivo recién cargado en OneDrive llamando al método sin stub `GetSharingLinkAsync`. La cadena `bodyContent` contiene un marcador de posición para el vínculo para compartir:

```
            // Get the sharing link and insert it into the message body.
            Permission sharingLink = await GetSharingLinkAsync(photoFile.Id);
            string bodyContentWithSharingLink = String.Format(bodyContent, sharingLink.Link.WebUrl);
```

El método `GetSharingLinkAsync` completo tiene un aspecto similar a este:

```
        public static async Task<Permission> GetSharingLinkAsync(string Id)
        {
            Permission permission = null;

            try
            {
                var graphClient = AuthenticationHelper.GetAuthenticatedClient();
                permission = await graphClient.Me.Drive.Items[Id].CreateLink("view").Request().PostAsync();
            }

            catch (ServiceException)
            {
                return null;
            }

            return permission;
        }
```

Ya que el usuario puede pasar potencialmente más de una dirección, la siguiente tarea es dividir la cadena ``recipients`` en un conjunto de objetos `EmailAddress` que pueden usarse a continuación para crear la lista de objetos `Recipients` que se pasará en el cuerpo POST de la solicitud:

```
            // Prepare the recipient list
            string[] splitter = { ";" };
            var splitRecipientsString = recipients.Split(splitter, StringSplitOptions.RemoveEmptyEntries);
            List<Recipient> recipientList = new List<Recipient>();

            foreach (string recipient in splitRecipientsString)
            {
                recipientList.Add(new Recipient { EmailAddress = new EmailAddress { Address = recipient.Trim() } });
            }
```

La última tarea consiste en crear un objeto `Message` y enviarlo al punto de conexión **me/microsoft.graph.SendMail** a través del `GraphServiceClient`. Ya que la cadena ``bodyContent`` es un documento HTML, la solicitud establece el valor **ContentType** a HTML.

```
            try
            {
                var graphClient = AuthenticationHelper.GetAuthenticatedClient();

                var email = new Message
                {
                    Body = new ItemBody
                    {
                        Content = bodyContentWithSharingLink,
                        ContentType = BodyType.Html,
                    },
                    Subject = subject,
                    ToRecipients = recipientList,
                    Attachments = attachments
                };

                try
                {
                    await graphClient.Me.SendMail(email, true).Request().PostAsync();
                }
                catch (ServiceException exception)
                {
                    throw new Exception("We could not send the message: " + exception.Error == null ? "No error message returned." : exception.Error.Message);
                }


            }

            catch (Exception e)
            {
                throw new Exception("We could not send the message: " + e.Message);
            }
```

La clase completa tendrá este aspecto:

```
    public class MailHelper
    {
        /// <summary>
        /// Compose and send a new email.
        /// </summary>
        /// <param name="subject">The subject line of the email.</param>
        /// <param name="bodyContent">The body of the email.</param>
        /// <param name="recipients">A semicolon-separated list of email addresses.</param>
        /// <returns></returns>
        public async Task ComposeAndSendMailAsync(string subject,
                                                            string bodyContent,
                                                            string recipients)
        {

            // Get current user photo
            Stream photoStream = await GetCurrentUserPhotoStreamAsync();


            // If the user doesn't have a photo, or if the user account is MSA, we use a default photo

            if (photoStream == null)
            {
                var assembly = typeof(MailHelper).GetTypeInfo().Assembly;
                photoStream = assembly.GetManifestResourceStream("XamarinConnect.test.jpg");
            }

            MemoryStream photoStreamMS = new MemoryStream();
            // Copy stream to MemoryStream object so that it can be converted to byte array.
            photoStream.CopyTo(photoStreamMS);

            DriveItem photoFile = await UploadFileToOneDriveAsync(photoStreamMS.ToArray());

            MessageAttachmentsCollectionPage attachments = new MessageAttachmentsCollectionPage();
            attachments.Add(new FileAttachment
            {
                ODataType = "#microsoft.graph.fileAttachment",
                ContentBytes = photoStreamMS.ToArray(),
                ContentType = "image/png",
                Name = "me.png"
            });

            // Get the sharing link and insert it into the message body.
            Permission sharingLink = await GetSharingLinkAsync(photoFile.Id);
            string bodyContentWithSharingLink = String.Format(bodyContent, sharingLink.Link.WebUrl);


            // Prepare the recipient list
            string[] splitter = { ";" };
            var splitRecipientsString = recipients.Split(splitter, StringSplitOptions.RemoveEmptyEntries);
            List<Recipient> recipientList = new List<Recipient>();

            foreach (string recipient in splitRecipientsString)
            {
                recipientList.Add(new Recipient { EmailAddress = new EmailAddress { Address = recipient.Trim() } });
            }

            try
            {
                var graphClient = AuthenticationHelper.GetAuthenticatedClient();

                var email = new Message
                {
                    Body = new ItemBody
                    {
                        Content = bodyContentWithSharingLink,
                        ContentType = BodyType.Html,
                    },
                    Subject = subject,
                    ToRecipients = recipientList,
                    Attachments = attachments
                };

                try
                {
                    await graphClient.Me.SendMail(email, true).Request().PostAsync();
                }
                catch (ServiceException exception)
                {
                    throw new Exception("We could not send the message: " + exception.Error == null ? "No error message returned." : exception.Error.Message);
                }


            }

            catch (Exception e)
            {
                throw new Exception("We could not send the message: " + e.Message);
            }
        }

        // Gets the stream content of the signed-in user's photo. 
        // This snippet doesn't work with consumer accounts.
        public async Task<Stream> GetCurrentUserPhotoStreamAsync()
        {
            Stream currentUserPhotoStream = null;

            try
            {
                var graphClient = AuthenticationHelper.GetAuthenticatedClient();
                currentUserPhotoStream = await graphClient.Me.Photo.Content.Request().GetAsync();

            }

            // If the user account is MSA (not work or school), the service will throw an exception.
            catch (ServiceException)
            {
                return null;
            }

            return currentUserPhotoStream;

        }

        // Uploads the specified file to the user's root OneDrive directory.
        public async Task<DriveItem> UploadFileToOneDriveAsync(byte[] file)
        {
            DriveItem uploadedFile = null;

            try
            {
                var graphClient = AuthenticationHelper.GetAuthenticatedClient();
                MemoryStream fileStream = new MemoryStream(file);
                uploadedFile = await graphClient.Me.Drive.Root.ItemWithPath("me.png").Content.Request().PutAsync<DriveItem>(fileStream);

            }


            catch (ServiceException)
            {
                return null;
            }

            return uploadedFile;
        }

        public static async Task<Permission> GetSharingLinkAsync(string Id)
        {
            Permission permission = null;

            try
            {
                var graphClient = AuthenticationHelper.GetAuthenticatedClient();
                permission = await graphClient.Me.Drive.Items[Id].CreateLink("view").Request().PostAsync();
            }

            catch (ServiceException)
            {
                return null;
            }

            return permission;
        }


    }
``` 

Ya ha llevado a cabo los tres pasos requeridos para interactuar con Microsoft Graph: el registro de la aplicación, la autenticación del usuario y la creación de una solicitud. 

## <a name="run-the-app"></a>Ejecutar la aplicación
1. Seleccione el proyecto que desee ejecutar. Si selecciona la opción de plataforma universal de Windows, puede ejecutar el ejemplo en el equipo local. Si desea ejecutar el proyecto iOS, necesitará conectarse a un [Mac que tenga las herramientas Xamarin](https://developer.xamarin.com/guides/ios/getting_started/installation/windows/connecting-to-mac/) instaladas. (También puede abrir esta solución en Xamarin Studio en un Mac y ejecutar el ejemplo directamente desde allí). Puede usar el [Emulador de Visual Studio para Android](https://www.visualstudio.com/features/msft-android-emulator-vs.aspx) si desea ejecutar el proyecto de Android. 

    ![](images/SelectProject.png "Seleccionar un proyecto en Visual Studio")

2. Pulse F5 para compilar y depurar. Ejecute la solución e inicie sesión con su cuenta personal, profesional o educativa.
    > **Nota** Es posible que tenga que abrir el administrador de configuración de compilación para asegurarse de que los pasos de compilación e implementación están seleccionados para el proyecto UWP. 

3. Inicie sesión con su cuenta personal, profesional o educativa y conceda los permisos solicitados.

4. Elija el botón **Enviar correo**. Cuando se envía el correo, se muestra un mensaje de Operación correcta. Este correo incluye la foto como un archivo adjunto y proporciona un vínculo para compartir al archivo cargado en OneDrive.

## <a name="next-steps"></a>Siguientes pasos
- Pruebe la API de REST mediante el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).
- Busque ejemplos de operaciones comunes en la [Biblioteca de fragmentos de código del SDK de Microsoft Graph para Xamarin.Forms](https://github.com/microsoftgraph/xamarin-csharp-snippets-sample) o explore el resto de nuestros [ejemplos de Xamarin](https://github.com/microsoftgraph?utf8=%E2%9C%93&query=xamarin) en GitHub.

## <a name="see-also"></a>Recursos adicionales
- [Biblioteca cliente .NET de Microsoft Graph](https://github.com/microsoftgraph/msgraph-sdk-dotnet)
- [Protocolos de Azure AD v2.0](https://azure.microsoft.com/documentation/articles/active-directory-v2-protocols/)
- [Tokens de Azure AD v2.0](https://azure.microsoft.com/documentation/articles/active-directory-v2-tokens/)
