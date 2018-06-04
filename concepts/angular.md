# <a name="get-started-with-microsoft-graph-in-an-angularjs-app"></a>Introducción a Microsoft Graph en una aplicación de AngularJS

En este artículo, se describen las tareas necesarias para obtener un token de acceso desde el punto de conexión v2.0 de Azure AD y llamar a Microsoft Graph. Le muestra los pasos para la compilación del [Ejemplo Connect de Microsoft para AngularJS](https://github.com/microsoftgraph/angular-connect-rest-sample) y explica los conceptos principales que implementará para usar Microsoft Graph. En el artículo, también se describe cómo obtener acceso a Microsoft Graph usando el [SDK de JavaScript de Microsoft Graph](https://github.com/microsoftgraph/msgraph-sdk-javascript) o llamadas de REST sin procesar.

En la imagen siguiente, se muestra la aplicación que va a crear. 

![Aplicación web después del inicio de sesión que muestra el botón “Enviar correo”](./images/angular-connect-sample.png)


**¿No desea compilar una aplicación?** Use el [inicio rápido de Microsoft Graph](https://graph.microsoft.io/es-ES/getting-started) para ponerlo todo en funcionamiento de manera rápida.

Para descargar una versión del ejemplo Connect que usa el punto de conexión de Azure AD, consulte el [Ejemplo Connect de Microsoft Graph para AngularJS](https://github.com/microsoftgraph/angular-connect-rest-sample/releases/tag/last_v1_auth).


## <a name="prerequisites"></a>Requisitos previos

Para comenzar, necesitará: 

- Una [cuenta Microsoft](https://www.outlook.com/) o una [cuenta profesional o educativa](https://docs.microsoft.com/es-ES/office/developer-program/office-365-developer-program-faq#account-types)
- [Node.js con npm](https://nodejs.org/en/download/)
- [Bower](https://bower.io)
- [Ejemplo Connect de Microsoft para AngularJS](https://github.com/microsoftgraph/angular-connect-sample). Usará la carpeta **starter-project** en los archivos de ejemplo para este tutorial.

## <a name="register-the-application"></a>Registrar la aplicación
Registre una aplicación en el Portal de registro de aplicaciones de Microsoft. Esta acción generará el identificador de la aplicación y la contraseña que usará para configurar la aplicación en Visual Studio.

1. Inicie sesión en el [Portal de registro de aplicaciones de Microsoft](https://apps.dev.microsoft.com/) mediante su cuenta personal, profesional o educativa.

2. Seleccione **Agregar una aplicación**.

3. Escriba un nombre para la aplicación y seleccione **Crear aplicación**. 
    
    Se muestra la página de registro, indicando las propiedades de la aplicación.

4. Copie el identificador de la aplicación. Este es el identificador único de la aplicación que usará para configurarla.

5. En **Plataformas**, pulse **Agregar plataforma** > **Web**.

6. Asegúrese de que la casilla **Permitir flujo implícito** esté activada y escriba *http://localhost:8080* como el URI de redireccionamiento. 

7. Seleccione **Guardar**.


## <a name="configure-the-project"></a>Configurar el proyecto
1. Abra la carpeta **starter-project** en los archivos de ejemplo.
2. En un símbolo del sistema, ejecute los siguientes comandos en el directorio raíz del proyecto inicial. Esta acción instalará las dependencias del proyecto.

        npm install  
        bower install
    
3. En los archivos del proyecto inicial, en la carpeta **public/scripts**, abra el archivo config.js.
4. En el campo **clientID**, cambie el valor del marcador de posición **ENTER_YOUR_CLIENT_ID** por el id. de aplicación que acaba de copiar.

## <a name="call-microsoft-graph-with-the-sdk"></a>Llamar a Microsoft Graph con el SDK
La aplicación llama a Microsoft Graph para obtener información del usuario y para enviar un correo electrónico en nombre de este. Estas llamadas se inician desde MainController en respuesta a los eventos de la interfaz de usuario.

Abra app.js y agregue el código siguiente al final del archivo. Esto inicializa el SDK.

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

### <a name="using-the-sdk"></a>Uso del SDK
1. En el archivo graphHelper.js, reemplace *// Get the profile of the current user* por el código siguiente. Esta acción configura y envía la solicitud GET al punto de conexión */me* y procesa la respuesta.

        // Get the profile of the current user.
        me: function me() {
          return graphClient.api('/me').get();
        },
  
2. Reemplace *// Send an email on behalf of the current user* por el código siguiente. Esta acción configura y envía la solicitud POST al punto de conexión */me/sendMail* y procesa la respuesta.

        // Send an email on behalf of the current user.
        sendMail: function sendMail(email) {
          return graphClient.api('/me/sendMail').post({ 'message' : email, 'saveToSentItems': true });
        }

3. En la carpeta **public/controllers**, abra el archivo mainController.js.

4. Reemplace *// Set the default headers and user properties* por el código siguiente. Esta acción agrega el token de acceso a la solicitud HTTP, llama a **GraphHelper.me** para obtener el perfil del usuario actual y procesa la respuesta.

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

5. Reemplace *// Send an email on behalf of the current user* por el código siguiente. Esta acción compila el mensaje de correo electrónico, llama a **GraphHelper.sendMail** y procesa la respuesta.

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

6. Guarde todos los cambios.

## <a name="run-the-app"></a>Ejecutar la aplicación

1. En un símbolo del sistema, ejecute el siguiente comando en el directorio raíz del proyecto inicial.

        npm start

2. En un explorador, navegue a *http://localhost:8080* y seleccione el botón **Conectar**.

3. Inicie sesión y conceda los permisos solicitados. 

4. De forma opcional, edite la dirección de correo electrónico del destinatario y elija el botón **Enviar correo**. Cuando se envíe el correo, se mostrará un mensaje de Operación correcta debajo del botón. 

## <a name="next-steps"></a>Pasos siguientes
- Pruebe la API de REST mediante el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).
- Explore el resto de nuestros [ejemplos de AngularJS](https://github.com/search?utf8=%E2%9C%93&q=angular+sample+user%3Amicrosoftgraph&type=Repositories&ref=searchresults) en GitHub.


## <a name="see-also"></a>Recursos adicionales
- [Protocolos de Azure AD v2.0](https://azure.microsoft.com/es-ES/documentation/articles/active-directory-v2-protocols/)
- [Tokens de Azure AD v2.0](https://azure.microsoft.com/es-ES/documentation/articles/active-directory-v2-tokens/)
