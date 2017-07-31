# <a name="get-started-with-microsoft-graph-in-an-aspnet-46-mvc-app"></a>Introducción a Microsoft Graph en una aplicación de ASP.NET 4.6 MVC

En este artículo, se describen las tareas necesarias para obtener un token de acceso desde el punto de conexión v2.0 de Azure AD y llamar a Microsoft Graph. Le muestra los pasos para la compilación del [Ejemplo Connect de Microsoft Graph para ASP.NET 4.6](https://github.com/microsoftgraph/aspnet-connect-sample) y describe los conceptos principales que implementará para usar Microsoft Graph.

En la imagen siguiente, se muestra la aplicación que va a crear. 

![La aplicación web con los botones "Obtener la dirección de correo electrónico" y "Enviar correo electrónico"](images/aspnet-connect-sample.png "La aplicación web con los botones "Obtener la dirección de correo electrónico" y "Enviar correo electrónico"")

El [punto de conexión v2.0 de Azure AD](https://azure.microsoft.com/en-us/documentation/articles/active-directory-appmodel-v2-overview) permite a los usuarios iniciar sesión con una cuenta Microsoft (MSA) o con una cuenta profesional o educativa. La aplicación usa el [middleware de OWIN de OpenID Connect ASP.Net](https://www.nuget.org/packages/Microsoft.Owin.Security.OpenIdConnect/) y la [Biblioteca de autenticación de Microsoft (MSAL) para .NET](https://www.nuget.org/packages/Microsoft.Identity.Client) para el inicio de sesión y la administración de tokens.

**¿No desea compilar una aplicación?** Use el [inicio rápido de Microsoft Graph](https://developer.microsoft.com/en-us/graph/quick-start) para ponerlo todo en funcionamiento de manera rápida. Tenga en cuenta también que tenemos una [versión de REST de esta muestra](https://github.com/microsoftgraph/aspnet-connect-rest-sample).

## <a name="prerequisites"></a>Requisitos previos

Para comenzar, necesitará: 

- Una [cuenta Microsoft](https://www.outlook.com/) o una [cuenta profesional o educativa](http://dev.office.com/devprogram)
- Visual Studio 2015 
- [Ejemplo de Connect de Microsoft Graph para ASP.NET 4.6](https://github.com/microsoftgraph/aspnet-connect-sample). Usará la carpeta **starter-project** en los archivos de ejemplo.


## <a name="register-the-application"></a>Registrar la aplicación

En este paso, registrará una aplicación en el Portal de registro de aplicaciones de Microsoft. Esta acción generará el identificador de la aplicación y la contraseña que usará para configurar la aplicación en Visual Studio.

1. Inicie sesión en el [Portal de registro de aplicaciones de Microsoft](https://apps.dev.microsoft.com/) mediante su cuenta personal, profesional o educativa.

2. Seleccione **Agregar una aplicación**.

3. Escriba un nombre para la aplicación y seleccione **Crear aplicación**. 
    
    Se muestra la página de registro, indicando las propiedades de la aplicación.

4. Copie el identificador de la aplicación. Se trata del identificador único para su aplicación. 

5. En **Secretos de aplicación**, seleccione **Generar nueva contraseña**. Copie la contraseña del cuadro de diálogo **Nueva contraseña generada**.

    Deberá usar el Id. y el secreto de aplicación para configurar la aplicación. 

6. En **Plataformas**, elija **Agregar plataforma** > **Web**.

7. Asegúrese de que la casilla **Permitir flujo implícito** esté seleccionada y escriba *http://localhost:55065/* como URI de redireccionamiento. 

    La opción **Permitir flujo implícito**habilita el flujo híbrido de OpenID Connect. Durante la autenticación, esto permite que la aplicación reciba tanto la información de inicio de sesión (el **id_token**) como los artefactos (en este caso, un código de autorización) que la aplicación usa para obtener un token de acceso.

8. Elija **Guardar**.

### <a name="configure-the-project"></a>Configurar el proyecto

1. Abra el archivo de la solución para el proyecto inicial en Visual Studio.

2. Abra el archivo Web.config del proyecto.

3. Busque las claves de configuración de la aplicación en el elemento **appSettings**. Reemplace los valores de los marcadores de posición ENTER_YOUR_CLIENT_ID y ENTER_YOUR_SECRET por los valores que acaba de copiar.

El URI de redireccionamiento es la URL del proyecto que ha registrado. Los [ámbitos de permisos](https://developer.microsoft.com/en-us/graph/docs/concepts/permission_scopes) solicitados permiten a la aplicación obtener la información del perfil de usuario y enviar un correo electrónico.

## <a name="call-microsoft-graph"></a>Llamar a Microsoft Graph

En este paso deberá centrarse en las clases **SDKHelper**, **GraphService** y **HomeController**. 

 - **SDKHelper** inicializa una instancia de **GraphServiceClient** desde la biblioteca antes de cada llamada a Microsoft Graph. Este es el momento en el que el token de acceso se agrega a la solicitud. 
 - **GraphService** compila las solicitudes HTTP y las envía a Microsoft Graph mediante la biblioteca y procesa las respuestas.
 - **HomeController** contiene las acciones que inician las llamadas a la biblioteca en respuesta a los eventos de interfaz de usuario.

El proyecto inicial ya declara una dependencia para el paquete de NuGet de la Biblioteca cliente .NET de Microsoft Graph:  *Microsoft.Graph*.

1. Haga clic con el botón derecho en la carpeta **Helpers** y elija **Agregar** > **Clase**. 

1. Asigne a la nueva clase el nombre *SDKHelper* y elija **Agregar**.

1. Reemplace el contenido por el siguiente código.

        using System.Net.Http.Headers;
        using Microsoft.Graph;

        namespace Microsoft_Graph_SDK_ASPNET_Connect.Helpers
        {
            public class SDKHelper
            {   
                private static GraphServiceClient graphClient = null;

                // Get an authenticated Microsoft Graph Service client.
                public static GraphServiceClient GetAuthenticatedClient()
                {
                    GraphServiceClient graphClient = new GraphServiceClient(
                        new DelegateAuthenticationProvider(
                            async (requestMessage) =>
                            {
                                string accessToken = await SampleAuthProvider.Instance.GetUserAccessTokenAsync();

                                // Append the access token to the request.
                                requestMessage.Headers.Authorization = new AuthenticationHeaderValue("bearer", accessToken);
                            }));
                    return graphClient;
                }

                public static void SignOutClient()
                {
                    graphClient = null;
                }
            }
        }

  Fíjese en la llamada a **SampleAuthProvider** para obtener el token cuando se inicialice el cliente.

1. En la carpeta **Modelos** abra el archivo GraphService.cs. El servicio usa la biblioteca para interactuar con Microsoft Graph.

1. Agregue la siguiente instrucción **Using**.

        using Microsoft.Graph;

1. Reemplace *// GetMyEmailAddress* por el siguiente método. Esta acción obtiene la dirección de correo electrónico del usuario actual. 

        // Get the current user's email address from their profile.
        public async Task<string> GetMyEmailAddress(GraphServiceClient graphClient)
        {

            // Get the current user. 
            // The app only needs the user's email address, so select the mail and userPrincipalName properties.
            // If the mail property isn't defined, userPrincipalName should map to the email for all account types. 
            User me = await graphClient.Me.Request().Select("mail,userPrincipalName").GetAsync();
            return me.Mail ?? me.UserPrincipalName;
        }

  Fíjese en el segmento **Select**, que solo solicita que se devuelvan los elementos **mail** y **userPrinicipalName**. Puede usar los segmentos **Select** y **Filter** para reducir el tamaño de la carga de datos de respuesta.

1. Reemplace *// SendEmail* por los siguientes métodos para crear y enviar el correo electrónico.

        // Send an email message from the current user.
        public async Task SendEmail(GraphServiceClient graphClient, Message message)
        {
            await graphClient.Me.SendMail(message, true).Request().PostAsync();
        }

        public async Task<Message> BuildEmailMessage(GraphServiceClient graphClient, string recipients, string subject)
        {

            // Get current user photo
            Stream photoStream = await GetCurrentUserPhotoStreamAsync(graphClient);


            // If the user doesn't have a photo, or if the user account is MSA, we use a default photo

            if ( photoStream == null)
            {
                photoStream = System.IO.File.OpenRead(System.Web.Hosting.HostingEnvironment.MapPath("/Content/test.jpg"));
            }

            MemoryStream photoStreamMS = new MemoryStream();
            // Copy stream to MemoryStream object so that it can be converted to byte array.
            photoStream.CopyTo(photoStreamMS);

            DriveItem photoFile = await UploadFileToOneDrive(graphClient, photoStreamMS.ToArray());

            MessageAttachmentsCollectionPage attachments = new MessageAttachmentsCollectionPage();
            attachments.Add(new FileAttachment
            {
                ODataType = "#microsoft.graph.fileAttachment",
                ContentBytes = photoStreamMS.ToArray(),
                ContentType = "image/png",
                Name = "me.png"
            });

            Permission sharingLink = await GetSharingLinkAsync(graphClient, photoFile.Id);

            // Add the sharing link to the email body.
            string bodyContent = string.Format(Resource.Graph_SendMail_Body_Content, sharingLink.Link.WebUrl);

            // Prepare the recipient list.
            string[] splitter = { ";" };
            string[] splitRecipientsString = recipients.Split(splitter, StringSplitOptions.RemoveEmptyEntries);
            List<Recipient> recipientList = new List<Recipient>();
            foreach (string recipient in splitRecipientsString)
            {
                recipientList.Add(new Recipient
                {
                    EmailAddress = new EmailAddress
                    {
                        Address = recipient.Trim()
                    }
                });
            }

            // Build the email message.
            Message email = new Message
            {
                Body = new ItemBody
                {
                    Content = bodyContent,
                    ContentType = BodyType.Html,
                },
                Subject = subject,
                ToRecipients = recipientList,
                Attachments = attachments
            };
            return email;
        }

        // Gets the stream content of the signed-in user's photo. 
        // This snippet doesn't work with consumer accounts.
        public async Task<Stream> GetCurrentUserPhotoStreamAsync(GraphServiceClient graphClient)
        {
            Stream currentUserPhotoStream = null;

            try
            {
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
        public async Task<DriveItem> UploadFileToOneDrive(GraphServiceClient graphClient, byte[] file)
        {
            DriveItem uploadedFile = null;

            try
            {
                MemoryStream fileStream = new MemoryStream(file);
                uploadedFile = await graphClient.Me.Drive.Root.ItemWithPath("me.png").Content.Request().PutAsync<DriveItem>(fileStream);

            }


            catch (ServiceException)
            {
                return null;
            }

            return uploadedFile;
        }

        public static async Task<Permission> GetSharingLinkAsync(GraphServiceClient graphClient, string Id)
        {
            Permission permission = null;

            try
            {
                permission = await graphClient.Me.Drive.Items[Id].CreateLink("view").Request().PostAsync();
            }

            catch (ServiceException)
            {
                return null;
            }

            return permission;
        }

1. En la carpeta **Controllers**, abra el archivo HomeController.cs.

1. Agregue la siguiente instrucción **Using**.

        using Microsoft.Graph;
  
1. Reemplace *// Controller actions* por las siguientes acciones.

        [Authorize]
        // Get the current user's email address from their profile.
        public async Task<ActionResult> GetMyEmailAddress()
        {
            try
            {

                // Initialize the GraphServiceClient.
                GraphServiceClient graphClient = SDKHelper.GetAuthenticatedClient();

                // Get the current user's email address. 
                ViewBag.Email = await graphService.GetMyEmailAddress(graphClient);
                return View("Graph");
            }
            catch (ServiceException se)
            {
                if (se.Error.Message == Resource.Error_AuthChallengeNeeded) return new EmptyResult();
                return RedirectToAction("Index", "Error", new { message = Resource.Error_Message + Request.RawUrl + ": " + se.Error.Message });
            }
        }

        [Authorize]
        // Send mail on behalf of the current user.
        public async Task<ActionResult> SendEmail()
        {
            if (string.IsNullOrEmpty(Request.Form["email-address"]))
            {
                ViewBag.Message = Resource.Graph_SendMail_Message_GetEmailFirst;
                return View("Graph");
            }

            try
            {

                // Initialize the GraphServiceClient.
                GraphServiceClient graphClient = SDKHelper.GetAuthenticatedClient();

                // Build the email message.
                Message message = await graphService.BuildEmailMessage(graphClient, Request.Form["recipients"], Request.Form["subject"]);

                // Send the email.
                await graphService.SendEmail(graphClient, message);

                // Reset the current user's email address and the status to display when the page reloads.
                ViewBag.Email = Request.Form["email-address"];
                ViewBag.Message = Resource.Graph_SendMail_Success_Result;
                return View("Graph");
            }
            catch (ServiceException se)
            {
                if (se.Error.Code == Resource.Error_AuthChallengeNeeded) return new EmptyResult();
                return RedirectToAction("Index", "Error", new { message = Resource.Error_Message + Request.RawUrl + ": " + se.Error.Message });
            }
        }

Ahora ya puede [ejecutar la aplicación](#run-the-app).

## <a name="run-the-app"></a>Ejecutar la aplicación
1. Pulse F5 para compilar y ejecutar la aplicación. 

2. Inicie sesión con su cuenta personal, profesional o educativa y conceda los permisos solicitados.

3. Seleccione el botón **Obtener la dirección de correo electrónico**. Cuando finaliza la operación, la dirección de correo electrónico del usuario con sesión iniciada se muestra en la página.

4. De forma opcional, modifique la lista de destinatarios y el asunto del correo electrónico y, después, seleccione el botón **Enviar correo electrónico**. Cuando se envía el correo, se muestra un mensaje de Operación correcta debajo del botón.


## <a name="next-steps"></a>Pasos siguientes
- Pruebe la API de REST mediante el [Probador de Graph](https://graph.microsoft.io/graph-explorer).
- Busque ejemplos de operaciones comunes en [Fragmentos de código de ejemplo para ASP.NET 4.6](https://github.com/microsoftgraph/aspnet-snippets-sample) o explore nuestros otros [ejemplos para ASP.NET](http://aka.ms/aspnetgraphsamples) en GitHub.

## <a name="see-also"></a>Recursos adicionales
- [Biblioteca cliente .NET de Microsoft Graph](https://github.com/microsoftgraph/msgraph-sdk-dotnet)
- [Aplicación web para el escenario de autenticación de la API web](https://azure.microsoft.com/en-us/documentation/articles/active-directory-authentication-scenarios/#web-application-to-web-api)
- [Integrar la identidad de Microsoft y Microsoft Graph en una aplicación web usando OpenID Connect](https://azure.microsoft.com/en-us/documentation/samples/active-directory-dotnet-webapp-openidconnect-v2/)
- [Protocolos de Azure AD v2.0](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-protocols/)
- [Tokens de Azure AD v2.0](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-tokens/)
