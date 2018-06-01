# <a name="get-started-with-microsoft-graph-in-a-java-app"></a>Introducción a Microsoft Graph en una aplicación Java

Este artículo usa la [console-java-connect-sample](https://github.com/microsoftgraph/console-java-connect-sample) para guiarle por el proceso de enviar correo a través de Microsoft Graph desde una aplicación de consola Java. El artículo le muestra el código que necesita agregar a la aplicación Java, por lo que puede usar la API de Microsoft Graph. La aplicación accede a Microsoft Graph mediante el [SDK de Microsoft Graph para Java](https://github.com/microsoftgraph/msgraph-sdk-java).

## <a name="choose-an-authentication-library"></a>Seleccionar una biblioteca de autenticación

Microsoft Graph adoptó los estándares de OAuth 2.0 y Open ID Connect, lo que le permite elegir entre muchas bibliotecas de Java de OAuth 2 de código abierto disponibles. El equipo de Azure AD recomienda usar [ScribeJava](https://github.com/scribejava/scribejava), una biblioteca de OAuth2 simple de Java.

La muestra implementa el flujo de concesión de código de autorización que es la opción adecuada para un escenario de autorización de cliente, un usuario y un extremo OAuth2 habilitado. En las aplicaciones de Java de servidor a servidor de producción, se usa el flujo de autorización de credenciales de cliente. **ScribeJava** controlado estos flujos de autorización. Para hacer que este ejemplo sea fácil de registrar, autenticar y ejecutar, se muestra el flujo más sencillo.

Antes de que la aplicación pueda realizar llamadas en Microsoft Graph, la aplicación debe obtener un token de acceso de Azure Active Directory (Azure AD). Este token debe estar presente en un encabezado de autenticación HTTP con cada llamada a Microsoft Graph. El **SDK de Microsoft Graph** se encarga de insertar el encabezado y agregar el token para cada llamada al implementar [IAuthenticationProvider](https://github.com/microsoftgraph/msgraph-sdk-java/blob/dev/src/main/java/com/microsoft/graph/authentication/IAuthenticationProvider.java). **ScribeJava** controla la autenticación y obtención de un token de acceso. La aplicación proporciona el token de acceso al SDK de Microsoft Graph mediante la interfaz de **IAuthenticationProvider**.

## <a name="install-and-run-the-sample"></a>Instalar y ejecutar la muestra

Para instalar y configurar la aplicación de muestra, siga las instrucciones del documento [LÉAME](https://github.com/microsoftgraph/console-java-connect-sample/blob/master/README.md) en el repositorio **console-java-connect-sample** de GitHub. Puede clonar la muestra y recorrer el código en su IDE de Java favorito con este comando para clonar el repositorio:

```
git@github.com:microsoftgraph/console-java-connect-sample.git
```

Cuando [registre la aplicación de conexión Java de consola](https://github.com/microsoftgraph/console-java-connect-sample/blob/master/README.md#register-your-app), asigne ámbitos delegados (permisos) a la muestra. Asegúrese de asignar ámbitos como se muestra en la siguiente imagen:

![Permisos de ejemplo de la consola de conexión de Java](../concepts/images/console-java-connnect-sample-permissions.JPG)

Después de registrar la aplicación y [configurar la muestra](https://github.com/microsoftgraph/console-java-connect-sample/blob/master/README.md#configure-your-app) para el **Id. de aplicación** que obtiene del registro de la aplicación, puede crear y ejecutar el ejemplo.

## <a name="console-java-connect-code"></a>Código de Console-Java-Connect 

Antes de examinar el flujo de lógica de ejemplo, dedique unos minutos para obtener información sobre la [estructura del proyecto de muestra](#sample-project-structure). Cuando tenga todo listo, examine la lógica del ejemplo:


   
### <a name="walk-through-the-code"></a>Recorra el código
Observaremos el código de ejemplo en un nivel superior y, después, profundizaremos en los detalles sobre cómo crear un mensaje de correo electrónico y enviarlo.

#### <a name="the-user-experience"></a>La experiencia de usuario

Esta sección echa un vistazo a la lógica que inicia la aplicación y, después, le muestra el resultado de ejemplo que ve el usuario al ejecutar la muestra.

El método estático **principal** [PublicClient](https://github.com/microsoftgraph/console-java-connect-sample/blob/master/src/main/java/com/microsoft/graphsample/PublicClient.java) crea una instancia de **PublicClient** y, después, inicia los procesos de cierre la sesión y de autenticación.  

[AuthenticationManager](https://github.com/microsoftgraph/console-java-connect-sample/blob/master/src/main/java/com/microsoft/graphsample/connect/AuthenticationManager) proporciona una instancia singleton que se usa para conectar el usuario a Microsoft Graph. **AuthenticationManager** expone un **token de acceso** como una propiedad de cadena. **Azure AD** devuelve el token de acceso cuando el usuario se autentica y proporciona a la muestra permiso para acceder a los recursos de Microsoft Graph solicitados. 

El método **PublicClient.startSendMail** realiza los siguientes pasos:

- Crea una nueva instancia en la clase [GraphSendMail](https://github.com/microsoftgraph/console-java-connect-sample/blob/master/src/main/java/com/microsoft/graphsample/msgraph/GraphSendMail.java). 
- Llama a **GraphSendMail.getMeUser()** para que devuelva el perfil de **Azure AD** del usuario actual para que el objeto de consola de muestra pueda personalizar los mensajes que muestra al usuario. 
- La consola muestra:

   `Hello, Laura Steele. Would you like to send an email to yourself or someone else?`

   `Enter the address to which you'd like to send a message. If you enter nothing, the message will go to your address`

- Llamadas al método **GraphSendMail.sendMail** que toman la entrada del usuario. Si se proporciona una dirección de correo electrónico, **sendMail** envía un mensaje a esa dirección. En caso contrario, se envía el mensaje para el usuario actual. 

- Solicita al usuario que envíe otro correo electrónico o cierre la aplicación de consola.

   `Email sent!`

   `Want to send another message? Type 'y' for yes and any other key to exit.`

#### <a name="the-send-mail-logic"></a>La lógica de envío de correos

La lógica de envío de correos tiene los siguientes pasos:



1. **Obtener la imagen de perfil**:<br/> Llama a **GraphServiceController.getUserProfilePicture()** para obtener una matriz de bytes que representa la imagen de perfil del usuario de **Azure AD** que ha iniciado sesión en la muestra.

   **La llamada de API**

```java
            photoStream = mGraphServiceClient
                    .me()
                    .photo()
                    .content()
                    .buildRequest()
                    .get();

```
2. **Cargar imagen en OneDrive**:
<br/>Llama a **GraphServiceController.uploadPictureToOneDrive(bytes)** para guardar la imagen de perfil en la carpeta raíz de OneDrive del usuario. Se devuelve un objeto **DriveItem** de SDK de Microsoft Graph. 

   **La llamada de API**
```java
            driveItem = mGraphServiceClient
                    .me()
                    .drive()
                    .root()
                    .itemWithPath("me2.png")
                    .content()
                    .buildRequest()
                    .put(picture);

```
3. **Obtener el vínculo de uso compartido de OneDrive de la imagen**:<br/>Llama a **GraphServiceController.getPermissionSharingLink** para crear un nuevo vínculo de uso compartido. Se devuelve un objeto **Permission** de SDK de Microsoft Graph.

   **La llamada de API**
```java
            permission = mGraphServiceClient
                    .me()
                    .drive()
                    .items(id)
                    .createLink("view", "organization")
                    .buildRequest()
                    .post();

```
4. **Reemplazar el contenido de la etiqueta de anclaje de la plantilla HTML** con la **dirección URL web** para el vínculo de uso compartido del paso anterior. 
> **Nota:** El cuerpo del mensaje enviado por la aplicación se origina como una plantilla HTML que se almacena en [Constants.java](https://github.com/microsoftgraph/console-java-connect-sample/blob/master/src/main/java/com/microsoft/graphsample/connect/Constants.java) como una cadena estática. Cuando se envía, el cuerpo del mensaje contiene un hipervínculo de uso compartido público a una imagen que la muestra en la carpeta raíz de OneDrive del usuario. 
5. **Crear un borrador**: <br/>Llama a **GraphServiceController.createDraftMail**, pasando la dirección de correo electrónico del destinatario, el texto del asunto y la plantilla HTML actualizada. Se crea un borrador y se guarda en la carpeta de borradores del usuario.

   **La llamada de API**
```java
            message = mGraphServiceClient
                    .me()
                    .messages()
                    .buildRequest()
                    .post(message);

```
6. **Adjuntar la imagen al borrador**: <br/>Llama a **GraphServiceController.addPictureToDraftMessage** para obtener el borrador y agregar la imagen al mensaje como datos adjuntos.

   **La llamada de API**
```java
            FileAttachment fileAttachment = new FileAttachment();
            fileAttachment.oDataType = "#microsoft.graph.fileAttachment";
            fileAttachment.contentBytes = attachementBytes;
            fileAttachment.name = "me.png";
            fileAttachment.size = attachementBytes.length;
            fileAttachment.isInline = false;
            fileAttachment.id = "my profile picture";

            attachment = mGraphServiceClient
                    .me()
                    .messages(messageId)
                    .attachments()
                    .buildRequest()
                    .post(fileAttachment);

```
7. **Enviar el borrador**:<br/>Llama a **GraphServiceController.sendDraftMessage** para enviar el borrador actualizado al usuario de destino.

   **La llamada de API**
```java
            mGraphServiceClient
                    .me()
                    .mailFolders("Drafts")
                    .messages(messageId)
                    .send()
                    .buildRequest()
                    .post();

```



### <a name="sample-project-structure"></a>Estructura de proyecto de muestra

### <a name="connect-package"></a>Paquete connect
Este paquete contiene la lógica de flujo de autenticación OAuth2 y la configuración que actualizará.

- [AuthenticationManager.java](https://github.com/microsoftgraph/console-java-connect-sample/blob/master/src/main/java/com/microsoft/graphsample/connect/AuthenticationManager.java): esta clase importa los objetos **ScribeJava** utilizados para el flujo de concesión de código de autorización.
- [Constants.Java](https://github.com/microsoftgraph/console-java-connect-sample/blob/master/src/main/java/com/microsoft/graphsample/connect/Constants.java): contiene cadenas estáticas públicas para proporcionar el registro de la aplicación relacionado con los valores y la plantilla para el mensaje de correo electrónico que la aplicación envíe.
- [Debug.Java](https://github.com/microsoftgraph/console-java-connect-sample/blob/master/src/main/java/com/microsoft/graphsample/connect/Debug.java): etiqueta de nivel de depuración público. Establezca su valor para cambiar el comportamiento del registro de la aplicación de muestra.
- [DebugLogger.java](https://github.com/microsoftgraph/console-java-connect-sample/blob/master/src/main/java/com/microsoft/graphsample/connect/DebugLogger.java): utilidad de registro que escribe información en la consola según el nivel de depuración establecido.
- [IConnectCallback](https://github.com/microsoftgraph/console-java-connect-sample/blob/master/src/main/java/com/microsoft/graphsample/connect/IConnectCallback.java): define el método que se usa si se llama a la sobrecarga asincrónica del método **ScribeJava.getAccessToken**.
- [SendMailException](https://github.com/microsoftgraph/console-java-connect-sample/blob/master/src/main/java/com/microsoft/graphsample/msgraph/SendMailException.java): una clase que se deriva de **Exception** y encapsula la información de excepción específica de Microsoft Graph. Las clases en el paquete **GraphSendMail** pueden producir este tipo de excepción.

### <a name="msgraph-package"></a>Paquete msgraph

Este paquete contiene la lógica que realice llamadas en Microsoft Graph.

- [GraphSendMail](https://github.com/microsoftgraph/console-java-connect-sample/blob/master/src/main/java/com/microsoft/graphsample/msgraph/GraphSendMail.java): une llamadas en **GraphServiceController** (una clase auxiliar de muestra de la API de Microsoft Graph) para crear y enviar un mensaje de correo electrónico con una imagen adjunta.
- [GraphServiceClientManager.java](https://github.com/microsoftgraph/console-java-connect-sample/blob/master/src/main/java/com/microsoft/graphsample/msgraph/GraphServiceClientManager.java): crea una instancia del SDK de Microsoft Graph [GraphServiceClient](https://github.com/microsoftgraph/msgraph-sdk-java/blob/dev/src/main/java/com/microsoft/graph/requests/extensions/GraphServiceClient.java) y agrega un token de acceso a todas las llamadas de la API salientes en el extremo de Microsoft Graph.

- [GraphServiceController.java](https://github.com/microsoftgraph/console-java-connect-sample/blob/master/src/main/java/com/microsoft/graphsample/msgraph/GraphServiceController.java): usa el SDK Microsoft Graph para realizar todas las llamadas en la **GraphServiceClient**. Las llamadas incluyen:

   - **createDraftMail**: crea un borrador de correo electrónico y lo guarda en la carpeta de borradores.
   - **sendNewMessageAsync**: crea y envía un mensaje de correo electrónico.
   - **addPictureToDraftMessage**: incluye un archivo adjunto en un borrador por identificador de mensaje
   - **addAttachmentToDraftAsync**: agrega datos adjuntos a un borrador
   - **sendDraftMessage**: envía un mensaje de la carpeta Borradores.
   - **getDraftMessage**: obtiene un mensaje de la colección de mensajes del usuario por identificador de mensaje.
   - **getUser**: obtiene el usuario local que se ha autenticado con el extremo de la API de Microsoft Graph.
   - **getUserProfilePicture**: obtiene la imagen de perfil del usuario que ha iniciado sesión de Microsoft Graph.
   - **uploadPictureToOneDrive**: carga una imagen como una matriz de bytes en la carpeta raíz de OneDrive del usuario.
   - **getPermissionSharingLink**: solicita a OneDrive que cree un vínculo de uso compartido público a una imagen almacenada en OneDrive.

## <a name="other-microsoft-graph-samples"></a>Otros ejemplos de código de Microsoft Graph

Si hay un ejemplo concreto que quiera ver, háganoslo saber [enviando un problema](https://github.com/microsoftgraph/console-java-connect-sample/issues). Estamos muy interesados en sus comentarios sobre cualquier escenario de Microsoft Graph que desee compilar en Java.

La API de Microsoft Graph es una interfaz unificadora y muy avanzada que permite trabajar con todos los tipos de datos de Microsoft. Consulte la [documentación de desarrollador](https://developer.microsoft.com/es-ES/graph/docs/concepts/overview) o el [Probador de Graph](https://developer.microsoft.com/es-ES/graph/graph-explorer) para explorar qué más puede realizar con Microsoft Graph.
