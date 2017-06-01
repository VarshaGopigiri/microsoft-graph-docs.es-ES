# <a name="get-started-with-microsoft-graph-in-a-universal-windows-10-app"></a>Introducción a Microsoft Graph en una aplicación de Windows 10 universal

> **¿Desea compilar aplicaciones para clientes empresariales?** Es posible que la aplicación no funcione si su cliente empresarial activa características de seguridad de movilidad empresarial como el <a href="https://azure.microsoft.com/en-us/documentation/articles/active-directory-conditional-access-device-policies/" target="_newtab">acceso condicional al dispositivo</a>. En casos así, es posible que no tenga constancia de esta activación y que sus clientes obtengan errores. 

> Para ser compatible con **todos los clientes empresariales** en **todos los escenarios de empresa**, tiene que usar el punto de conexión de AD de Azure y administrar las aplicaciones mediante el [Portal de administración de Azure](https://aka.ms/aadapplist). Para obtener más información, consulte [Decidir entre los puntos de conexión de Azure AD y Azure AD v2.0 ](../concepts/auth_overview.md#deciding-between-the-azure-ad-and-azure-ad-v20-endpoints).

En este artículo, se describen las tareas necesarias para obtener un token de acceso desde el [punto de conexión v2.0 de Azure AD](https://developer.microsoft.com/en-us/graph/docs/concepts/converged_auth) y llamar a Microsoft Graph. Le guiará por el código del [Ejemplo Connect de Microsoft Graph para UWP (biblioteca)](https://github.com/microsoftgraph/uwp-csharp-connect-sample) para explicar los conceptos principales que se deben implementar en una aplicación que use Microsoft Graph.

**¿No desea compilar una aplicación?** Use el [inicio rápido de Microsoft Graph](https://developer.microsoft.com/graph/quick-start) para ponerlo todo en funcionamiento de manera rápida o descargue el [Ejemplo Connect de Microsoft Graph para UWP (biblioteca)](https://github.com/microsoftgraph/uwp-csharp-connect-sample) en el que se basa este artículo. Tenga en cuenta también que tenemos una [versión de REST de esta muestra](https://github.com/microsoftgraph/uwp-csharp-connect-rest-sample).

## <a name="sample-user-interface"></a>Interfaz de usuario de ejemplo

El ejemplo contiene una interfaz de usuario muy sencilla, que consta de una barra de comandos superior, el **botón Conectar**, el botón **Enviar correo** y un cuadro de texto que se rellena automáticamente con la dirección de correo electrónico del usuario que ha iniciado sesión pero puede modificarse.

El botón **Enviar correo** está deshabilitado cuando el usuario no está conectado:

![Pantalla que muestra el botón Conectar habilitado y el botón Enviar correo deshabilitado](images/SignedOut.png)

En la barra de comandos superior, aparece un botón de desconexión cuando el usuario está conectado:

![Pantalla que muestra la dirección de correo electrónico del usuario conectado y el botón Enviar correo habilitado](images/SignedIn.png)

Todas las cadenas de la interfaz de usuario del ejemplo se almacenan en el archivo Resources.resw dentro de la carpeta Assets.

## <a name="prerequisites"></a>Requisitos previos

Para comenzar, necesitará: 

- Una [cuenta Microsoft](https://www.outlook.com/) o una [cuenta profesional o educativa](http://dev.office.com/devprogram)
- Visual Studio 2015 
- [Proyecto inicial de Microsoft Graph para UWP (biblioteca)](https://github.com/microsoftgraph/uwp-csharp-connect-sample/tree/master/starter). Ambas plantillas contienen clases a las que agregará código. También contienen cadenas de recursos. Para obtener este proyecto, clone o descargue el [Ejemplo Connect de Microsoft Graph UWP (biblioteca)](https://github.com/microsoftgraph/uwp-csharp-connect-sample) y abra la solución dentro de la carpeta **starter**.


## <a name="register-the-app"></a>Registrar la aplicación
 
1. Inicie sesión en el [Portal de registro de aplicaciones](https://apps.dev.microsoft.com/) mediante su cuenta personal, profesional o educativa.
2. Seleccione **Agregar una aplicación**.
3. Escriba un nombre para la aplicación y seleccione **Crear aplicación**.
    
    Se muestra la página de registro, indicando las propiedades de la aplicación.
 
4. En **Plataformas**, seleccione **Agregar plataforma**.
5. Seleccione **Aplicación nativa**.
6. Copie tanto el identificador de cliente (identificador de la aplicación) como los valores del URI de redireccionamiento al Portapapeles. Deberá escribir estos valores en la aplicación de ejemplo.

    El identificador de la aplicación es un identificador único para su aplicación. El URI de redireccionamiento es un URI único que proporciona Windows 10 para cada aplicación con el fin de garantizar que los mensajes enviados a ese URI solo se envían a esa aplicación. 

7. Seleccione **Guardar**.

## <a name="configure-the-project"></a>Configurar el proyecto

1. Abra el archivo de la solución para el proyecto inicial en Visual Studio.
2. Abra el archivo **App.xaml** del proyecto y busque el nodo `Application.Resources`. Reemplace los marcadores de posición identificador de la aplicación y URI de redireccionamiento por los valores correspondientes de la aplicación que haya registrado.


```xml
    <Application.Resources>
        <!-- Add your Client Id here. -->
        <x:String x:Key="ida:ClientID">ENTER_YOUR_CLIENT_ID</x:String>
        <!-- Add your Redirect URI here. -->
        <x:String x:Key="ida:ReturnUrl">ENTER_YOUR_REDIRECT_URI</x:String>
    </Application.Resources>
```

## <a name="install-the-microsoft-authentication-library-msal"></a>Instalar la Biblioteca de autenticación de Microsoft (MSAL)

La [Biblioteca de autenticación de Microsoft](https://www.nuget.org/packages/Microsoft.Identity.Client) contiene clases y métodos que facilitan la autenticación de los usuarios a través del punto de conexión v2.0 de Azure AD.

1. En el Explorador de soluciones, haga clic con el botón derecho en el nombre del proyecto y seleccione **Administrar paquetes de NuGet...**
2. Haga clic en Examinar y busque Microsoft.Identity.Client.
3. Seleccione la versión más reciente de la Biblioteca de autenticación de Microsoft y haga clic en **Instalar**.

## <a name="install-the-microsoft-graph-client-library"></a>Instalar la biblioteca cliente de Microsoft Graph

1. En el Explorador de soluciones, haga clic con el botón derecho en el nombre del proyecto y seleccione **Administrar paquetes de NuGet...**
2. Haga clic en Examinar y busque Microsoft.Graph.
3. Seleccione la versión más reciente de la Biblioteca cliente de Microsoft y haga clic en **Instalar**.

## <a name="install-the-newtonsoftjson-library"></a>Instalar la biblioteca Newtonsoft.JSON

1. En el Explorador de soluciones, haga clic con el botón derecho en el proyecto **XamarinConnect (Portable)** y seleccione **Administrar paquetes de NuGet...**
2. Haga clic en Examinar y busque NewtonSoft.JSON.
3. Seleccione la versión 9.0.1 de la biblioteca NewtonSoft.JSON y haga clic en **Instalar**.

## <a name="create-the-authenticationhelpercs-class"></a>Crear la clase AuthenticationHelper.cs

Abra el archivo AuthenticationHelper.cs en el proyecto inicial. El archivo contiene el código de autenticación completo, junto con la lógica adicional que almacena la información del usuario, y exige la autenticación solo cuando el usuario se ha desconectado de la aplicación. Esta clase contiene al menos dos métodos: `GetTokenForUserAsync` y `Signout`. Si usa la Biblioteca cliente de Microsoft Graph, necesitará agregar un tercer método: `GetAuthenticatedClient`.

El método ``GetTokenHelperAsync`` se ejecuta cuando el usuario se autentica y, posteriormente, cada vez que la aplicación llama a Microsoft Graph.

**Usar declaraciones**

***Versión de la biblioteca cliente***

Asegúrese de que el archivo contiene estas declaraciones:

```
using System;
using System.Diagnostics;
using System.Net.Http.Headers;
using System.Threading.Tasks;
using Microsoft.Graph;
using Microsoft.Identity.Client;
```

**Campos de clase**

Asegúrese de que tiene esos campos en la clase AuthenticationHelper:

```
// The Client ID is used by the application to uniquely identify itself to the Azure AD v2.0 endpoint.
static string clientId = App.Current.Resources["ida:ClientID"].ToString();
public static string[] Scopes = { "User.Read", "Mail.Send" };
public static PublicClientApplication IdentityClientApp = new PublicClientApplication(clientId);
public static string TokenForUser = null;
public static DateTimeOffset Expiration;
private static GraphServiceClient graphClient = null;
```

En el ejemplo, se almacena el `GraphServicesClient` en un campo de modo que solo deba crearlo una sola vez. Usa la clase `PublicClientApplication` de MSAL para autenticar el usuario. El campo `Scopes` almacena los ámbitos de permisos de Microsoft Graph que la aplicación deberá solicitar cuando el usuario se autentique. 


**GetTokenForUserAsync**

El método `GetTokenForUserAsync` usa los valores de configuración PublicClientApplicationClass y ClientId para obtener un token de acceso para el usuario. Si el usuario todavía no se ha autenticado, inicia la interfaz de usuario de autenticación.

```
        public static async Task<string> GetTokenForUserAsync()
        {
            AuthenticationResult authResult;
            try
            {
                authResult = await IdentityClientApp.AcquireTokenSilentAsync(Scopes);
                TokenForUser = authResult.Token;
            }

            catch (Exception)
            {
                if (TokenForUser == null || Expiration <= DateTimeOffset.UtcNow.AddMinutes(5))
                {
                    authResult = await IdentityClientApp.AcquireTokenAsync(Scopes);

                    TokenForUser = authResult.Token;
                    Expiration = authResult.ExpiresOn;
                }
            }

            return TokenForUser;
        }
```

**Cerrar sesión**

El método `Signout` cierra la sesión de todos los usuarios que la hayan iniciado a través de la `PublicClientApplication` (en este caso, solo hay un usuario) y anula el valor `TokenForUser`. También anulan el valor `GraphServicesClient`.

Esta es la versión de la biblioteca cliente del método `Signout`.

```
        public static void SignOut()
        {
            foreach (var user in IdentityClientApp.Users)
            {
                user.SignOut();
            }
            graphClient = null;
            TokenForUser = null;

        }
``` 

**GetAuthenticatedClient**

Por último, necesitará un método que cree un `GraphServicesClient`. Este método crea un cliente que usa el método `GetTokenForUserAsync` para cada llamada a Microsoft Graph que realiza a través del cliente.

```
        public static GraphServiceClient GetAuthenticatedClient()
        {
            if (graphClient == null)
            {
                // Create Microsoft Graph client.
                try
                {
                    graphClient = new GraphServiceClient(
                        "https://graph.microsoft.com/v1.0",
                        new DelegateAuthenticationProvider(
                            async (requestMessage) =>
                            {
                                var token = await GetTokenForUserAsync();
                                requestMessage.Headers.Authorization = new AuthenticationHeaderValue("bearer", token);
                            }));
                    return graphClient;
                }

                catch (Exception ex)
                {
                    Debug.WriteLine("Could not create a graph client: " + ex.Message);
                }
            }

            return graphClient;
        }
```

## <a name="send-an-email-with-microsoft-graph"></a>Enviar un correo electrónico con Microsoft Graph

Abra el archivo MailHelper.cs en su proyecto inicial. Este archivo contiene el código que crea y envía correos electrónicos. Consta de un único método (``ComposeAndSendMailAsync``) que crea y envía una solicitud POST al punto de conexión **https://graph.microsoft.com/v1.0/me/microsoft.graph.SendMail**. 

El método ``ComposeAndSendMailAsync`` adquiere tres valores de cadena (``subject``, ``bodyContent`` y ``recipients``) que le pasa el archivo MainPage.xaml.cs. Las cadenas ``subject`` y ``bodyContent`` se almacenan, junto con todas las demás cadenas de la interfaz de usuario, en el archivo Resources.resw. La cadena ``recipients`` proviene del cuadro de dirección en la interfaz de la aplicación. 

Asegúrese de que el archivo MailHelper.cs tiene las siguientes declaraciones `using`:

```
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.IO;
using System.Threading.Tasks;
using Microsoft.Graph;
using Windows.Storage;
```

La primera tarea dentro del método ``ComposeAndSendMailAsync`` consiste en obtener la fotografía del usuario actual de Microsoft Graph. Esta línea llama al método `GetCurrentUserPhotoStreamAsync`:

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
                StorageFile file = await Windows.ApplicationModel.Package.Current.InstalledLocation.GetFileAsync("test.jpg");
                photoStream = (await file.OpenReadAsync()).AsStreamForRead();
            }
```

Ahora que tenemos una secuencia de imagen, podemos cargar el archivo a OneDrive llamando al método `UploadFileToOneDriveAsync`:

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

Podemos obtener un vínculo para compartir para el archivo recién cargado en OneDrive llamando al método `GetSharingLinkAsync`. La cadena `bodyContent` contiene un marcador de posición para el vínculo para compartir:

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
                StorageFile file = await Windows.ApplicationModel.Package.Current.InstalledLocation.GetFileAsync("test.jpg");
                photoStream = (await file.OpenReadAsync()).AsStreamForRead();
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

##<a name="create-the-user-interface-in-mainpagexaml"></a>Crear la interfaz de usuario en MainPage.xaml

Ahora que ya ha escrito el código que realiza todo el trabajo de autenticación del usuario y del envío de un mensaje a través de Microsoft Graph, solo deberá crear la interfaz simple que se describe anteriormente. 

El archivo MainPage.xaml de su proyecto inicial ya incluye todo el lenguaje XAML que necesitará. Solo deberá agregar el código que dirige la interfaz al archivo MainPage.xaml.cs. Busque este archivo en el proyecto y ábralo.

Agregue este código en su espacio de nombres para completar la versión de la biblioteca cliente de la clase MainPage en MainPage.xaml.cs:

```
    public sealed partial class MainPage : Page
    {
        private string _mailAddress;
        private string _displayName = null;
        private MailHelper _mailHelper = new MailHelper();

        public MainPage()
        {
            this.InitializeComponent();
        }

        protected override void OnNavigatedTo(NavigationEventArgs e)
        {
            // Developer code - if you haven't registered the app yet, we warn you. 
            if (!App.Current.Resources.ContainsKey("ida:ClientID"))
            {
                InfoText.Text = ResourceLoader.GetForCurrentView().GetString("NoClientIdMessage");
                ConnectButton.IsEnabled = false;
            }
            else
            {
                InfoText.Text = ResourceLoader.GetForCurrentView().GetString("ConnectPrompt");
                ConnectButton.IsEnabled = true;
            }
        }

        /// <summary>
        /// Signs in the current user.
        /// </summary>
        /// <returns></returns>
        public async Task<bool> SignInCurrentUserAsync()
        {
            var graphClient = AuthenticationHelper.GetAuthenticatedClient();

            if (graphClient != null)
            {
                var user = await graphClient.Me.Request().GetAsync();
                string userId = user.Id;
                _mailAddress = user.UserPrincipalName;
                _displayName = user.DisplayName;
                return true;
            }
            else
            {
                return false;
            }

        }


        private async void ConnectButton_Click(object sender, RoutedEventArgs e)
        {
            ProgressBar.Visibility = Visibility.Visible;
            if (await SignInCurrentUserAsync())
            { 
                InfoText.Text = "Hi " + _displayName + "," + Environment.NewLine + ResourceLoader.GetForCurrentView().GetString("SendMailPrompt");
                MailButton.IsEnabled = true;
                EmailAddressBox.IsEnabled = true;
                ConnectButton.Visibility = Visibility.Collapsed;
                DisconnectButton.Visibility = Visibility.Visible;
                EmailAddressBox.Text = _mailAddress;
            }
            else
            {
                InfoText.Text = ResourceLoader.GetForCurrentView().GetString("AuthenticationErrorMessage");
            }

            ProgressBar.Visibility = Visibility.Collapsed;
        }

        private async void MailButton_Click(object sender, RoutedEventArgs e)
        {
            _mailAddress = EmailAddressBox.Text;
            ProgressBar.Visibility = Visibility.Visible;
            MailStatus.Text = string.Empty;
            try
            {
                await _mailHelper.ComposeAndSendMailAsync(ResourceLoader.GetForCurrentView().GetString("MailSubject"), ResourceLoader.GetForCurrentView().GetString("MailContents"), _mailAddress);
                MailStatus.Text = string.Format(ResourceLoader.GetForCurrentView().GetString("SendMailSuccess"), _mailAddress);
            }
            catch (Exception)
            {
                MailStatus.Text = ResourceLoader.GetForCurrentView().GetString("MailErrorMessage");
            }
            finally
            {
                ProgressBar.Visibility = Visibility.Collapsed;
            }
            
        }

        private void Disconnect_Click(object sender, RoutedEventArgs e)
        {
            ProgressBar.Visibility = Visibility.Visible;
            AuthenticationHelper.SignOut();
            ProgressBar.Visibility = Visibility.Collapsed;
            MailButton.IsEnabled = false;
            EmailAddressBox.IsEnabled = false;
            ConnectButton.Visibility = Visibility.Visible;
            InfoText.Text = ResourceLoader.GetForCurrentView().GetString("ConnectPrompt");
            this._displayName = null;
            this._mailAddress = null;
        }
    }
```
 
Ya ha llevado a cabo los tres pasos necesarios para interactuar con Microsoft Graph: el registro de la aplicación, la autenticación del usuario y la creación de las solicitudes. 

## <a name="run-the-app"></a>Ejecutar la aplicación
1. Pulse F5 para compilar y ejecutar la aplicación. 

2. Inicie sesión con su cuenta personal, profesional o educativa y conceda los permisos solicitados.

3. Elija el botón **Enviar correo electrónico**. Al enviar el correo, se muestra un mensaje de operación correcta debajo del botón. El mensaje del correo incluye la foto como un archivo adjunto y proporciona un vínculo para compartir al archivo cargado en OneDrive.

## <a name="next-steps"></a>Siguientes pasos
- Pruebe la API de REST mediante el [Probador de Graph](https://graph.microsoft.io/graph-explorer).
- Busque ejemplos de operaciones comunes tanto para REST como para SDK en el [Ejemplo de fragmentos de código de UWP para Microsoft Graph (SDK)](https://github.com/microsoftgraph/uwp-csharp-snippets-sample) y en el [Ejemplo de fragmentos de código de UWP para Microsoft Graph (REST)](https://github.com/microsoftgraph/uwp-csharp-snippets-rest-sample) o explore el resto de nuestros [ejemplos de UWP](https://github.com/microsoftgraph?utf8=%E2%9C%93&query=uwp) en GitHub.

## <a name="see-also"></a>Recursos adicionales
- [Biblioteca cliente .NET de Microsoft Graph](https://github.com/microsoftgraph/msgraph-sdk-dotnet)
- [Protocolos de Azure AD v2.0](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-protocols/)
- [Tokens de Azure AD v2.0](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-tokens/)

