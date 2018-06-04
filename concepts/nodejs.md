# <a name="get-started-with-microsoft-graph-in-a-nodejs-app"></a>Introducción a Microsoft Graph en una aplicación de Node.js

En este artículo, se describen las tareas necesarias para obtener un token de acceso desde el punto de conexión de Azure AD v2.0 y llamar a Microsoft Graph. Le muestra los pasos para la compilación del [ejemplo Connect de Microsoft para Node.js](https://github.com/microsoftgraph/nodejs-connect-rest-sample) y explica los conceptos principales que implementará para usar Microsoft Graph. En el artículo se describe cómo obtener acceso a la API de Microsoft Graph mediante llamadas de REST sin procesar. Si le interesa compilar una aplicación Node.js que se conecte a Microsoft Graph con el SDK de JavaScript, vea nuestro [ejemplo Connect de Node.js basado en el SDK de Microsoft Graph](https://github.com/microsoftgraph/nodejs-connect-sample).

En la imagen siguiente, se muestra la aplicación que va a crear. 

![Aplicación web después del inicio de sesión que muestra el botón “Enviar correo”](./images/web-screenshot.png)


**¿No desea compilar una aplicación?** Use el [inicio rápido de Microsoft Graph](https://graph.microsoft.io/es-ES/getting-started) para ponerlo todo en funcionamiento de manera rápida.

Para descargar una versión del ejemplo Connect que usa el punto de conexión de Azure AD, consulte el [Ejemplo Connect de Microsoft Graph para Node.js](https://github.com/microsoftgraph/nodejs-connect-rest-sample/releases/tag/last_v1_auth).


## <a name="prerequisites"></a>Requisitos previos

Para comenzar, necesitará: 

- Una [cuenta Microsoft](https://www.outlook.com/) o una [cuenta profesional o educativa](https://docs.microsoft.com/es-ES/office/developer-program/office-365-developer-program-faq#account-types)
- [Node.js con npm](https://nodejs.org/en/download/) 
- El [ejemplo Connect de Microsoft para Node.js](https://github.com/microsoftgraph/nodejs-connect-rest-sample). Usará la carpeta **starter-project** en los archivos de ejemplo para este tutorial.

## <a name="register-the-application"></a>Registro de la aplicación
Registre una aplicación en el Portal de registro de aplicaciones de Microsoft. Esta acción generará el identificador de la aplicación y la contraseña que usará para configurar la aplicación en Visual Studio.

1. Inicie sesión en el [Portal de registro de aplicaciones de Microsoft](https://apps.dev.microsoft.com/) mediante su cuenta personal, profesional o educativa.

2. Seleccione **Agregar una aplicación**.

3. Escriba un nombre para la aplicación y seleccione **Crear aplicación**. 
    
    Se muestra la página de registro, indicando las propiedades de la aplicación.

4. Copie el identificador de la aplicación. Se trata del identificador único para su aplicación. 

5. En **Secretos de aplicación**, seleccione **Generar nueva contraseña**. Copie la contraseña del cuadro de diálogo **Nueva contraseña generada**.

    Deberá usar el identificador de la aplicación y la contraseña (secreto) para configurar la aplicación. 

6. En **Plataformas**, pulse **Agregar plataforma** > **Web**.

7. Escriba *http://localhost:3000/token* como el URI de redireccionamiento. 

8. Seleccione **Guardar**.


## <a name="configure-the-project"></a>Configurar el proyecto
1. Abra la carpeta **starter-project** en los archivos de ejemplo.

1. En un símbolo del sistema, ejecute el siguiente comando en el directorio raíz del proyecto inicial. Esta acción instalará las dependencias del proyecto.

        npm install

1. En los archivos del proyecto inicial, abra el archivo utils\config.js.


1. En el campo **Credenciales**, reemplace los valores de los marcadores de posición **ENTER\_YOUR\_CLIENT\_ID** y **ENTER\_YOUR\_SECRET** por los valores que acaba de copiar.

  
## <a name="authenticate-the-user-and-get-an-access-token"></a>Autenticar al usuario y obtener un token de acceso
En este paso, agregará el código de administración del token y de inicio de sesión. Pero, primero, echemos un vistazo más de cerca al flujo de autenticación.

Esta aplicación usa el flujo de concesión de códigos de autorización con una identidad de usuario delegado. Para una aplicación web, el flujo requiere el identificador de la aplicación, el secreto y el URI de redireccionamiento de la aplicación registrada. 

El flujo de autenticación puede desglosarse en los siguientes pasos básicos:

1. Redirigir al usuario para la autenticación y el consentimiento
2. Obtener un código de autorización
3. Canjear el código de autorización por un token de acceso
4. Use el token de actualización para obtener un token de acceso nuevo cuando expire el actual.

La aplicación usa el middleware [oauth](https://www.npmjs.com/package/oauth) para autenticar y obtener tokens. Usa el middleware [cookie-parser](https://www.npmjs.com/package/cookie-parser) para almacenar en caché la información del token en las cookies. El código que se usa para almacenar y obtener acceso a la información de token se encuentra en el controlador index.js.
    
   >**Importante**: La autenticación simple y el uso de tokens en este proyecto se realizan solo con fines de ejemplo. En una aplicación de producción, deberá crear una forma más segura de usar la autenticación, incluidos el uso seguro de tokens y la validación.

Ahora ya puede agregar código para llamar a Microsoft Graph. 

## <a name="call-microsoft-graph"></a>Llamar a Microsoft Graph
La aplicación llama a Microsoft Graph para obtener información del usuario y para enviar un correo electrónico en nombre de este. Estas llamadas se inician desde el controlador index.js en respuesta a los eventos de la interfaz de usuario.

1. Abra el archivo utils\graphHelper.js.

1. Reemplace la función **getUserData** por el siguiente código. Esta acción configura y envía la solicitud GET al punto de conexión */me* y procesa la respuesta.

        function getUserData(accessToken, callback) {
          request
           .get('https://graph.microsoft.com/v1.0/me')
           .set('Authorization', 'Bearer ' + accessToken)
           .end((err, res) => {
             callback(err, res);
           });
        }

1. Reemplace la función **getProfilePhoto** por el siguiente código. Esta acción configura y envía la solicitud GET al punto de conexión */me/photo/$value* y procesa la respuesta. Tenga en cuenta que las fotos de perfil no están disponibles actualmente para cuentas MSA.
    
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

1. Reemplace la función **uploadFile** por el siguiente código. Esto configura y envía la solicitud PUT al punto de conexión */me/drive/root/children/mypic.jpg/content*. Si el archivo existe, la solicitud actualiza el contenido. Si no existe, lo crea y carga el contenido de la imagen de perfil. 

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

1. Reemplace la función **getSharingLink** por el siguiente código. Esta acción configura y envía la solicitud GET al punto de conexión */me/drive/items/{file id}/createLink* y procesa el resultado. El resultado es un vínculo para uso compartido al archivo que se incluirá en el mensaje.

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

1. Reemplace la función **postSendMail** por el siguiente código. Esta acción configura y envía la solicitud POST al punto de conexión */me/sendMail* y procesa la respuesta.

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

1. Abra el archivo utils\emailer.js.

1. Reemplace la función **wrapEmail** por el siguiente código. Esta acción compila la carga que representa el mensaje de correo electrónico que se enviará.

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

## <a name="run-the-app"></a>Ejecutar la aplicación

1. En un símbolo del sistema, ejecute el siguiente comando en el directorio raíz del proyecto inicial.


        npm start

1. En un explorador, navegue a *http://localhost:3000* y seleccione el botón **Conectarse a Office 365**.

1. Inicie sesión y conceda los permisos solicitados. 

1. De forma opcional, edite la dirección de correo electrónico del destinatario y elija el botón **Enviar correo**. Cuando se envíe el correo, se mostrará un mensaje de Operación correcta debajo del botón. 

## <a name="next-steps"></a>Pasos siguientes
- Pruebe la API de REST mediante el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).
- Explore nuestros otros [ejemplos de Node.js](https://github.com/search?utf8=%E2%9C%93&q=node+sample+user%3Amicrosoftgraph&type=Repositories&ref=searchresults) en GitHub.
- Use los [tipos TypeScript de Microsoft Graph](https://github.com/microsoftgraph/msgraph-typescript-typings).
- Pruebe el [SDK de JavaScript de Microsoft Graph](https://github.com/microsoftgraph/msgraph-sdk-javascript).

## <a name="see-also"></a>Ver también
- [Protocolos de Azure AD v2.0](https://azure.microsoft.com/es-ES/documentation/articles/active-directory-v2-protocols/)
- [Tokens de Azure AD v2.0](https://azure.microsoft.com/es-ES/documentation/articles/active-directory-v2-tokens/)
- [Ejemplo Connect de Node.js del SDK de JavaScript de Microsoft Graph](https://github.com/microsoftgraph/nodejs-connect-sample)
