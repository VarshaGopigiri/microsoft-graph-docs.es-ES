# <a name="get-started-with-microsoft-graph-in-a-swift-ios-app"></a>Introducción a Microsoft Graph en una aplicación de iOS con Swift

> **¿Desea compilar aplicaciones para clientes empresariales?** Es posible que la aplicación no funcione si su cliente empresarial activa características de seguridad de movilidad empresarial como el <a href="https://azure.microsoft.com/en-us/documentation/articles/active-directory-conditional-access-device-policies/" target="_newtab">acceso condicional al dispositivo</a>. En casos así, es posible que no tenga constancia de esta activación y que sus clientes obtengan errores. 

> Para ser compatible con **todos los clientes empresariales** en **todos los escenarios de empresa**, tiene que usar el punto de conexión de AD de Azure y administrar las aplicaciones mediante [Azure Portal](https://aka.ms/aadapplist). Para más información, vea [Decidir entre los puntos de conexión de Azure AD y Azure AD v2.0](../concepts/auth_overview.md#deciding-between-the-azure-ad-and-azure-ad-v20-endpoints).

En este artículo se describen las tareas necesarias para obtener un token de acceso desde el punto de conexión de [Azure AD v2.0](https://developer.microsoft.com/es-ES/graph/docs/concepts/converged_auth) y llamar a Microsoft Graph. Le guiará por el código del [Ejemplo Connect de Office 365 para iOS (SDK)](https://github.com/microsoftgraph/ios-swift-connect-sample) para explicar los conceptos principales que se deben implementar en una aplicación que use Microsoft Graph. Describe cómo obtener acceso a Microsoft Graph mediante el [SDK de Microsoft Graph para iOS](https://github.com/microsoftgraph/msgraph-sdk-ios).

Puede descargar la versión de la aplicación que creará desde este repositorio de GitHub:

* [Ejemplo Connect de Office 365 para iOS con el SDK de Microsoft Graph](https://github.com/microsoftgraph/ios-swift-connect-sample)

En la imagen siguiente, se muestra la aplicación que va a crear.

![El tutorial de conexión de ejemplo, muestra cómo conectarse y enviar un correo en la aplicación.](./images/iOSConnectWalkthrough.png)


El flujo de trabajo será conectarse o autenticarse en Microsoft Graph, iniciar sesión con su cuenta personal o profesional y, por último, enviar un correo a un destinatario.

**¿No desea compilar una aplicación?** Use el [inicio rápido de Microsoft Graph](https://graph.microsoft.io/es-ES/getting-started) para ponerlo todo en funcionamiento de manera rápida.

## <a name="prerequisites"></a>Requisitos previos

Para comenzar, necesitará: 

* [Xcode](https://developer.apple.com/xcode/downloads/) de Apple
* La instalación de [CocoaPods](https://guides.cocoapods.org/using/using-cocoapods.html) como administrador de dependencias.
* Una [cuenta Microsoft](https://www.outlook.com/) o una [cuenta profesional o educativa](http://dev.office.com/devprogram)
* [Proyecto inicial de Microsoft Graph para iOS](https://github.com/microsoftgraph/ios-objectivec-connect-sample). Esta plantilla contiene clases a las que agregará código. Para obtener este proyecto, clone o descargue el proyecto de ejemplo desde esta ubicación y trabajará con el área de trabajo de la carpeta **starter-project** (**ios-objectivec-connect-sample.xcworkspace**).

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

1. Clone este repositorio ([Ejemplo Connect de Office 365 para iOS con el SDK de Microsoft Graph](https://github.com/microsoftgraph/ios-objectivec-connect-sample)). 
>IMPORTANTE: use el ejemplo de la carpeta starter-project y no el ejemplo de la raíz del proyecto.

2. Use CocoaPods para importar el SDK de Microsoft Graph y las dependencias de autenticación. Esta aplicación de ejemplo ya contiene un podfile que recibirá los pods en el proyecto. Vaya a la carpeta **starter-project** de la aplicación **Terminal** y, desde **Terminal**, ejecute lo siguiente:

        pod install

   Recibirá la confirmación de la importación de los pods al proyecto. Para obtener más información, consulte [CocoaPods](https://guides.cocoapods.org/using/using-cocoapods.html).


## <a name="enable-keychain-sharing"></a>Habilitar el uso compartido de cadenas de claves
 
Para Xcode 8, deberá agregar el grupo de cadenas de claves o la aplicación no podrá obtener acceso a la cadena de claves. Para agregar el grupo de cadenas de claves:
 
1. Seleccione el proyecto en el panel de administración de proyectos de Xcode. (⌘ + 1).
 
2. Seleccione **iOS-ObjectiveC-Connect-Sample**.
 
3. En la pestaña Funcionalidad, habilite **Uso compartido de cadenas de claves**.
 
4. Agregue **com.microsoft.ios-objectivec-connect-sample** a los grupos de llaves.

## <a name="authenticating-with-microsoft-graph"></a>Autenticación con Microsoft Graph

Para volver a visitar el flujo de trabajo de la interfaz de usuario, la aplicación va a solicitar al usuario que se autentique y, a continuación, este podrá enviar un correo al usuario especificado. Para realizar solicitudes en el servicio Microsoft Graph, se debe proporcionar un proveedor de autenticación que sea capaz de autenticar solicitudes HTTPS con un token de portador OAuth 2.0 adecuado. En el proyecto de ejemplo, hay una estructura de autenticación que ya tiene código auxiliar que se llama **Authentication.swift**. Agregaremos una función para solicitar (y adquirir) un token de acceso para llamar a la API de Microsoft Graph. 

1. Abra el área de trabajo del proyecto de Xcode (**Graph-iOS-Swift-Connect.xcworkspace**) y abra el archivo de extensión de la estructura **Authentication.swift**. Busque el siguiente código en esa extensión.


  ```swift
     /**
     Authenticates to Microsoft Graph. 
     If a user has previously signed in before and not disconnected, silent log in
     will take place. 
     If not, authentication will ask for credentials
     */
    func connectToGraph(withClientId clientId: String,
                                     scopes: [String],
                                     completion:@escaping (_ error: MSGraphError?) -> Void) {
    
        // Set client ID
        NXOAuth2AuthenticationProvider.setClientId(clientId, scopes: scopes)
        
        // Try silent log in. This will attempt to sign in if there is a previous successful
        // sign in user information.
        if NXOAuth2AuthenticationProvider.sharedAuth().loginSilent() == true {
            completion(nil)
        }
        // Otherwise, present log in controller.
        else {
            NXOAuth2AuthenticationProvider.sharedAuth()
                .login(with: nil) { (error: Error?) in
                    
                    if let nserror = error {
                        completion(MSGraphError.nsErrorType(error: nserror as NSError))
                    }
                    else {
                        completion(nil)
                    }
            }
        }
    }
  ```


2. Llamaremos a este método desde **ConnectViewController.swift**. Este controlador es la vista predeterminada que carga la aplicación y hay un único botón denominado **Conectar** que el usuario pulsará para iniciar el proceso de autenticación. Este método toma un parámetro, el **scopes**, a continuación analizaremos los ámbitos más detalladamente. Agregue la siguiente acción a **ConnectViewController.swift**.

  ```swift
  // MARK: Authentication
  private extension ConnectViewController {
    func authenticate() {
        loadingUI(show: true)
        
        let clientId = ApplicationConstants.clientId
        let scopes = ApplicationConstants.scopes
        
        authentication.connectToGraph(withClientId: clientId, scopes: scopes) {
            (error) in
            
            defer {self.loadingUI(show: false)}
            
            if let graphError = error {
                switch graphError {
                case .nsErrorType(let nsError):
                    print(NSLocalizedString("ERROR", comment: ""), nsError.localizedDescription)
                    self.showError(message: NSLocalizedString("CHECK_LOG_ERROR", comment: ""))
                }
            }
            else {
                self.performSegue(withIdentifier: "showSendMail", sender: nil)
            }
        }
    }
  }

  ```

## <a name="send-an-email-with-microsoft-graph"></a>Enviar un correo electrónico con Microsoft Graph

Después de configurar el proyecto para poder autenticar, las siguientes tareas obtienen la dirección de correo electrónico, el nombre para mostrar y la foto de perfil del usuario autenticado. Después de que el ejemplo obtenga dichos valores, carga la foto de perfil en OneDrive y obtiene la dirección URL para compartir de la imagen. Por último, envía un correo a un usuario mediante la API de Microsoft Graph. 

De forma predeterminada, el usuario que inició sesión será el destinatario, pero tiene la posibilidad de cambiarlo a cualquier otro destinatario. El código con el que trabajaremos aquí está en la clase **SendMailViewController.swift.** Verá que aquí hay otro código representado para la interfaz de usuario y un método auxiliar para recuperar la información del perfil del usuario desde el servicio Microsoft Graph. Nos concentraremos en los métodos para crear un mensaje de correo y enviarlo.

1. Abra **SendMailViewController.swift.**  y busque el método auxiliar de creación del cuerpo de correo en la clase:

  ```swift
    /**
     Creates sample email message
     
     - parameter emailAddress: recipient email address
     
     - returns: MSGraphMessage object with given recipient. The body is created from EmailBody.html
     */
    func createSampleMessage(to emailAddress: String, picLink pictureUrl: String) -> MSGraphMessage? {
        let message = MSGraphMessage()
        
        // set recipients
        
        let _ = self.userPicture
        let toRecipient = MSGraphRecipient()
        let msEmailAddress = MSGraphEmailAddress()
        msEmailAddress.address = emailAddress
        toRecipient.emailAddress = msEmailAddress
        let toRecipientList = [toRecipient]
        message.toRecipients = toRecipientList
        message.subject = NSLocalizedString("MAIL_SUBJECT", comment: "")
        let messageBody = MSGraphItemBody()
        messageBody.contentType = MSGraphBodyType.html()
        guard let emailBodyFilePath = Bundle.main.path(forResource: "EmailBody", ofType: "html") else {return nil}
        messageBody.content = try! String(contentsOfFile: emailBodyFilePath, encoding: String.Encoding.utf8)
        messageBody.content = messageBody.content.replacingOccurrences(of: "a href=%s", with: ("a href=" + pictureUrl))
        message.body = messageBody

        if let unwrappedImage = self.userPicture {
            let fileAttachment = MSGraphFileAttachment()
            let data = UIImageJPEGRepresentation(unwrappedImage, 1.0)
            fileAttachment.contentType = "image/png"
            fileAttachment.oDataType = "#microsoft.graph.fileAttachment"
            fileAttachment.contentBytes = data?.base64EncodedString()
            fileAttachment.name = "me.png"
            message.attachments.append(fileAttachment)
        }
        return message
    }

  ```
2. Encuentre los siguientes métodos auxiliares para obtener información del usuario, obtener una fotografía de perfil y cargar la fotografía en OneDrive:

  ```swift
      /**
     Fetches user information such as mail and display name
     */
    func getUserInfo() {
        self.sendButton.isEnabled = false
        self.statusTextView.text = NSLocalizedString("LOADING_USER_INFO", comment: "")
        
        self.graphClient.me().request().getWithCompletion {
            (user: MSGraphUser?, error: Error?) in
            if let graphError = error {
                print(NSLocalizedString("ERROR", comment: ""), graphError)
                DispatchQueue.main.async(execute: {
                    self.statusTextView.text = NSLocalizedString("GRAPH_ERROR", comment: "")
                })
            }
            else {
                guard let userInfo = user else {
                    DispatchQueue.main.async(execute: {
                        self.statusTextView.text = NSLocalizedString("USER_INFO_LOAD_FAILURE", comment: "")
                    })
                    return
                }
                DispatchQueue.main.async(execute: {
                    self.emailTextField.text = userInfo.mail
                    
                    if let displayName = userInfo.displayName {
                        self.headerLabel.text = "Hi " + displayName
                    }
                    else {
                        self.headerLabel.text = NSString(format: NSLocalizedString("HI_USER", comment: "") as NSString, "") as String
                    }
                    
                    self.statusTextView.text = NSLocalizedString("USER_INFO_LOAD_SUCCESS", comment: "")
                    self.sendButton.isEnabled = true
                })
            }
        }
    }
    
    /**
     Uploads the user's profile picture (obtained via the Graph API) to the user's OneDrive drive. The OneDrive sharing url is
     returned in the completion handler.
    */
    func uploadPictureToOneDrive(uploadFile image: UIImage?, with completion: @escaping (_ result: GraphResult<String, NSError>) ->Void) {
        
        var webUrl: String = ""
        guard let unwrappedImage = image else {
            return
        }
        let data = UIImageJPEGRepresentation(unwrappedImage, 1.0)
        self.graphClient
            .me()
            .drive()
            .root()
            .children()
            .driveItem("me.png")
            .contentRequest()
            .upload(from: data, completion: {
                (driveItem: MSGraphDriveItem?, error: Error?) in
                if let nsError = error {
                    print(NSLocalizedString("ERROR", comment: ""), nsError.localizedDescription)
                    DispatchQueue.main.async(execute: {
                        self.statusTextView.text = NSLocalizedString("UPLOAD_PICTURE_FAILURE", comment: nsError.localizedDescription)
                    })
                    return

                } else {
                    webUrl = (driveItem?.webUrl)!
                    completion(.success(webUrl))
                }
            })
    }


    /**
     Gets the user's profile picture. Returns the picture as a UIImage via completion handler
    */
    func getUserPicture(forUser upn: String, with completion: @escaping (_ result: GraphResult<UIImage, NSError>) -> Void) {
        
        //Asynchronous Graph call. Closure is invoked after getUserPicture completes. Requires @escaping attribute
        self.graphClient.me().photoValue().download {
            (url: URL?, response: URLResponse?, error: Error?) in
            
                if let nsError = error {
                    print(NSLocalizedString("ERROR", comment: ""), nsError.localizedDescription)
                    DispatchQueue.main.async(execute: {
                        self.statusTextView.text = NSLocalizedString("GET_PICTURE_FAILURE", comment: nsError.localizedDescription)
                    })
                    return
                }
                guard let picUrl = url else {
                    DispatchQueue.main.async(execute: {
                        self.statusTextView.text = NSLocalizedString("GET_PICTURE_FAILURE", comment: "User profile picture is nil")
                    })
                    return
                }
                print(picUrl)
            
                let picData = NSData(contentsOf: picUrl)
                let picImage = UIImage(data: picData! as Data)
            
                if let validPic = picImage {
                    completion(.success(validPic))
                }
                else {
                    DispatchQueue.main.async(execute: {
                        self.statusTextView.text = NSLocalizedString("GET_PICTURE_FAILURE", comment: "Picture data is invalid")
                    })
                }
            }
    }

  ```

3. Encuentre el siguiente método para enviar correo en la clase.  

  ```swift
    @IBAction func sendMail(_ sender: AnyObject) {
        guard let toEmail = self.emailTextField.text else {return}
        guard let picUrl = self.userPictureUrl else {return}
        if let message = self.createSampleMessage(to: toEmail, picLink: picUrl) {
            
            let requestBuilder = graphClient.me().sendMail(with: message, saveToSentItems: false)
            let mailRequest = requestBuilder?.request()
            
            _ = mailRequest?.execute(completion: {
                (response: [AnyHashable: Any]?, error: Error?) in
                if let nsError = error {
                    print(NSLocalizedString("ERROR", comment: ""), nsError.localizedDescription)
                    DispatchQueue.main.async(execute: {
                        self.statusTextView.text = NSLocalizedString("SEND_FAILURE", comment: "")
                    })
                }
                else {
                    DispatchQueue.main.async(execute: {
                        self.descriptionLabel.text = "Check your inbox. You have a new message :)"
                        self.statusTextView.text = NSLocalizedString("SEND_SUCCESS", comment: "")
                    })
                }
            })
        }
    }

  ```


## <a name="run-the-app"></a>Ejecutar la aplicación
1. Antes de ejecutar el ejemplo, deberá proporcionar el identificador de cliente que recibió del proceso de registro en la sección **Registrar la aplicación.** Abra **ApplicationConstants.swift**. Verá que el ClientID del proceso de registro se puede agregar a la parte superior del archivo:  

  ```swift
struct ApplicationConstants {
    static let clientId = "Enter_Client_Id_Here"
    static let scopes   = ["openid", "profile", "Mail.ReadWrite","mail.send","Files.ReadWrite","User.ReadBasic.All"]
}


  ```

> Nota: Observará que se han configurado los siguientes ámbitos de permiso para este proyecto: **"https://graph.microsoft.com/Mail.Send", "https://graph.microsoft.com/User.Read", "offline_access"**. Las llamadas de servicio usadas en este proyecto, el envío de un correo a su cuenta de correo y la recuperación de parte de la información de perfil (nombre para mostrar, dirección de correo electrónico) requieren estos permisos para que la aplicación se ejecute correctamente.

2. Ejecute el ejemplo, pulse **Conectar**, inicie sesión con su cuenta personal, profesional o educativa y conceda los permisos solicitados.

3. Elija el botón **Enviar correo electrónico**. Cuando se envíe el correo, se mostrará un mensaje de operación correcta debajo del botón.

## <a name="next-steps"></a>Pasos siguientes
- Pruebe la API de REST mediante el [Probador de Graph](https://graph.microsoft.io/graph-explorer).
- Busque ejemplos de operaciones comunes tanto para REST como para SDK en el [Ejemplo de fragmentos de código de Objective C para Microsoft Graph para iOS](https://github.com/microsoftgraph/ios-objectiveC-snippets-sample). 

## <a name="see-also"></a>Ver también
- [Protocolos de Azure AD v2.0](https://azure.microsoft.com/es-ES/documentation/articles/active-directory-v2-protocols/)
- [Tokens de Azure AD v2.0](https://azure.microsoft.com/es-ES/documentation/articles/active-directory-v2-tokens/)
