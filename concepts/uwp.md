# <a name="get-started-with-microsoft-graph-in-a-universal-windows-10-app"></a><span data-ttu-id="63c89-101">Introducción a Microsoft Graph en una aplicación de Windows 10 universal</span><span class="sxs-lookup"><span data-stu-id="63c89-101">Get started with Microsoft Graph in a universal Windows 10 app</span></span>

> <span data-ttu-id="63c89-p101">**¿Desea compilar aplicaciones para clientes empresariales?** Es posible que la aplicación no funcione si su cliente empresarial activa características de seguridad de movilidad empresarial como el <a href="https://azure.microsoft.com/en-us/documentation/articles/active-directory-conditional-access-device-policies/" target="_newtab">acceso condicional al dispositivo</a>. En casos así, es posible que no tenga constancia de esta activación y que sus clientes obtengan errores.</span><span class="sxs-lookup"><span data-stu-id="63c89-p101">**Building apps for enterprise customers?** Your app may not work if your enterprise customer turns on enterprise mobility security features like <a href="https://azure.microsoft.com/en-us/documentation/articles/active-directory-conditional-access-device-policies/" target="_newtab">conditional device access</a>. In this case, you may not know and your customers may experience errors.</span></span> 

> <span data-ttu-id="63c89-p102">Para ser compatible con **todos los clientes empresariales** en **todos los escenarios de empresa**, tiene que usar el punto de conexión de AD de Azure y administrar las aplicaciones mediante el [Portal de administración de Azure]((https://aka.ms/aadapplist)). Para obtener más información, consulte [Decidir entre los puntos de conexión de Azure AD y Azure AD v2.0 ](../concepts/auth_overview.md#deciding-between-the-azure-ad-and-azure-ad-v20-endpoints).</span><span class="sxs-lookup"><span data-stu-id="63c89-p102">To support **all enterprise customers** across **all enterprise scenarios**, you must use the Azure AD endpoint and manage your apps using the [Azure Management Portal]((https://aka.ms/aadapplist)). For more information, see [Deciding between the Azure AD and Azure AD v2.0 endpoints](../concepts/auth_overview.md#deciding-between-the-azure-ad-and-azure-ad-v20-endpoints).</span></span>

<span data-ttu-id="63c89-p103">En este artículo, se describen las tareas necesarias para obtener un token de acceso desde el [punto de conexión v2.0 de Azure AD]((https://developer.microsoft.com/es-ES/graph/docs/concepts/converged_auth)) y llamar a Microsoft Graph. Le guiará por el código del [Ejemplo Connect de Microsoft Graph para UWP (biblioteca)]((https://github.com/microsoftgraph/uwp-csharp-connect-sample)) para explicar los conceptos principales que se deben implementar en una aplicación que use Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="63c89-p103">This article describes the tasks required to get an access token from the [Azure AD v2.0 endpoint]((https://developer.microsoft.com/es-ES/graph/docs/concepts/converged_auth)) and call Microsoft Graph. It walks you through the code inside the [Microsoft Graph Connect Sample for UWP (Library)]((https://github.com/microsoftgraph/uwp-csharp-connect-sample)) samples to explain the main concepts that you have to implement in an app that uses Microsoft Graph.</span></span>

<span data-ttu-id="63c89-p104">**¿No desea compilar una aplicación?** Use el [inicio rápido de Microsoft Graph]((https://developer.microsoft.com/graph/quick-start)) para ponerlo todo en funcionamiento de manera rápida o descargue el [Ejemplo Connect de Microsoft Graph para UWP (biblioteca)]((https://github.com/microsoftgraph/uwp-csharp-connect-sample)) en el que se basa este artículo. Tenga en cuenta también que tenemos una [versión de REST de esta muestra]((https://github.com/microsoftgraph/uwp-csharp-connect-rest-sample)).</span><span class="sxs-lookup"><span data-stu-id="63c89-p104">**Don't feel like building an app?** Use the [Microsoft Graph quick start]((https://developer.microsoft.com/graph/quick-start)) to get up and running fast, or download the [Microsoft Graph Connect Sample for UWP (Library)]((https://github.com/microsoftgraph/uwp-csharp-connect-sample)) that this article is based on. Also note that we have a [REST version of this sample]((https://github.com/microsoftgraph/uwp-csharp-connect-rest-sample)).</span></span>

## <a name="sample-user-interface"></a><span data-ttu-id="63c89-112">Interfaz de usuario de ejemplo</span><span class="sxs-lookup"><span data-stu-id="63c89-112">Sample user interface</span></span>

<span data-ttu-id="63c89-113">El ejemplo contiene una interfaz de usuario muy sencilla, que consta de una barra de comandos superior, el **botón Conectar**, el botón **Enviar correo** y un cuadro de texto que se rellena automáticamente con la dirección de correo electrónico del usuario que ha iniciado sesión pero puede modificarse.</span><span class="sxs-lookup"><span data-stu-id="63c89-113">The sample contains a very simple user interface, consisting of a top command bar, a **connect button**, a **send mail** button, and a text box that is automatically populated with the signed-in user's e-mail address but that can be edited.</span></span>

<span data-ttu-id="63c89-114">El botón **Enviar correo** está deshabilitado cuando el usuario no está conectado:</span><span class="sxs-lookup"><span data-stu-id="63c89-114">The **send mail** button is disabled when the user has not connected:</span></span>

![Pantalla que muestra el botón Conectar habilitado y el botón Enviar correo deshabilitado](images/SignedOut.png)

<span data-ttu-id="63c89-116">En la barra de comandos superior, aparece un botón de desconexión cuando el usuario está conectado:</span><span class="sxs-lookup"><span data-stu-id="63c89-116">The top command bar contains a disconnect button when the user has connected:</span></span>

![Pantalla que muestra la dirección de correo electrónico del usuario conectado y el botón Enviar correo habilitado](images/SignedIn.png)

<span data-ttu-id="63c89-118">Todas las cadenas de la interfaz de usuario del ejemplo se almacenan en el archivo Resources.resw dentro de la carpeta Assets.</span><span class="sxs-lookup"><span data-stu-id="63c89-118">All of the sample's UI strings are stored in the Resources.resw file inside the Assets folder.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="63c89-119">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="63c89-119">Prerequisites</span></span>

<span data-ttu-id="63c89-120">Para comenzar, necesitará:</span><span class="sxs-lookup"><span data-stu-id="63c89-120">To get started, you'll need:</span></span> 

- <span data-ttu-id="63c89-121">Una [cuenta Microsoft]((https://www.outlook.com/)) o una [cuenta profesional o educativa]((http://dev.office.com/devprogram))</span><span class="sxs-lookup"><span data-stu-id="63c89-121">A [Microsoft account]((https://www.outlook.com/)) or a [work or school account]((http://dev.office.com/devprogram))</span></span>
- <span data-ttu-id="63c89-122">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="63c89-122">Using Visual Studio 2017</span></span> 
- <span data-ttu-id="63c89-p105">[Proyecto inicial de Microsoft Graph para UWP (biblioteca)]((https://github.com/microsoftgraph/uwp-csharp-connect-sample)/tree/master/starter). Ambas plantillas contienen clases a las que agregará código. También contienen cadenas de recursos. Para obtener este proyecto, clone o descargue el [Ejemplo Connect de Microsoft Graph UWP (biblioteca)]((https://github.com/microsoftgraph/uwp-csharp-connect-sample)) y abra la solución dentro de la carpeta **starter**.</span><span class="sxs-lookup"><span data-stu-id="63c89-p105">The [Microsoft Graph Starter Project for UWP (Library)]((https://github.com/microsoftgraph/uwp-csharp-connect-sample)/tree/master/starter). Both templates contain empty classes that you'll add code to. They also contains resource strings. To get this project, clone or download the [Microsoft Graph Connect Sample for UWP (Library)]((https://github.com/microsoftgraph/uwp-csharp-connect-sample)) and then open the solution inside the **starter** folder.</span></span>


## <a name="register-the-app"></a><span data-ttu-id="63c89-127">Registrar la aplicación</span><span class="sxs-lookup"><span data-stu-id="63c89-127">Register the app</span></span>
 
1. <span data-ttu-id="63c89-128">Inicie sesión en el [Portal de registro de aplicaciones]((https://apps.dev.microsoft.com/)) mediante su cuenta personal, profesional o educativa.</span><span class="sxs-lookup"><span data-stu-id="63c89-128">Sign into the [App Registration Portal]((https://apps.dev.microsoft.com/)) using either your personal or work or school account.</span></span>
2. <span data-ttu-id="63c89-129">Seleccione **Agregar una aplicación**.</span><span class="sxs-lookup"><span data-stu-id="63c89-129">Select **Add an app**.</span></span>
3. <span data-ttu-id="63c89-130">Escriba un nombre para la aplicación y seleccione **Crear aplicación**.</span><span class="sxs-lookup"><span data-stu-id="63c89-130">Enter a name for the app, and select **Create application**.</span></span>
    
    <span data-ttu-id="63c89-131">Se muestra la página de registro, indicando las propiedades de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="63c89-131">The registration page displays, listing the properties of your app.</span></span>
 
4. <span data-ttu-id="63c89-132">En **Plataformas**, seleccione **Agregar plataforma**.</span><span class="sxs-lookup"><span data-stu-id="63c89-132">Under **Platforms**, select **Add platform**.</span></span>
5. <span data-ttu-id="63c89-133">Seleccione **Aplicación nativa**.</span><span class="sxs-lookup"><span data-stu-id="63c89-133">Select **Native Application**.</span></span>
6. <span data-ttu-id="63c89-p106">Copie tanto el identificador de cliente (identificador de la aplicación) como los valores del URI de redireccionamiento al Portapapeles. Deberá escribir estos valores en la aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="63c89-p106">Copy both the Client Id (App Id) and Redirect URI values to the clipboard. You'll need to enter these values into the sample app.</span></span>

    <span data-ttu-id="63c89-p107">El identificador de la aplicación es un identificador único para su aplicación. El URI de redireccionamiento es un URI único que proporciona Windows 10 para cada aplicación con el fin de garantizar que los mensajes enviados a ese URI solo se envían a esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="63c89-p107">The app id is a unique identifier for your app. The redirect URI is a unique URI provided by Windows 10 for each application to ensure that messages sent to that URI are only sent to that application.</span></span> 

7. <span data-ttu-id="63c89-138">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="63c89-138">Select **Save**.</span></span>

## <a name="configure-the-project"></a><span data-ttu-id="63c89-139">Configurar el proyecto</span><span class="sxs-lookup"><span data-stu-id="63c89-139">Configure the project</span></span>

1. <span data-ttu-id="63c89-140">Abra el archivo de la solución para el proyecto inicial en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="63c89-140">Open the solution file for the starter project in Visual Studio.</span></span>
2. <span data-ttu-id="63c89-p108">Abra el archivo **App.xaml** del proyecto y busque el nodo `Application.Resources`. Reemplace los marcadores de posición identificador de la aplicación y URI de redireccionamiento por los valores correspondientes de la aplicación que haya registrado.</span><span class="sxs-lookup"><span data-stu-id="63c89-p108">Open the project's **App.xaml** file and locate the `Application.Resources` node. Replace the application ID and redirect URI placeholders with the corresponding values of the app you registered.</span></span>


```xml
    <Application.Resources>
        <!-- Add your Client Id here. -->
        <x:String x:Key="ida:ClientID">ENTER_YOUR_CLIENT_ID</x:String>
        <!-- Add your Redirect URI here. -->
        <x:String x:Key="ida:ReturnUrl">ENTER_YOUR_REDIRECT_URI</x:String>
    </Application.Resources>
```

## <a name="send-an-email-with-microsoft-graph"></a><span data-ttu-id="63c89-143">Enviar un correo electrónico con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="63c89-143">Send an email with Microsoft Graph</span></span>

<span data-ttu-id="63c89-p109">Abra el archivo MailHelper.cs en su proyecto inicial. Este archivo contiene el código que crea y envía correos electrónicos. Consta de un único método (``ComposeAndSendMailAsync``) que crea y envía una solicitud POST al punto de conexión **https://graph.microsoft.com/v1.0/me/microsoft.graph.SendMail**.</span><span class="sxs-lookup"><span data-stu-id="63c89-p109">Open the MailHelper.cs file in your starter project. This file contains the code that constructs and sends an email. It consists of a single method -- ``ComposeAndSendMailAsync`` -- that constructs and sends a POST request to the **https://graph.microsoft.com/v1.0/me/microsoft.graph.SendMail** endpoint.</span></span> 

<span data-ttu-id="63c89-p110">El método ``ComposeAndSendMailAsync`` adquiere tres valores de cadena (``subject``, ``bodyContent`` y ``recipients``) que le pasa el archivo MainPage.xaml.cs. Las cadenas ``subject`` y ``bodyContent`` se almacenan, junto con todas las demás cadenas de la interfaz de usuario, en el archivo Resources.resw. La cadena ``recipients`` proviene del cuadro de dirección en la interfaz de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="63c89-p110">The ``ComposeAndSendMailAsync`` method takes three string values -- ``subject``, ``bodyContent``, and ``recipients`` -- that are passed to it by the MainPage.xaml.cs file. The ``subject`` and ``bodyContent`` strings are stored, along with all other UI strings, in the Resources.resw file. The ``recipients`` string comes from the address box in the app's interface.</span></span> 

<span data-ttu-id="63c89-p111">La primera tarea dentro del método ``ComposeAndSendMailAsync`` consiste en obtener la fotografía del usuario actual de Microsoft Graph. Esta línea llama al método `GetCurrentUserPhotoStreamAsync`:</span><span class="sxs-lookup"><span data-stu-id="63c89-p111">The first task inside the ``ComposeAndSendMailAsync`` method is to get the current user's photo from Microsoft Graph. This line calls the `GetCurrentUserPhotoStreamAsync` method:</span></span>

```
            // Get current user photo
            Stream photoStream = await GetCurrentUserPhotoStreamAsync();
```

<span data-ttu-id="63c89-152">El método `GetCurrentUserPhotoStreamAsync` completo tiene un aspecto similar a este:</span><span class="sxs-lookup"><span data-stu-id="63c89-152">This is what the complete `GetCurrentUserPhotoStreamAsync` method looks like:</span></span>

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

<span data-ttu-id="63c89-153">Si el usuario no tiene ninguna foto, esta lógica obtiene otro archivo de imagen que se haya incluido en el proyecto:</span><span class="sxs-lookup"><span data-stu-id="63c89-153">If the user doesn't have a photo, this logic gets another image file that has been included with the project:</span></span>

```
            // If the user doesn't have a photo, or if the user account is MSA, we use a default photo

            if (photoStream == null)
            {
                StorageFile file = await Windows.ApplicationModel.Package.Current.InstalledLocation.GetFileAsync("test.jpg");
                photoStream = (await file.OpenReadAsync()).AsStreamForRead();
            }
```

<span data-ttu-id="63c89-154">Ahora que tenemos una secuencia de imagen, podemos cargar el archivo a OneDrive llamando al método `UploadFileToOneDriveAsync`:</span><span class="sxs-lookup"><span data-stu-id="63c89-154">Now that we have an image stream, we can upload the file to OneDrive by calling the `UploadFileToOneDriveAsync` method:</span></span>

```
            MemoryStream photoStreamMS = new MemoryStream();
            // Copy stream to MemoryStream object so that it can be converted to byte array.
            photoStream.CopyTo(photoStreamMS);

            DriveItem photoFile = await UploadFileToOneDriveAsync(photoStreamMS.ToArray());
```

<span data-ttu-id="63c89-155">El método `UploadFileToOneDriveAsync` completo tiene un aspecto similar a este:</span><span class="sxs-lookup"><span data-stu-id="63c89-155">This is what the complete `UploadFileToOneDriveAsync` method looks like:</span></span>

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

<span data-ttu-id="63c89-156">También podemos usar esta secuencia para crear un objeto `MessageAttachmentsCollectionPage` que se pueda pasar junto al mensaje:</span><span class="sxs-lookup"><span data-stu-id="63c89-156">We can also use this stream to create a `MessageAttachmentsCollectionPage` object that we can pass along with the message:</span></span>

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

<span data-ttu-id="63c89-p112">Podemos obtener un vínculo para compartir para el archivo recién cargado en OneDrive llamando al método `GetSharingLinkAsync`. La cadena `bodyContent` contiene un marcador de posición para el vínculo para compartir:</span><span class="sxs-lookup"><span data-stu-id="63c89-p112">We can get a sharing link for the newly uploaded OneDrive file by calling the `GetSharingLinkAsync` method. The `bodyContent` string contains a placeholder for the sharing link:</span></span>

```
            // Get the sharing link and insert it into the message body.
            Permission sharingLink = await GetSharingLinkAsync(photoFile.Id);
            string bodyContentWithSharingLink = String.Format(bodyContent, sharingLink.Link.WebUrl);
```

<span data-ttu-id="63c89-159">El método `GetSharingLinkAsync` completo tiene un aspecto similar a este:</span><span class="sxs-lookup"><span data-stu-id="63c89-159">This is what the complete `GetSharingLinkAsync` method looks like:</span></span>

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

<span data-ttu-id="63c89-160">Ya que el usuario puede pasar potencialmente más de una dirección, la siguiente tarea es dividir la cadena ``recipients`` en un conjunto de objetos `EmailAddress` que pueden usarse a continuación para crear la lista de objetos `Recipients` que se pasará en el cuerpo POST de la solicitud:</span><span class="sxs-lookup"><span data-stu-id="63c89-160">Since the user can potentially pass more than one address, the next task is to split the ``recipients`` string into a set of `EmailAddress` objects that can then be used to construct the list of `Recipients` objects that will be passed in the POST body of the request:</span></span>

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

<span data-ttu-id="63c89-p113">La última tarea consiste en crear un objeto `Message` y enviarlo al punto de conexión **me/microsoft.graph.SendMail** a través del `GraphServiceClient`. Ya que la cadena ``bodyContent`` es un documento HTML, la solicitud establece el valor **ContentType** a HTML.</span><span class="sxs-lookup"><span data-stu-id="63c89-p113">The last task is to construct a `Message` object and send it to the **me/microsoft.graph.SendMail** endpoint through the `GraphServiceClient`. Since the ``bodyContent`` string is an HTML document, the request sets the **ContentType** value to HTML.</span></span>

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

<span data-ttu-id="63c89-163">La clase completa tendrá este aspecto:</span><span class="sxs-lookup"><span data-stu-id="63c89-163">The complete class will look like this:</span></span>

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

 
<span data-ttu-id="63c89-164">Ya ha realizado los pasos necesarios para interactuar con Microsoft Graph: el registro de la aplicación, la autenticación del usuario y la creación de las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="63c89-164">You've now performed the steps required for interacting with Microsoft Graph: app registration, user authentication, and making the requests.</span></span> 

## <a name="run-the-app"></a><span data-ttu-id="63c89-165">Ejecutar la aplicación</span><span class="sxs-lookup"><span data-stu-id="63c89-165">Run the app</span></span>
1. <span data-ttu-id="63c89-166">Pulse F5 para compilar y ejecutar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="63c89-166">Press F5 to build and run the app.</span></span> 

2. <span data-ttu-id="63c89-167">Inicie sesión con su cuenta personal, profesional o educativa y conceda los permisos solicitados.</span><span class="sxs-lookup"><span data-stu-id="63c89-167">Sign in with your personal or work or school account and grant the requested permissions.</span></span>

3. <span data-ttu-id="63c89-p114">Elija el botón **Enviar correo electrónico**. Al enviar el correo, se muestra un mensaje de operación correcta debajo del botón. El mensaje del correo incluye la foto como un archivo adjunto y proporciona un vínculo para compartir al archivo cargado en OneDrive.</span><span class="sxs-lookup"><span data-stu-id="63c89-p114">Choose the **Send email** button. When the mail is sent, a Success message is displayed below the button. the mail message includes the photo as an attachment and also provides a sharing link to the uploaded file in OneDrive.</span></span>

## <a name="next-steps"></a><span data-ttu-id="63c89-171">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="63c89-171">Next steps</span></span>
- <span data-ttu-id="63c89-172">Pruebe la API de REST mediante el [Probador de Graph]((https://developer.microsoft.com/es-ES/graph/graph-explorer)).</span><span class="sxs-lookup"><span data-stu-id="63c89-172">Try out the REST API using the [Graph explorer]((https://developer.microsoft.com/es-ES/graph/graph-explorer)).</span></span>
- <span data-ttu-id="63c89-173">Busque ejemplos de operaciones comunes tanto para REST como para SDK en el [Ejemplo de fragmentos de código de UWP para Microsoft Graph (SDK)]((https://github.com/microsoftgraph/uwp-csharp-snippets-sample)) y en el [Ejemplo de fragmentos de código de UWP para Microsoft Graph (REST)]((https://github.com/microsoftgraph/uwp-csharp-snippets-rest-sample)) o explore el resto de nuestros [ejemplos de UWP](https://github.com/microsoftgraph?utf8=%E2%9C%93&query=uwp) en GitHub.</span><span class="sxs-lookup"><span data-stu-id="63c89-173">Find examples of common operations for both REST and SDK operations in the [Microsoft Graph UWP Snippets Sample (SDK)]((https://github.com/microsoftgraph/uwp-csharp-snippets-sample)) and the [Microsoft Graph UWP Snippets Sample (REST)]((https://github.com/microsoftgraph/uwp-csharp-snippets-rest-sample)), or explore our other [UWP samples](https://github.com/microsoftgraph?utf8=%E2%9C%93&query=uwp) on GitHub.</span></span>

## <a name="see-also"></a><span data-ttu-id="63c89-174">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="63c89-174">See also</span></span>
- <span data-ttu-id="63c89-175">[Biblioteca cliente .NET de Microsoft Graph]((https://github.com/microsoftgraph/msgraph-sdk-dotnet))</span><span class="sxs-lookup"><span data-stu-id="63c89-175">[Microsoft Graph .NET Client Library]((https://github.com/microsoftgraph/msgraph-sdk-dotnet))</span></span>
- <span data-ttu-id="63c89-176">[Protocolos de Azure AD v2.0]((https://azure.microsoft.com/es-ES/documentation/articles/active-directory-v2-protocols/))</span><span class="sxs-lookup"><span data-stu-id="63c89-176">[Azure AD v2.0 protocols]((https://azure.microsoft.com/es-ES/documentation/articles/active-directory-v2-protocols/))</span></span>
- <span data-ttu-id="63c89-177">[Tokens de Azure AD v2.0]((https://azure.microsoft.com/es-ES/documentation/articles/active-directory-v2-tokens/))</span><span class="sxs-lookup"><span data-stu-id="63c89-177">[Azure AD v2.0 tokens]((https://azure.microsoft.com/es-ES/documentation/articles/active-directory-v2-tokens/))</span></span>

