# <a name="get-started-with-microsoft-graph-in-a-nodejs-app"></a><span data-ttu-id="5a361-101">Introducción a Microsoft Graph en una aplicación de Node.js</span><span class="sxs-lookup"><span data-stu-id="5a361-101">Get started with Microsoft Graph in a Node.js app</span></span>

<span data-ttu-id="5a361-102">En este artículo, se describen las tareas necesarias para obtener un token de acceso desde el punto de conexión de Azure AD v2.0 y llamar a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="5a361-102">This article describes the tasks required to get an access token from the Azure AD v2.0 endpoint and call Microsoft Graph.</span></span> <span data-ttu-id="5a361-103">Le muestra los pasos para la compilación del [ejemplo Connect de Microsoft para Node.js](https://github.com/microsoftgraph/nodejs-connect-rest-sample) y explica los conceptos principales que implementará para usar Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="5a361-103">It walks you through building the [Microsoft Connect sample for Node.js](https://github.com/microsoftgraph/nodejs-connect-rest-sample) and explains the main concepts that you implement to use Microsoft Graph.</span></span> <span data-ttu-id="5a361-104">En el artículo se describe cómo obtener acceso a la API de Microsoft Graph mediante llamadas de REST sin procesar.</span><span class="sxs-lookup"><span data-stu-id="5a361-104">The article describes how to access the Microsoft Graph API by using raw REST calls.</span></span> <span data-ttu-id="5a361-105">Si le interesa compilar una aplicación Node.js que se conecte a Microsoft Graph con el SDK de JavaScript, vea nuestro [ejemplo Connect de Node.js basado en el SDK de Microsoft Graph](https://github.com/microsoftgraph/nodejs-connect-sample).</span><span class="sxs-lookup"><span data-stu-id="5a361-105">If you're interested in building a Node.js app that connects to Microsoft Graph with the JavaScript SDK, see our [Microsoft Graph SDK-based Node.js Connect sample](https://github.com/microsoftgraph/nodejs-connect-sample).</span></span>

<span data-ttu-id="5a361-106">En la imagen siguiente, se muestra la aplicación que va a crear.</span><span class="sxs-lookup"><span data-stu-id="5a361-106">The following image shows is the app you'll create.</span></span> 

![Aplicación web después del inicio de sesión que muestra el botón “Enviar correo”](./images/web-screenshot.png)


<span data-ttu-id="5a361-p102">**¿No desea compilar una aplicación?** Use el [inicio rápido de Microsoft Graph](https://graph.microsoft.io/es-ES/getting-started) para ponerlo todo en funcionamiento de manera rápida.</span><span class="sxs-lookup"><span data-stu-id="5a361-p102">**Don't feel like building an app?** Use the [Microsoft Graph quick start](https://graph.microsoft.io/es-ES/getting-started) to get up and running fast.</span></span>

<span data-ttu-id="5a361-110">Para descargar una versión del ejemplo Connect que usa el punto de conexión de Azure AD, consulte el [Ejemplo Connect de Microsoft Graph para Node.js](https://github.com/microsoftgraph/nodejs-connect-rest-sample/releases/tag/last_v1_auth).</span><span class="sxs-lookup"><span data-stu-id="5a361-110">To download a version of the Connect sample that uses the Azure AD endpoint, see [Microsoft Graph Connect Sample for Node.js](https://github.com/microsoftgraph/nodejs-connect-rest-sample/releases/tag/last_v1_auth).</span></span>


## <a name="prerequisites"></a><span data-ttu-id="5a361-111">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5a361-111">Prerequisites</span></span>

<span data-ttu-id="5a361-112">Para comenzar, necesitará:</span><span class="sxs-lookup"><span data-stu-id="5a361-112">To get started, you'll need:</span></span> 

- <span data-ttu-id="5a361-113">Una [cuenta Microsoft](https://www.outlook.com/) o una [cuenta profesional o educativa](https://docs.microsoft.com/es-ES/office/developer-program/office-365-developer-program-faq#account-types)</span><span class="sxs-lookup"><span data-stu-id="5a361-113">A [Microsoft account](https://www.outlook.com/) or a [work or school account](https://docs.microsoft.com/es-ES/office/developer-program/office-365-developer-program-faq#account-types)</span></span>
- [<span data-ttu-id="5a361-114">Node.js con npm</span><span class="sxs-lookup"><span data-stu-id="5a361-114">Node.js with npm</span></span>](https://nodejs.org/en/download/) 
- <span data-ttu-id="5a361-115">El [ejemplo Connect de Microsoft para Node.js](https://github.com/microsoftgraph/nodejs-connect-rest-sample).</span><span class="sxs-lookup"><span data-stu-id="5a361-115">The [Microsoft Connect sample for Node.js](https://github.com/microsoftgraph/nodejs-connect-rest-sample).</span></span> <span data-ttu-id="5a361-116">Usará la carpeta **starter-project** en los archivos de ejemplo para este tutorial.</span><span class="sxs-lookup"><span data-stu-id="5a361-116">You'll use the **starter-project** folder in the sample files for this walkthrough.</span></span>

## <a name="register-the-application"></a><span data-ttu-id="5a361-117">Registro de la aplicación</span><span class="sxs-lookup"><span data-stu-id="5a361-117">Register the application</span></span>
<span data-ttu-id="5a361-p104">Registre una aplicación en el Portal de registro de aplicaciones de Microsoft. Esta acción generará el identificador de la aplicación y la contraseña que usará para configurar la aplicación en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5a361-p104">Register an app on the Microsoft App Registration Portal. This generates the app ID and password that you'll use to configure the app in Visual Studio.</span></span>

1. <span data-ttu-id="5a361-120">Inicie sesión en el [Portal de registro de aplicaciones de Microsoft](https://apps.dev.microsoft.com/) mediante su cuenta personal, profesional o educativa.</span><span class="sxs-lookup"><span data-stu-id="5a361-120">Sign into the [Microsoft App Registration Portal](https://apps.dev.microsoft.com/) using either your personal or work or school account.</span></span>

2. <span data-ttu-id="5a361-121">Seleccione **Agregar una aplicación**.</span><span class="sxs-lookup"><span data-stu-id="5a361-121">Choose **Add an app**.</span></span>

3. <span data-ttu-id="5a361-122">Escriba un nombre para la aplicación y seleccione **Crear aplicación**.</span><span class="sxs-lookup"><span data-stu-id="5a361-122">Enter a name for the app, and choose **Create application**.</span></span> 
    
    <span data-ttu-id="5a361-123">Se muestra la página de registro, indicando las propiedades de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5a361-123">The registration page displays, listing the properties of your app.</span></span>

4. <span data-ttu-id="5a361-p105">Copie el identificador de la aplicación. Se trata del identificador único para su aplicación.</span><span class="sxs-lookup"><span data-stu-id="5a361-p105">Copy the application ID. This is the unique identifier for your app.</span></span> 

5. <span data-ttu-id="5a361-p106">En **Secretos de aplicación**, seleccione **Generar nueva contraseña**. Copie la contraseña del cuadro de diálogo **Nueva contraseña generada**.</span><span class="sxs-lookup"><span data-stu-id="5a361-p106">Under **Application Secrets**, choose **Generate New Password**. Copy the password from the **New password generated** dialog.</span></span>

    <span data-ttu-id="5a361-128">Deberá usar el identificador de la aplicación y la contraseña (secreto) para configurar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5a361-128">You'll use the application ID and application password (secret) to configure the app.</span></span> 

6. <span data-ttu-id="5a361-129">En **Plataformas**, pulse **Agregar plataforma** > **Web**.</span><span class="sxs-lookup"><span data-stu-id="5a361-129">Under **Platforms**, choose **Add platform** > **Web**.</span></span>

7. <span data-ttu-id="5a361-130">Escriba *http://localhost:3000/token* como el URI de redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="5a361-130">Enter http://localhost:3000/token as the Redirect URI.</span></span> 

8. <span data-ttu-id="5a361-131">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="5a361-131">Choose **Save**.</span></span>


## <a name="configure-the-project"></a><span data-ttu-id="5a361-132">Configurar el proyecto</span><span class="sxs-lookup"><span data-stu-id="5a361-132">Configure the project</span></span>
1. <span data-ttu-id="5a361-133">Abra la carpeta **starter-project** en los archivos de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5a361-133">Open the **starter-project** folder in the sample files.</span></span>

1. <span data-ttu-id="5a361-p107">En un símbolo del sistema, ejecute el siguiente comando en el directorio raíz del proyecto inicial. Esta acción instalará las dependencias del proyecto.</span><span class="sxs-lookup"><span data-stu-id="5a361-p107">In a command prompt, run the following command in the root directory of the starter project. This installs the project dependencies.</span></span>

        npm install

1. <span data-ttu-id="5a361-136">En los archivos del proyecto inicial, abra el archivo utils\config.js.</span><span class="sxs-lookup"><span data-stu-id="5a361-136">In the starter project files, open utils\config.js.</span></span>


1. <span data-ttu-id="5a361-137">En el campo **Credenciales**, reemplace los valores de los marcadores de posición **ENTER\_YOUR\_CLIENT\_ID** y **ENTER\_YOUR\_SECRET** por los valores que acaba de copiar.</span><span class="sxs-lookup"><span data-stu-id="5a361-137">In the **credentials** field, replace the **ENTER\_YOUR\_CLIENT\_ID** and **ENTER\_YOUR\_SECRET** placeholder values with the values you just copied.</span></span>

  
## <a name="authenticate-the-user-and-get-an-access-token"></a><span data-ttu-id="5a361-138">Autenticar al usuario y obtener un token de acceso</span><span class="sxs-lookup"><span data-stu-id="5a361-138">Authenticate the user and get an access token</span></span>
<span data-ttu-id="5a361-p108">En este paso, agregará el código de administración del token y de inicio de sesión. Pero, primero, echemos un vistazo más de cerca al flujo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="5a361-p108">In this step, you'll add sign-in and token management code. But first, let's take a closer look at the auth flow.</span></span>

<span data-ttu-id="5a361-p109">Esta aplicación usa el flujo de concesión de códigos de autorización con una identidad de usuario delegado. Para una aplicación web, el flujo requiere el identificador de la aplicación, el secreto y el URI de redireccionamiento de la aplicación registrada.</span><span class="sxs-lookup"><span data-stu-id="5a361-p109">This app uses the authorization code grant flow with a delegated user identity. For a web application, the flow requires the application ID, secret, and redirect URI from the registered app.</span></span> 

<span data-ttu-id="5a361-143">El flujo de autenticación puede desglosarse en los siguientes pasos básicos:</span><span class="sxs-lookup"><span data-stu-id="5a361-143">The auth flow can be broken down into these basic steps:</span></span>

1. <span data-ttu-id="5a361-144">Redirigir al usuario para la autenticación y el consentimiento</span><span class="sxs-lookup"><span data-stu-id="5a361-144">Redirect the user for authentication and consent</span></span>
2. <span data-ttu-id="5a361-145">Obtener un código de autorización</span><span class="sxs-lookup"><span data-stu-id="5a361-145">Get an authorization code</span></span>
3. <span data-ttu-id="5a361-146">Canjear el código de autorización por un token de acceso</span><span class="sxs-lookup"><span data-stu-id="5a361-146">Redeem the authorization code for an access token</span></span>
4. <span data-ttu-id="5a361-147">Use el token de actualización para obtener un token de acceso nuevo cuando expire el actual.</span><span class="sxs-lookup"><span data-stu-id="5a361-147">Use the refresh token to get a new access token when the access token expires</span></span>

<span data-ttu-id="5a361-p110">La aplicación usa el middleware [oauth](https://www.npmjs.com/package/oauth) para autenticar y obtener tokens. Usa el middleware [cookie-parser](https://www.npmjs.com/package/cookie-parser) para almacenar en caché la información del token en las cookies. El código que se usa para almacenar y obtener acceso a la información de token se encuentra en el controlador index.js.</span><span class="sxs-lookup"><span data-stu-id="5a361-p110">The app uses the [oauth](https://www.npmjs.com/package/oauth) middleware to authenticate and obtain tokens. It uses the [cookie-parser](https://www.npmjs.com/package/cookie-parser) middleware to cache token information in cookies. The code used to store and access token information is found in the index.js controller.</span></span>
    
   ><span data-ttu-id="5a361-p111">**Importante**: La autenticación simple y el uso de tokens en este proyecto se realizan solo con fines de ejemplo. En una aplicación de producción, deberá crear una forma más segura de usar la autenticación, incluidos el uso seguro de tokens y la validación.</span><span class="sxs-lookup"><span data-stu-id="5a361-p111">**Important** The simple authentication and token handling in this project is for sample purposes only. In a production app, you should construct a more robust way of handling authentication, including validation and secure token handling.</span></span>

<span data-ttu-id="5a361-153">Ahora ya puede agregar código para llamar a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="5a361-153">Now you're ready to add code to call Microsoft Graph.</span></span> 

## <a name="call-microsoft-graph"></a><span data-ttu-id="5a361-154">Llamar a Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="5a361-154">Call Microsoft Graph</span></span>
<span data-ttu-id="5a361-p112">La aplicación llama a Microsoft Graph para obtener información del usuario y para enviar un correo electrónico en nombre de este. Estas llamadas se inician desde el controlador index.js en respuesta a los eventos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5a361-p112">The app calls Microsoft Graph to get user information and to send an email on the user's behalf. These calls are initiated from the index.js controller in response to UI events.</span></span>

1. <span data-ttu-id="5a361-157">Abra el archivo utils\graphHelper.js.</span><span class="sxs-lookup"><span data-stu-id="5a361-157">Open utils\graphHelper.js.</span></span>

1. <span data-ttu-id="5a361-p113">Reemplace la función **getUserData** por el siguiente código. Esta acción configura y envía la solicitud GET al punto de conexión */me* y procesa la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5a361-p113">Replace the **getUserData** function with the following code. This configures and sends the GET request to the */me* endpoint and processes the response.</span></span>

        function getUserData(accessToken, callback) {
          request
           .get('https://graph.microsoft.com/v1.0/me')
           .set('Authorization', 'Bearer ' + accessToken)
           .end((err, res) => {
             callback(err, res);
           });
        }

1. <span data-ttu-id="5a361-p114">Reemplace la función **getProfilePhoto** por el siguiente código. Esta acción configura y envía la solicitud GET al punto de conexión */me/photo/$value* y procesa la respuesta. Tenga en cuenta que las fotos de perfil no están disponibles actualmente para cuentas MSA.</span><span class="sxs-lookup"><span data-stu-id="5a361-p114">Replace the **getProfilePhoto** function with the following code. This configures and sends the GET request to the */me/photo/$value* endpoint and processes the response. Note that profile photos aren't currently available for MSA accounts.</span></span>
    
        function getProfilePhoto(accessToken, callback) {
          // Get the profile photo of the current user (from the user's mailbox on Exchange Online).
          // This operation in version 1.0 supports only work or school mailboxes, not personal mailboxes.
          request
           .get('https://graph.microsoft.com/v1.0/me/photo/$value')
           .set('Authorization', 'Bearer ' + accessToken)
           .end((err, res) => {
             // Returns 200 OK and the photo in the body. If no photo exists, returns 404 Not Found.
             callback(err, res.body);
           });
        }

1. <span data-ttu-id="5a361-p115">Reemplace la función **uploadFile** por el siguiente código. Esto configura y envía la solicitud PUT al punto de conexión */me/drive/root/children/mypic.jpg/content*. Si el archivo existe, la solicitud actualiza el contenido. Si no existe, lo crea y carga el contenido de la imagen de perfil.</span><span class="sxs-lookup"><span data-stu-id="5a361-p115">Replace the **uploadFile** function with the following code. This configures and sends the PUT request to the */me/drive/root/children/mypic.jpg/content* endpoint. If the file exists, this requests updates the content. If it doesn't exist, it creates the file and uploads the contents of the profile photo.</span></span> 

        function uploadFile(accessToken, file, callback) {
          // This operation only supports files up to 4MB in size.
          // To upload larger files, see `https://developer.microsoft.com/graph/docs/api-reference/v1.0/api/item_createUploadSession`.
          request
           .put('https://graph.microsoft.com/v1.0/me/drive/root/children/mypic.jpg/content')
           .send(file)
           .set('Authorization', 'Bearer ' + accessToken)
           .set('Content-Type', 'image/jpg')
           .end((err, res) => {
             // Returns 200 OK and the file metadata in the body.
             callback(err, res.body);
           });
        }

1. <span data-ttu-id="5a361-p116">Reemplace la función **getSharingLink** por el siguiente código. Esta acción configura y envía la solicitud GET al punto de conexión */me/drive/items/{file id}/createLink* y procesa el resultado. El resultado es un vínculo para uso compartido al archivo que se incluirá en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="5a361-p116">Replace the **getSharingLink** function with the following code. This configures and sends the GET request to the */me/drive/items/{file id}/createLink* endpoint and processes the result. The result is a sharing link to the file that will be included in the message.</span></span>

        function getSharingLink(accessToken, id, callback) {
          request
           .post('https://graph.microsoft.com/v1.0/me/drive/items/' + id + '/createLink')
           .send({ type: 'view' })
           .set('Authorization', 'Bearer ' + accessToken)
           .set('Content-Type', 'application/json')
           .end((err, res) => {
             // Returns 200 OK and the permission with the link in the body.
             callback(err, res.body.link);
           });
        }

1. <span data-ttu-id="5a361-p117">Reemplace la función **postSendMail** por el siguiente código. Esta acción configura y envía la solicitud POST al punto de conexión */me/sendMail* y procesa la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5a361-p117">Replace the **postSendMail** function with the following code. This configures and sends the POST request to the */me/sendMail* endpoint and processes the response.</span></span>

        function postSendMail(accessToken, message, callback) {
          request
           .post('https://graph.microsoft.com/v1.0/me/sendMail')
           .send(message)
           .set('Authorization', 'Bearer ' + accessToken)
           .set('Content-Type', 'application/json')
           .set('Content-Length', message.length)
           .end((err, res) => {
             // Returns 202 if successful.
             // Note: If you receive a 500 - Internal Server Error
             // while using a Microsoft account (outlook.com, hotmail.com or live.com),
             // it's possible that your account has not been migrated to support this flow.
             // Check the inner error object for code 'ErrorInternalServerTransientError'.
             // You can try using a newly created Microsoft account or contact support.
             callback(err, res);
           });
        }

1. <span data-ttu-id="5a361-172">Abra el archivo utils\emailer.js.</span><span class="sxs-lookup"><span data-stu-id="5a361-172">Open utils\emailer.js.</span></span>

1. <span data-ttu-id="5a361-p118">Reemplace la función **wrapEmail** por el siguiente código. Esta acción compila la carga que representa el mensaje de correo electrónico que se enviará.</span><span class="sxs-lookup"><span data-stu-id="5a361-p118">Replace the **wrapEmail** function with the following code. This builds the payload that represents the email message to send.</span></span>

        function wrapEmail(content, recipient, file) {
          const attachments = [{
            '@odata.type': '#microsoft.graph.fileAttachment',
            ContentBytes: file,
            Name: 'mypic.jpg'
          }];
          const emailAsPayload = {
            Message: {
              Subject: 'Welcome to Microsoft Graph development with Node.js and the Microsoft Graph Connect sample',
              Body: {
                ContentType: 'HTML',
                Content: content
              },
              ToRecipients: [
                {
                  EmailAddress: {
                    Address: recipient
                  }
                }
              ]
            },
            SaveToSentItems: true,
            Attachments: attachments
          };
          return emailAsPayload;
        }

## <a name="run-the-app"></a><span data-ttu-id="5a361-175">Ejecutar la aplicación</span><span class="sxs-lookup"><span data-stu-id="5a361-175">Run the app</span></span>

1. <span data-ttu-id="5a361-176">En un símbolo del sistema, ejecute el siguiente comando en el directorio raíz del proyecto inicial.</span><span class="sxs-lookup"><span data-stu-id="5a361-176">In a command prompt, run the following command in the root directory of the starter project.</span></span>


        npm start

1. <span data-ttu-id="5a361-177">En un explorador, navegue a *http://localhost:3000* y seleccione el botón **Conectarse a Office 365**.</span><span class="sxs-lookup"><span data-stu-id="5a361-177">In a browser, navigate to http://localhost:3000 and choose the Connect to Office 365 button.</span></span>

1. <span data-ttu-id="5a361-178">Inicie sesión y conceda los permisos solicitados.</span><span class="sxs-lookup"><span data-stu-id="5a361-178">Sign in and grant the requested permissions.</span></span> 

1. <span data-ttu-id="5a361-p119">De forma opcional, edite la dirección de correo electrónico del destinatario y elija el botón **Enviar correo**. Cuando se envíe el correo, se mostrará un mensaje de Operación correcta debajo del botón.</span><span class="sxs-lookup"><span data-stu-id="5a361-p119">Optionally edit the recipient's email address, and then choose the **Send mail** button. When the mail is sent, a Success message is displayed below the button.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="5a361-181">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="5a361-181">Next steps</span></span>
- <span data-ttu-id="5a361-182">Pruebe la API de REST mediante el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).</span><span class="sxs-lookup"><span data-stu-id="5a361-182">Try out the REST API using the [Graph explorer](https://developer.microsoft.com/graph/graph-explorer).</span></span>
- <span data-ttu-id="5a361-183">Explore nuestros otros [ejemplos de Node.js](https://github.com/search?utf8=%E2%9C%93&q=node+sample+user%3Amicrosoftgraph&type=Repositories&ref=searchresults) en GitHub.</span><span class="sxs-lookup"><span data-stu-id="5a361-183">Explore our other [Node.js samples](https://github.com/search?utf8=%E2%9C%93&q=node+sample+user%3Amicrosoftgraph&type=Repositories&ref=searchresults) on GitHub.</span></span>
- <span data-ttu-id="5a361-184">Use los [tipos TypeScript de Microsoft Graph](https://github.com/microsoftgraph/msgraph-typescript-typings).</span><span class="sxs-lookup"><span data-stu-id="5a361-184">Use the [Microsoft Graph TypeScript types](https://github.com/microsoftgraph/msgraph-typescript-typings)</span></span>
- <span data-ttu-id="5a361-185">Pruebe el [SDK de JavaScript de Microsoft Graph](https://github.com/microsoftgraph/msgraph-sdk-javascript).</span><span class="sxs-lookup"><span data-stu-id="5a361-185">Try the [Microsoft Graph JavaScript SDK](https://github.com/microsoftgraph/msgraph-sdk-javascript)</span></span>

## <a name="see-also"></a><span data-ttu-id="5a361-186">Ver también</span><span class="sxs-lookup"><span data-stu-id="5a361-186">See also</span></span>
- [<span data-ttu-id="5a361-187">Protocolos de Azure AD v2.0</span><span class="sxs-lookup"><span data-stu-id="5a361-187">Azure AD v2.0 protocols</span></span>](https://azure.microsoft.com/es-ES/documentation/articles/active-directory-v2-protocols/)
- [<span data-ttu-id="5a361-188">Tokens de Azure AD v2.0</span><span class="sxs-lookup"><span data-stu-id="5a361-188">Azure AD v2.0 tokens</span></span>](https://azure.microsoft.com/es-ES/documentation/articles/active-directory-v2-tokens/)
- [<span data-ttu-id="5a361-189">Ejemplo Connect de Node.js del SDK de JavaScript de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="5a361-189">Microsoft Graph JavaScript SDK Node.js Connect sample</span></span>](https://github.com/microsoftgraph/nodejs-connect-sample)
