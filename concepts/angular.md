# <a name="get-started-with-microsoft-graph-in-an-angularjs-app"></a><span data-ttu-id="a0231-101">Introducción a Microsoft Graph en una aplicación de AngularJS</span><span class="sxs-lookup"><span data-stu-id="a0231-101">Get started with Microsoft Graph in an AngularJS app</span></span>

<span data-ttu-id="a0231-p101">En este artículo, se describen las tareas necesarias para obtener un token de acceso desde el punto de conexión v2.0 de Azure AD y llamar a Microsoft Graph. Le muestra los pasos para la compilación del [Ejemplo Connect de Microsoft para AngularJS](https://github.com/microsoftgraph/angular-connect-rest-sample) y explica los conceptos principales que implementará para usar Microsoft Graph. En el artículo, también se describe cómo obtener acceso a Microsoft Graph usando el [SDK de JavaScript de Microsoft Graph](https://github.com/microsoftgraph/msgraph-sdk-javascript) o llamadas de REST sin procesar.</span><span class="sxs-lookup"><span data-stu-id="a0231-p101">This article describes the tasks required to get an access token from the Azure AD v2.0 endpoint and call Microsoft Graph. It walks you through building the [Microsoft Connect Sample for AngularJS](https://github.com/microsoftgraph/angular-connect-rest-sample) and explains the main concepts that you implement to use Microsoft Graph. The article also describes how to access Microsoft Graph by using either the [Microsoft Graph JavaScript SDK](https://github.com/microsoftgraph/msgraph-sdk-javascript) or raw REST calls.</span></span>

<span data-ttu-id="a0231-105">En la imagen siguiente, se muestra la aplicación que va a crear.</span><span class="sxs-lookup"><span data-stu-id="a0231-105">The following image shows the app you'll create.</span></span> 

![Aplicación web después del inicio de sesión que muestra el botón “Enviar correo”](./images/angular-connect-sample.png)


<span data-ttu-id="a0231-p102">**¿No desea compilar una aplicación?** Use el [inicio rápido de Microsoft Graph](https://graph.microsoft.io/en-us/getting-started) para ponerlo todo en funcionamiento de manera rápida.</span><span class="sxs-lookup"><span data-stu-id="a0231-p102">**Don't feel like building an app?** Use the [Microsoft Graph quick start](https://graph.microsoft.io/en-us/getting-started) to get up and running fast.</span></span>

<span data-ttu-id="a0231-109">Para descargar una versión del ejemplo Connect que usa el punto de conexión de Azure AD, consulte el [Ejemplo Connect de Microsoft Graph para AngularJS](https://github.com/microsoftgraph/angular-connect-rest-sample/releases/tag/last_v1_auth).</span><span class="sxs-lookup"><span data-stu-id="a0231-109">To download a version of the Connect sample that uses the Azure AD endpoint, see [Microsoft Graph Connect Sample for AngularJS](https://github.com/microsoftgraph/angular-connect-rest-sample/releases/tag/last_v1_auth).</span></span>


## <a name="prerequisites"></a><span data-ttu-id="a0231-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a0231-110">Prerequisites</span></span>

<span data-ttu-id="a0231-111">Para comenzar, necesitará:</span><span class="sxs-lookup"><span data-stu-id="a0231-111">To get started, you'll need:</span></span> 

- <span data-ttu-id="a0231-112">Una [cuenta Microsoft](https://www.outlook.com/) o una [cuenta profesional o educativa](http://dev.office.com/devprogram)</span><span class="sxs-lookup"><span data-stu-id="a0231-112">A [Microsoft account](https://www.outlook.com/) or a [work or school account](http://dev.office.com/devprogram)</span></span>
- [<span data-ttu-id="a0231-113">Node.js con npm</span><span class="sxs-lookup"><span data-stu-id="a0231-113">Node.js with npm</span></span>](https://nodejs.org/en/download/)
- [<span data-ttu-id="a0231-114">Bower</span><span class="sxs-lookup"><span data-stu-id="a0231-114">Bower</span></span>](https://bower.io)
- <span data-ttu-id="a0231-p103">[Ejemplo Connect de Microsoft para AngularJS](https://github.com/microsoftgraph/angular-connect-sample). Usará la carpeta **starter-project** en los archivos de ejemplo para este tutorial.</span><span class="sxs-lookup"><span data-stu-id="a0231-p103">The [Microsoft Connect Sample for AngularJS](https://github.com/microsoftgraph/angular-connect-sample). You'll use the **starter-project** folder in the sample files for this walkthrough.</span></span>

## <a name="register-the-application"></a><span data-ttu-id="a0231-117">Registrar la aplicación</span><span class="sxs-lookup"><span data-stu-id="a0231-117">Register the application</span></span>
<span data-ttu-id="a0231-p104">Registre una aplicación en el Portal de registro de aplicaciones de Microsoft. Esta acción generará el identificador de la aplicación y la contraseña que usará para configurar la aplicación en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a0231-p104">Register an app on the Microsoft App Registration Portal. This generates the app ID and password that you'll use to configure the app in Visual Studio.</span></span>

1. <span data-ttu-id="a0231-120">Inicie sesión en el [Portal de registro de aplicaciones de Microsoft](https://apps.dev.microsoft.com/) mediante su cuenta personal, profesional o educativa.</span><span class="sxs-lookup"><span data-stu-id="a0231-120">Sign into the [Microsoft App Registration Portal](https://apps.dev.microsoft.com/) using either your personal or work or school account.</span></span>

2. <span data-ttu-id="a0231-121">Seleccione **Agregar una aplicación**.</span><span class="sxs-lookup"><span data-stu-id="a0231-121">Choose **Add an app**.</span></span>

3. <span data-ttu-id="a0231-122">Escriba un nombre para la aplicación y seleccione **Crear aplicación**.</span><span class="sxs-lookup"><span data-stu-id="a0231-122">Enter a name for the app, and choose **Create application**.</span></span> 
    
    <span data-ttu-id="a0231-123">Se muestra la página de registro, indicando las propiedades de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a0231-123">The registration page displays, listing the properties of your app.</span></span>

4. <span data-ttu-id="a0231-p105">Copie el identificador de la aplicación. Este es el identificador único de la aplicación que usará para configurarla.</span><span class="sxs-lookup"><span data-stu-id="a0231-p105">Copy the application ID. This is the unique identifier for your app that you'll use to configure the app.</span></span>

5. <span data-ttu-id="a0231-126">En **Plataformas**, elija **Agregar plataforma** > **Web**.</span><span class="sxs-lookup"><span data-stu-id="a0231-126">Under **Platforms**, choose **Add Platform** > **Web**.</span></span>

6. <span data-ttu-id="a0231-127">Asegúrese de que la casilla **Permitir flujo implícito** esté seleccionada y escriba *http://localhost:8080/* como URI de redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="a0231-127">Make sure the **Allow Implicit Flow** check box is selected, and enter *http://localhost:8080* as the Redirect URI.</span></span> 

7. <span data-ttu-id="a0231-128">Elija **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="a0231-128">Choose **Save**.</span></span>


## <a name="configure-the-project"></a><span data-ttu-id="a0231-129">Configurar el proyecto</span><span class="sxs-lookup"><span data-stu-id="a0231-129">Configure the project</span></span>
1. <span data-ttu-id="a0231-130">Abra la carpeta **starter-project** en los archivos de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a0231-130">Open the **starter-project** folder in the sample files.</span></span>
2. <span data-ttu-id="a0231-p106">En un símbolo del sistema, ejecute los siguientes comandos en el directorio raíz del proyecto inicial. Esta acción instalará las dependencias del proyecto.</span><span class="sxs-lookup"><span data-stu-id="a0231-p106">In a command prompt, run the following commands in the root directory of the starter project. This installs the project dependencies.</span></span>

        npm install  
        bower install
    
3. <span data-ttu-id="a0231-133">En los archivos del proyecto inicial, en la carpeta **public/scripts**, abra el archivo config.js.</span><span class="sxs-lookup"><span data-stu-id="a0231-133">In the starter project files, in the **public/scripts** folder, open config.js.</span></span>
4. <span data-ttu-id="a0231-134">En el campo **clientID**, cambie el valor del marcador de posición **ENTER_YOUR_CLIENT_ID** por el id. de aplicación que acaba de copiar.</span><span class="sxs-lookup"><span data-stu-id="a0231-134">In the **clientID** field, replace the **ENTER_YOUR_CLIENT_ID** placeholder value with the application ID you just copied.</span></span>

## <a name="call-microsoft-graph-with-the-sdk"></a><span data-ttu-id="a0231-135">Llamar a Microsoft Graph con el SDK</span><span class="sxs-lookup"><span data-stu-id="a0231-135">Call Microsoft Graph with the SDK</span></span>
<span data-ttu-id="a0231-p107">La aplicación llama a Microsoft Graph para obtener información del usuario y para enviar un correo electrónico en nombre de este. Estas llamadas se inician desde MainController en respuesta a los eventos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="a0231-p107">The app calls Microsoft Graph to get user information and to send an email on the user's behalf. These calls are initiated from the MainController in response to UI events.</span></span>

<span data-ttu-id="a0231-p108">Abra app.js y agregue el código siguiente al final del archivo. Esto inicializa el SDK.</span><span class="sxs-lookup"><span data-stu-id="a0231-p108">Open app.js and add the following code to the bottom of the file. This initializes the SDK.</span></span>

    var authToken;
    var graphClient = MicrosoftGraph.Client.init({
        authProvider: function(done) {
        if (typeof authToken === "undefined") {
          done({err: "No auth token"})
        } else {
          done(null, authToken); //first parameter takes an error if you can't get an access token
        }
        }
    });

### <a name="using-the-sdk"></a><span data-ttu-id="a0231-140">Uso del SDK</span><span class="sxs-lookup"><span data-stu-id="a0231-140">Using the SDK</span></span>
1. <span data-ttu-id="a0231-p109">En el archivo graphHelper.js, reemplace *// Get the profile of the current user* por el código siguiente. Esta acción configura y envía la solicitud GET al punto de conexión */me* y procesa la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0231-p109">In graphHelper.js, replace *// Get the profile of the current user* with the following code. This configures and sends the GET request to the */me* endpoint, and processes the response.</span></span>

        // Get the profile of the current user.
        me: function me() {
          return graphClient.api('/me').get();
        },
  
2. <span data-ttu-id="a0231-p110">Reemplace *// Send an email on behalf of the current user* por el código siguiente. Esta acción configura y envía la solicitud POST al punto de conexión */me/sendMail* y procesa la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0231-p110">Replace *// Send an email on behalf of the current user* with the following code. This configures and sends the POST request to the */me/sendMail* endpoint, and processes the response.</span></span>

        // Send an email on behalf of the current user.
        sendMail: function sendMail(email) {
          return graphClient.api('/me/sendMail').post({ 'message' : email, 'saveToSentItems': true });
        }

3. <span data-ttu-id="a0231-145">En la carpeta **public/controllers**, abra el archivo mainController.js.</span><span class="sxs-lookup"><span data-stu-id="a0231-145">In the **public/controllers** folder, open mainController.js.</span></span>

4. <span data-ttu-id="a0231-p111">Reemplace *// Set the default headers and user properties* por el código siguiente. Esta acción agrega el token de acceso a la solicitud HTTP, llama a **GraphHelper.me** para obtener el perfil del usuario actual y procesa la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0231-p111">Replace *// Set the default headers and user properties* with the following code. This adds the access token to the HTTP request, calls **GraphHelper.me** to get the current user's profile, and processes the response.</span></span>

        // Set the default headers and user properties.
        function processAuth() {

        // let the authProvider access the access token
        authToken = localStorage.token;

        if (localStorage.getItem('user') === null) {

          // Get the profile of the current user.
          GraphHelper.me().then(function(user) {

            // Save the user to localStorage.
            localStorage.setItem('user', angular.toJson(user));

            vm.displayName = user.displayName;
            vm.emailAddress = user.mail || user.userPrincipalName;
          });
        } else {
          let user = angular.fromJson(localStorage.user);

          vm.displayName = user.displayName;
          vm.emailAddress = user.mail || user.userPrincipalName;
        }

        }

5. <span data-ttu-id="a0231-p112">Reemplace *// Send an email on behalf of the current user* por el código siguiente. Esta acción compila el mensaje de correo electrónico, llama a **GraphHelper.sendMail** y procesa la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0231-p112">Replace *// Send an email on behalf of the current user* with the following code. This builds the email message, calls **GraphHelper.sendMail**, and processes the response.</span></span>

        // Send an email on behalf of the current user.
        function sendMail() {

          authToken = localStorage.token;       

          // Build the HTTP request payload (the Message object).
          var email = {
          Subject: 'Welcome to Microsoft Graph development with Angular and the Microsoft Graph Connect sample',
          Body: {
            ContentType: 'HTML',
            Content: getEmailContent()
          },
          ToRecipients: [
            {
              EmailAddress: {
            Address: vm.emailAddress
              }
            }
          ]
          };

          // Save email address so it doesn't get lost with two way data binding.
          vm.emailAddressSent = vm.emailAddress;
          GraphHelper.sendMail(email)
        .then(function (response) {
          $log.debug('HTTP request to the Microsoft Graph API returned successfully.', response);
          vm.requestSuccess = true;
          vm.requestFinished = true;
          $scope.$apply();
        }, function (error) {
          $log.error('HTTP request to the Microsoft Graph API failed.');
          vm.requestSuccess = false;
          vm.requestFinished = true;
          $scope.$apply();
        });

        };

6. <span data-ttu-id="a0231-150">Guarde todos los cambios.</span><span class="sxs-lookup"><span data-stu-id="a0231-150">Save all your changes.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="a0231-151">Ejecutar la aplicación</span><span class="sxs-lookup"><span data-stu-id="a0231-151">Run the app</span></span>

1. <span data-ttu-id="a0231-152">En un símbolo del sistema, ejecute el siguiente comando en el directorio raíz del proyecto inicial.</span><span class="sxs-lookup"><span data-stu-id="a0231-152">In a command prompt, run the following command in the root directory of the starter project.</span></span>

        npm start

2. <span data-ttu-id="a0231-153">En un explorador, vaya a *http://localhost:8080* y elija el botón **Conectar**.</span><span class="sxs-lookup"><span data-stu-id="a0231-153">In a browser, navigate to *http://localhost:8080* and choose the **Connect** button.</span></span>

3. <span data-ttu-id="a0231-154">Inicie sesión y conceda los permisos solicitados.</span><span class="sxs-lookup"><span data-stu-id="a0231-154">Sign in and grant the requested permissions.</span></span> 

4. <span data-ttu-id="a0231-p113">De forma opcional, edite la dirección de correo electrónico del destinatario y elija el botón **Enviar correo**. Cuando se envíe el correo, se mostrará un mensaje de Operación correcta debajo del botón.</span><span class="sxs-lookup"><span data-stu-id="a0231-p113">Optionally edit the recipient's email address, and then choose the **Send mail** button. When the mail is sent, a Success message is displayed below the button.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="a0231-157">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="a0231-157">Next steps</span></span>
- <span data-ttu-id="a0231-158">Pruebe la API de REST mediante el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).</span><span class="sxs-lookup"><span data-stu-id="a0231-158">Try out the REST API using the [Graph explorer](https://developer.microsoft.com/graph/graph-explorer).</span></span>
- <span data-ttu-id="a0231-159">Explore el resto de nuestros [ejemplos de AngularJS](https://github.com/search?utf8=%E2%9C%93&q=angular+sample+user%3Amicrosoftgraph&type=Repositories&ref=searchresults) en GitHub.</span><span class="sxs-lookup"><span data-stu-id="a0231-159">Explore our other [AngularJS samples](https://github.com/search?utf8=%E2%9C%93&q=angular+sample+user%3Amicrosoftgraph&type=Repositories&ref=searchresults) on GitHub.</span></span>


## <a name="see-also"></a><span data-ttu-id="a0231-160">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a0231-160">See also</span></span>
- [<span data-ttu-id="a0231-161">Protocolos de Azure AD v2.0</span><span class="sxs-lookup"><span data-stu-id="a0231-161">Azure AD v2.0 protocols</span></span>](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-protocols/)
- [<span data-ttu-id="a0231-162">Tokens de Azure AD v2.0</span><span class="sxs-lookup"><span data-stu-id="a0231-162">Azure AD v2.0 tokens</span></span>](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-tokens/)
