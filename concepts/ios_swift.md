# <a name="get-started-with-microsoft-graph-in-a-swift-ios-app"></a>Introducción a Microsoft Graph en una aplicación de iOS con Swift

> **¿Desea compilar aplicaciones para clientes empresariales?** Es posible que la aplicación no funcione si su cliente empresarial activa características de seguridad de movilidad empresarial como el <a href="https://azure.microsoft.com/en-us/documentation/articles/active-directory-conditional-access-device-policies/" target="_newtab">acceso condicional al dispositivo</a>. En casos así, es posible que no tenga constancia de esta activación y que sus clientes obtengan errores. 

> Para ser compatible con **todos los clientes empresariales** en **todos los escenarios de empresa**, tiene que usar el punto de conexión de AD de Azure y administrar las aplicaciones mediante [Azure Portal](https://aka.ms/aadapplist). Para más información, vea [Decidir entre los puntos de conexión de Azure AD y Azure AD v2.0](../concepts/auth_overview.md#deciding-between-the-azure-ad-and-azure-ad-v20-endpoints).

En este artículo, se describen las tareas necesarias para obtener un token de acceso desde el [punto de conexión de Azure AD v2.0](https://developer.microsoft.com/en-us/graph/docs/concepts/converged_auth) y llamar a Microsoft Graph. Se describe el código del [Ejemplo de conexión a Office 365 para iOS (REST)](https://github.com/microsoftgraph/ios-swift-connect-rest-sample) para explicar los conceptos básicos que se implementan en una aplicación que use Microsoft Graph. Se describe cómo obtener acceso a Microsoft Graph con operaciones de REST en un modelo asincrónico de **cadena de promesa**. Las promesas del ejemplo se implementan con el elemento [mxcl/PromiseKit 4.5.2](https://github.com/mxcl/PromiseKit/blob/master/README.md) de CocoaPod. 

Este ejemplo se creó con **Xcode 9.2** y **Swift 3.2**.

Puede descargar la versión de la aplicación que creará desde este repositorio de GitHub:

* [Ejemplo Connect de Office 365 para iOS con el SDK de Microsoft Graph](https://github.com/microsoftgraph/ios-swift-connect-rest-sample)

En la imagen siguiente, se muestra la aplicación que va a crear.

![En el tutorial de conexión de ejemplo, se muestra cómo conectarse y enviar un correo en la aplicación.](./images/iOSConnectWalkthrough.png)


El flujo de trabajo autentica y autoriza el ejemplo para obtener acceso a recursos de Microsoft Graph, inicia sesión con su cuenta personal o profesional y, por último, envía un correo a un destinatario.

**¿No desea compilar una aplicación?** Use el [inicio rápido de Microsoft Graph](https://developer.microsoft.com/en-us/graph/quick-start) para ponerlo todo en funcionamiento de manera rápida.

## <a name="prerequisites"></a>Requisitos previos

Para comenzar, necesitará: 

* [Xcode](https://developer.apple.com/xcode/downloads/) de Apple
* Instalación de [CocoaPods](https://guides.cocoapods.org/using/using-cocoapods.html) como un administrador de dependencias.
* Instalación de [Carthage](https://github.com/Carthage/Carthage) para importar y compilar la biblioteca de biblioteca de **MSAL**.
* Instalación del elemento [PromiseKit 4.5.2](https://github.com/mxcl/PromiseKit/blob/master/Documentation/Installation.md) de CocoaPod. 
* Una [cuenta Microsoft](https://www.outlook.com/) o una [cuenta profesional o educativa](https://docs.microsoft.com/en-us/office/developer-program/office-365-developer-program-faq#account-types).

## <a name="register-the-app"></a>Registrar la aplicación
 
1. Inicie sesión en el [Portal de registro de aplicaciones](https://apps.dev.microsoft.com/) mediante su cuenta personal, profesional o educativa.
2. Seleccione **Agregar una aplicación**.
3. Escriba un nombre para la aplicación y seleccione **Crear aplicación**.
    
    Se muestra la página de registro, indicando las propiedades de la aplicación.
 
4. En **Plataformas**, seleccione **Agregar plataforma**.
5. Seleccione **Plataforma nativa**.
6. Copie el identificador de cliente en el Portapapeles. Deberá escribir este valor en la aplicación de ejemplo.

    El id. de la aplicación es un identificador único para su aplicación. 

7. Seleccione **Guardar**.

## <a name="importing-the-project-dependencies"></a>Importar las dependencias del proyecto

1. Clone este repositorio ([Ejemplo de conexión de Office 365 para iOS con el SDK de Microsoft Graph](https://github.com/microsoftgraph/ios-swift-connect-rest-sample)). 


2. Use CocoaPods para importar las dependencias de PromiseKit. Esta aplicación de ejemplo ya contiene un podfile que recibirá los pods en el proyecto. Vaya a la carpeta raíz del proyecto en la aplicación **Terminal** y, desde **Terminal**, ejecute lo siguiente:

        pod install

   Recibirá la confirmación de la importación de los pods al proyecto. Para obtener más información, vea [CocoaPods](https://guides.cocoapods.org/using/using-cocoapods.html)

## <a name="install-the-msal-authentication-framework"></a>Instalación del marco de autenticación de MSAL

La versión preliminar de MSAL se distribuye como archivos de símbolos y encabezado con Carthage. Para instalar MSAL en el proyecto, siga este procedimiento:

1. Abra el terminal Bash y vaya a la carpeta raíz de la aplicación.
2. Cree un **cartfile**: copie `echo "github \"AzureAD/microsoft-authentication-library-for-objc\" \"master\"" > Cartfile` en el terminal y ejecute el comando.
3. Compile la biblioteca de MSAL: copie `carthage update` en el terminal y ejecute el comando.


## <a name="enable-keychain-sharing"></a>Habilitar el uso compartido de cadenas de claves
 
Para Xcode8, tendrá que agregar el grupo de cadenas de claves; de lo contrario, la aplicación no podrá obtener acceso a la cadena de claves. Para agregar el grupo de cadenas de claves:
 
1. Seleccione el proyecto en el panel del administrador de proyectos de Xcode. (⌘ + 1).
 
2. Seleccione el destino **O365-iOS-Microsoft-Graph-Connect-swift**.

3. En la pestaña **General**, en la sección **Firma**, asegúrese de que la casilla **Administrar automáticamente la firma** esté activada y que tenga un certificado de firma válido.
 
3. En la pestaña **Funciones**, habilite la opción **Uso compartido de la cadena de claves**.
 
4. Si **com.microsoft.O365-iOS-Microsoft-Graph-Connect-Swift-REST** no está en la lista de grupos de cadenas de claves, agréguelo.

## <a name="authenticating-with-microsoft-graph"></a>Autenticación con Microsoft Graph

El flujo de trabajo de la interfaz de usuario es el siguiente: la aplicación pide al usuario que se autentique. Después de la autenticación, el usuario puede enviar un correo a otro usuario. Para realizar solicitudes con Microsoft Graph, en el ejemplo se usa la biblioteca de autenticación de **MSAL** para autenticar solicitudes HTTPS con un token de portador de OAuth 2.0 adecuado. En el proyecto de ejemplo, la clase **AuthenticationClass.swift** importa la biblioteca de **MSAL** y adquiere el token de acceso necesario para las operaciones de REST de Microsoft Graph.

1. Abra el área de trabajo del proyecto de **Xcode** (**Graph-iOS-Swift-Connect.xcworkspace**) y abra el archivo de clase **AuthenticationClass.swift**. Busque el código siguiente en esa clase.


  ```swift
     /**
     Authenticates to Microsoft Graph.
     If a user has previously signed in before and not disconnected, silent log in
     will take place.
     If not, authentication will ask for credentials
     */
    func connectToGraph(scopes: [String],
                        completion:@escaping (_ error: ApplicationConstants.MSGraphError?, _ accessToken: String) -> Bool)  {
        do {
            if let initError = self.lastInitError {
                if initError.lengthOfBytes(using: String.Encoding.ascii) > 1 {
                    throw NSError.init(domain: initError, code: 0, userInfo: nil)
                }
            }
            // We check to see if we have a current logged in user. If we don't, then we need to sign someone in.
            // We throw an interactionRequired so that we trigger the interactive signin.
            if  try authenticationProvider.users().isEmpty {
                throw NSError.init(domain: "MSALErrorDomain", code: MSALErrorCode.interactionRequired.rawValue, userInfo: nil)
            } else {
                // Acquire a token for an existing user silently
                try authenticationProvider.acquireTokenSilent(forScopes: scopes, user: authenticationProvider.users().first) { (result, error) in
                    if error == nil {
                        self.accessToken = (result?.accessToken)!
                        _ = completion(nil, self.accessToken);
                    } else {
                        //"Could not acquire token silently: \(error ?? "No error information" as! Error )"
                       var _ = completion(ApplicationConstants.MSGraphError.nsErrorType(error: error! as NSError), "");
                    }
                }
            }
        }  catch let error as NSError {
            // interactionRequired means we need to ask the user to sign-in. This usually happens
            // when the user's Refresh Token is expired or if the user has changed their password
            // among other possible reasons.
            if error.code == MSALErrorCode.interactionRequired.rawValue {
                authenticationProvider.acquireToken(forScopes: scopes) { (result, error) in
                    if error == nil {
                        self.accessToken = (result?.accessToken)!
                        var _ = completion(nil, self.accessToken);
                    } else  {
                        var _ = completion(ApplicationConstants.MSGraphError.nsErrorType(error: error! as NSError), "");
                    }
                }
            } else {
                var _ = completion(ApplicationConstants.MSGraphError.nsErrorType(error: error as NSError), error.localizedDescription);

            }
        } catch {
            // This is the catch all error.
            var _ = completion(ApplicationConstants.MSGraphError.nsErrorType(error: error as NSError), error.localizedDescription);
        }
    }

  ```


2. Llamaremos a la función **connectToGraph** desde **ConnectViewController.swift**. Este controlador es la vista predeterminada que la aplicación carga con un único botón denominado **Conectar** que el usuario pulsa para iniciar la autenticación. 

  ```swift
// MARK: Authentication
private extension ConnectViewController {
    func authenticate() {
        loadingUI(show: true)
        let scopes = ApplicationConstants.kScopes
        AuthenticationClass.sharedInstance?.connectToGraph( scopes: scopes) {
            (result: ApplicationConstants.MSGraphError?, accessToken: String) -> Bool  in
            defer {self.loadingUI(show: false)}
            if let graphError = result {
                switch graphError {
                case .nsErrorType(let nsError):
                    print(NSLocalizedString("ERROR", comment: ""), nsError.userInfo)
                    self.showError(message: NSLocalizedString("CHECK_LOG_ERROR", comment: ""))
                }
                return false
            }
            else {
                // run on main thread!!
                DispatchQueue.main.async {
                    self.performSegue(withIdentifier: "sendMail", sender: nil)
                }
                return true
            }
        }
    }
}

  ```

## <a name="send-an-email-with-microsoft-graph"></a>Enviar un correo electrónico con Microsoft Graph

Después de conectar al usuario con Microsoft Graph, el ejemplo obtiene la dirección de correo electrónico, el nombre para mostrar y la foto de perfil del usuario autenticado. En el ejemplo, se carga la foto de perfil en la carpeta raíz de la cuenta de OneDrive del usuario y se solicita a OneDrive la URL para compartir de la imagen. Por último, en el ejemplo se publica una solicitud REST a Microsoft Graph para enviar un mensaje de correo a la dirección de correo electrónico especificada. 

El cuerpo del mensaje contiene el vínculo de uso compartido de imágenes y la imagen en sí como un archivo de imagen adjunto. El destinatario predeterminado es el usuario autenticado, pero el ejemplo permite al usuario especificar la dirección de correo electrónico de cualquier otro usuario. 

El código con el que trabajaremos aquí está en la clase **SendMailViewController_WithPromise.swift**. La función `viewDidLoad()` lee el valor `self.emailTextField.text` para obtener la dirección de correo electrónico del destinatario de correo y, después, inicia una **cadena de promesa** para obtener la imagen de perfil del usuario autenticado. Si se rechaza la promesa, no se habilitará `sendMailButton`.

1. Abra **SendMailViewController_WithPromise.swift** y busque la función `viewDidLoad`. Se llama a la función `self.userPictureWork` para iniciar la cadena de promesa.

   ```swift
    override func viewDidLoad() {
        super.viewDidLoad()
        //Get user state values before creating mail message to be sent
        do
        {
            try self.userName = AuthenticationClass.sharedInstance?.authenticationProvider.users()[0].name!
            try self.emailTextField.text = AuthenticationClass.sharedInstance?.authenticationProvider.users()[0].displayableId
            self.userEmailAddress = self.emailTextField.text
            self.headerLabel.text = "Hi, \(self.userName! )"
            
            updateUI(showActivityIndicator: true, statusText: "Getting picture", sendMail: true)

            //Important: Break out of async promise chain by declaring result returns Void
            _ = self.userPictureWork().then{
                result -> Void in
                    self.userPictureUrl = (result[1] as! String)
                    self.userProfilePicture = (result[0] as! UIImage)
                    self.updateUI(showActivityIndicator: false, statusText: "", sendMail: true)

            }.catch{err -> Void  in
                self.updateUI(showActivityIndicator: false, statusText: "", sendMail: false)

            }
        } catch _ as NSError{
            self.updateUI(showActivityIndicator: false,
                          statusText: "Error getting user profile picture.", sendMail: false)
        }
    }
  
   ```

   

1. Busque la función auxiliar de creación de solicitud del correo en la clase:

   ```swift
    /**
     Prepare mail content by loading the JSON request payload template and HTML message body template from resources and replacing placeholders in the templates with appropriate values.
     */
    func mailContent() -> Data? {
        if let emailFilePath = Bundle.main.path(forResource: "EmailPostContent", ofType: "json"),
            let emailBodyFilePath = Bundle.main.path(forResource: "EmailBody", ofType: "html")
        {
            do {
                // Prepare upload content
                let emailContent = try String(contentsOfFile: emailFilePath, encoding: String.Encoding.utf8)
                let emailBodyRaw = try String(contentsOfFile: emailBodyFilePath, encoding: String.Encoding.utf8)
                // Request doesn't accept a single quotation mark("), so change it to the acceptable form (\")
                var emailValidBody: String;
                emailValidBody = emailBodyRaw.replacingOccurrences(of: "\"", with: "\\\"")
                emailValidBody = emailValidBody.replacingOccurrences(of: "a href=%s", with: ("a href=" + self.userPictureUrl!))
                let imageData: NSData = UIImagePNGRepresentation(self.userProfilePicture!)! as NSData;
                let emailPostContent = emailContent.replacingOccurrences(of: "<EMAIL>", with: self.emailTextField.text!)
                    .replacingOccurrences(of: "<CONTENTTYPE>", with: "HTML")
                    .replacingOccurrences(of: "<CONTENT>", with: emailValidBody)
                    .replacingOccurrences(of: "<ODATA.TYPE>", with: "#microsoft.graph.fileAttachment")
                    .replacingOccurrences(of: "<IMAGE.TYPE>", with: "image\\/png")
                    .replacingOccurrences(of: "<CONTENTBYTES>", with: imageData.base64EncodedString())
                    .replacingOccurrences(of: "<NAME>", with: "me.png")
                // Return JSON payload with mail body as HTML string and attached picture as a file attachment of type NSData
                return emailPostContent.data(using: String.Encoding.utf8)
            }
            catch {
                // Error handling in case file loading fails.
                return nil
            }
        }
        // Error handling in case files aren't present.
        return nil
    }

   ```
2. Busque las siguientes funciones auxiliares para obtener la imagen de perfil del usuario, cargar la fotografía en OneDrive y solicitar un vínculo para compartir de la imagen:

   ```swift
    /**
      Async func. Get user's profile photo, upload photo to OneDrive, and get sharing link
     - returns:
        Promise<UIImage>. The user's profile picture
     */
    func getUserPicture()->Promise<UIImage?>{
        return Promise{ fulfill, reject in
            let urlRequest = self.buildRequest(operation: "GET", resource: "photo/$value") as URLRequest
            let task = URLSession.shared.dataTask(with:urlRequest){ data , res , err in
                if let err:Error = err {
                    print(err.localizedDescription)
                    return reject(err)
                }
                if ((self.checkResult(result: res!)) != HTTPError.NoError) {
                    return fulfill(self.getDefaultPicture())
                }
                if let data = data {
                    if let userImage: UIImage = UIImage(data:data) {
                        self.userProfilePicture = userImage
                        return fulfill(userImage)
                    } else {
                        return reject("no image" as! Error)
                    }
                } else {
                    return fulfill(self.getDefaultPicture())
                }
            }
            task.resume()
        }
    }
    
    /**
     Async func. Uploads a UIImage object to the signed in user's OneDrive root folder
     - Returns:
        A Promise encapsulating an array of AnyObject. Element 0 contains the user profile photo obtained in the previous chained async call
        Element 1 contains the web sharing URL of the photo in OneDrive as a String
     - Parameters:
     - UIImage: The image to upload to OneDrive
     */
    func uploadPicture(photo: UIImage) -> Promise<[AnyObject]> {
        return Promise<[AnyObject]>{ fulfill, reject in
            let uploadRequestUrl = self.buildRequest(operation: "PUT", resource: "drive/root:/me.jpg:/content", content: UIImageJPEGRepresentation(photo, 1.0)!) as URLRequest
            let task = URLSession.shared.dataTask(with:uploadRequestUrl){ data, res, err in
                if let err = err{
                    return reject(err)
                }
                if ((self.checkResult(result: res!)) != HTTPError.NoError) {
                    return reject(HTTPError.InvalidRequest)
                }
                //data can be serialized to a DriveItem object
                //https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/driveitem
                var itemId: String = "";
                if let responseContent = data {
                    itemId = self.getValueFromResponse(json: responseContent, key: "id" )
                    var returnValues = [AnyObject]();
                    returnValues.append(photo as AnyObject)
                    returnValues.append(itemId as AnyObject)
                    return fulfill(returnValues)
                }
            }
            task.resume()
        }
    }

    /**
     Async func. Requests a new sharing link for the OneDrive item specified by the item id.
     - returns:
     - Promise<String: AnyObject>. The new sharing link and the image wrapped in a Promise
     */
    func createSharingLink(itemId: String, image: UIImage) ->Promise<[AnyObject]>{
        return Promise<[AnyObject]>{ fulfill, reject in
            //Create Data object for the JSON payload
            if let sharingLinkFilePath = Bundle.main.path(forResource: "CreateSharingLink", ofType: "json")
            {
                do {
                    let sharingLinkcontent = try String(contentsOfFile: sharingLinkFilePath, encoding: String.Encoding.utf8)
                    let jsonPayload: Data = sharingLinkcontent.data(using: String.Encoding.utf8)!
                    let uploadRequestUrl = self.buildRequest(
                        operation: "POST", resource: "drive/items/"+itemId+"/createLink", content: jsonPayload) as URLRequest
                    let task = URLSession.shared.dataTask(with:uploadRequestUrl){ data, res, err in
                        if let err = err{
                            return reject(err)
                        }
                        if ((self.checkResult(result: res!)) != HTTPError.NoError) {
                            return reject(HTTPError.InvalidRequest)
                        }
                        //data can be serialized to a DriveItem object
                        //https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/driveitem
                        var sharingLink: String = "";
                        if let responseContent = data {
                            do {
                                let resultJson = try JSONSerialization.jsonObject(
                                    with: responseContent, options: []) as? [String:AnyObject]
                                sharingLink = (OneDriveFileLink.init(json:resultJson!)?.webUrl)!

                            } catch let error as NSError {
                                print(error)
                            }
                            var returnValues = [AnyObject]();
                            returnValues.append(image as AnyObject)
                            returnValues.append(sharingLink as AnyObject)
                            return fulfill(returnValues)
                        }
                    }
                    task.resume()

                }
            }
        }
   ```

3. Busque la siguiente función de envío de correo en la clase.  
 
   ```swift
    /**
     POSTS a new message to the sendmail resource
     - parameters:
        - Data: The body of the message
     */
    func sendMailRESTWithContent(_ content: Data) {
        let _ = self.sendCRUDMessage(resource: "microsoft.graph.sendmail",
                                     operation: "POST",
                                     content: content)
    }
    
    /**
     Send a create, read, update, delete (CRUD) message.
     Create= POST, Update= PUT, Delete= DELETE.
     Read= GET. Use sendGETMessage(resource: String) to read Graph contents
     - returns:
     JSON response as Data
     - parameters:
        - String: The REST resource receiving the CRUD request
        - String: the REST operation requested
        - Data: The json (as Data) representing the values to update
     */
    func sendCRUDMessage(resource: String, operation:String, content: Data)->Data  {
        var returnData: Data;
        returnData = Data.init();
        if  (self.connectToGraph()){
            if (operation == "GET") {
                return self.sendGETMessage(resource: resource)
            }
            let request = self.buildRequest(operation: operation, resource: resource, content:content);
            let task = URLSession.shared.dataTask(with:request as URLRequest, completionHandler:{ data, res, err in
                if let err = err{
                    self.updateUI(showActivityIndicator: false,
                             statusText: "Error assembling the mail content." + err.localizedDescription, sendMail: false)
                }
                let nttpError = self.checkResult(result: res!)
                if (nttpError != HTTPError.NoError) {
                    self.updateUI(showActivityIndicator: false,
                                  statusText: "Error sending the mail.", sendMail: false)
                }
                else {
                    self.updateUI(showActivityIndicator: false, statusText: "", sendMail: true)
                }
            }) // let task
             task.resume()
        }
        return returnData;
    }

   ```


## <a name="run-the-app"></a>Ejecutar la aplicación
1. Antes de ejecutar el ejemplo, tendrá que proporcionar el id. de cliente que recibió del proceso de registro en la sección **Registrar la aplicación.** Abra **Info.plist** como código fuente. 

   - Reemplace `ENTER_CLIENT_ID_HERE` por el **id. de cliente** del proceso de registro. Asegúrese de no reemplazar `msal`. Después de reemplazar la cadena, el valor de la cadena de la matriz es similar a `msal48d31887-5fad-4d73-a9f5-3c356e68a038`, donde la parte del GUID es **su** id. de cliente:  

   Por ejemplo, 

  ```xml
    <key>CFBundleURLTypes</key>
    <array>
        <dict>
            <key>CFBundleTypeRole</key>
            <string>Editor</string>
            <key>CFBundleURLName</key>
            <string>$(PRODUCT_BUNDLE_IDENTIFIER)</string>
            <key>CFBundleURLSchemes</key>
            <array>
                <string>msalENTER_CLIENT_ID_HERE</string>
                <string>auth</string>
            </array>
        </dict>
    </array>
  ```

     se convierte en… 

  ```xml
    <key>CFBundleURLTypes</key>
    <array>
        <dict>
            <key>CFBundleTypeRole</key>
            <string>Editor</string>
            <key>CFBundleURLName</key>
            <string>$(PRODUCT_BUNDLE_IDENTIFIER)</string>
            <key>CFBundleURLSchemes</key>
            <array>
                <string>msal48d31887-5fad-4d73-a9f5-3c356e68a038</string>
                <string>auth</string>
            </array>
        </dict>
    </array>
  ```

> **Nota:** Verá que, en los siguientes ámbitos de permiso de configuración para este proyecto: `["https://graph.microsoft.com/Mail.ReadWrite","https://graph.microsoft.com/Mail.Send","https://graph.microsoft.com/Files.ReadWrite","https://graph.microsoft.com/User.ReadBasic.All"]`. Para realizar las llamadas de servicio usadas en este proyecto, enviar un correo a su cuenta de correo, recuperar parte de la información del perfil (nombre para mostrar, dirección de correo electrónico) y escribir en la carpeta raíz de la cuenta de OneDrive del usuario, se necesitan estos permisos para que la aplicación pueda ejecutarse sin que se produzcan errores de permisos.

2. Ejecute el ejemplo, pulse **Conectar**, inicie sesión con su cuenta personal, profesional o educativa, y conceda los permisos solicitados.

3. Elija el botón **Enviar correo electrónico**. Cuando se envíe el correo, se mostrará un mensaje de operación correcta debajo del botón.

## <a name="next-steps"></a>Pasos siguientes
- Pruebe la API de REST mediante el [Probador de Graph](https://graph.microsoft.io/graph-explorer).
- Busque ejemplos de operaciones comunes, tanto para REST como para SDK, en el [Ejemplo de fragmentos de código de Objective C para Microsoft Graph para iOS](https://github.com/microsoftgraph/ios-objectiveC-snippets-sample).

## <a name="see-also"></a>Vea también
- [Protocolos de Azure AD v2.0](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-protocols/)
- [Tokens de Azure AD v2.0](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-tokens/)
