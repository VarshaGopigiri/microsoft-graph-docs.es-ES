# <a name="get-started-with-microsoft-graph-in-a-swift-ios-app"></a><span data-ttu-id="6b621-101">Introducción a Microsoft Graph en una aplicación de iOS con Swift</span><span class="sxs-lookup"><span data-stu-id="6b621-101">Get started with Microsoft Graph in a Swift iOS App</span></span>

> <span data-ttu-id="6b621-p101">**¿Desea compilar aplicaciones para clientes empresariales?** Es posible que la aplicación no funcione si su cliente empresarial activa características de seguridad de movilidad empresarial como el <a href="https://azure.microsoft.com/en-us/documentation/articles/active-directory-conditional-access-device-policies/" target="_newtab">acceso condicional al dispositivo</a>. En casos así, es posible que no tenga constancia de esta activación y que sus clientes obtengan errores.</span><span class="sxs-lookup"><span data-stu-id="6b621-p101">**Building apps for enterprise customers?** Your app may not work if your enterprise customer turns on enterprise mobility security features like <a href="https://azure.microsoft.com/en-us/documentation/articles/active-directory-conditional-access-device-policies/" target="_newtab">conditional device access</a>. In this case, you may not know and your customers may experience errors.</span></span> 

> <span data-ttu-id="6b621-p102">Para ser compatible con **todos los clientes empresariales** en **todos los escenarios de empresa**, tiene que usar el punto de conexión de AD de Azure y administrar las aplicaciones mediante [Azure Portal](https://aka.ms/aadapplist). Para más información, vea [Decidir entre los puntos de conexión de Azure AD y Azure AD v2.0](../concepts/auth_overview.md#deciding-between-the-azure-ad-and-azure-ad-v20-endpoints).</span><span class="sxs-lookup"><span data-stu-id="6b621-p102">To support **all enterprise customers** across **all enterprise scenarios**, you must use the Azure AD endpoint and manage your apps using the [Azure portal](https://aka.ms/aadapplist). For more information, see [Deciding between the Azure AD and Azure AD v2.0 endpoints](../concepts/auth_overview.md#deciding-between-the-azure-ad-and-azure-ad-v20-endpoints).</span></span>

<span data-ttu-id="6b621-p103">En este artículo, se describen las tareas necesarias para obtener un token de acceso desde el [punto de conexión de Azure AD v2.0](https://developer.microsoft.com/en-us/graph/docs/concepts/converged_auth) y llamar a Microsoft Graph. Se describe el código del [Ejemplo de conexión a Office 365 para iOS (REST)](https://github.com/microsoftgraph/ios-swift-connect-rest-sample) para explicar los conceptos básicos que se implementan en una aplicación que use Microsoft Graph. Se describe cómo obtener acceso a Microsoft Graph con operaciones de REST en un modelo asincrónico de **cadena de promesa**. Las promesas del ejemplo se implementan con el elemento [mxcl/PromiseKit 4.5.2](https://github.com/mxcl/PromiseKit/blob/master/README.md) de CocoaPod.</span><span class="sxs-lookup"><span data-stu-id="6b621-p103">This article describes the tasks required to get an access token from the [Azure AD v2.0 endpoint](https://developer.microsoft.com/en-us/graph/docs/concepts/converged_auth) and call Microsoft Graph. It walks you through the code inside the [Office 365 Connect Sample for iOS (REST)](https://github.com/microsoftgraph/ios-swift-connect-rest-sample) to explain the main concepts that you implement in an app that uses Microsoft Graph. It describes how to access Microsoft Graph by using REST operations in an asynchronous **Promise chain** pattern.  Promises in the sample are implemented by using the [mxcl/PromiseKit 4.5.2](https://github.com/mxcl/PromiseKit/blob/master/README.md) CocoaPod.</span></span> 

<span data-ttu-id="6b621-111">Este ejemplo se creó con **Xcode 9.2** y **Swift 3.2**.</span><span class="sxs-lookup"><span data-stu-id="6b621-111">The sample was created using **XCode 9.2** and **Swift 3.2**.</span></span>

<span data-ttu-id="6b621-112">Puede descargar la versión de la aplicación que creará desde este repositorio de GitHub:</span><span class="sxs-lookup"><span data-stu-id="6b621-112">You can download the version of the app that you'll create from this GitHub repo:</span></span>

* [<span data-ttu-id="6b621-113">Ejemplo Connect de Office 365 para iOS con el SDK de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="6b621-113">Office 365 Connect Sample for iOS Using the Microsoft Graph SDK</span></span>](https://github.com/microsoftgraph/ios-swift-connect-rest-sample)

<span data-ttu-id="6b621-114">En la imagen siguiente, se muestra la aplicación que va a crear.</span><span class="sxs-lookup"><span data-stu-id="6b621-114">The following image shows the app you'll create.</span></span>

![En el tutorial de conexión de ejemplo, se muestra cómo conectarse y enviar un correo en la aplicación.](./images/iOSConnectWalkthrough.png)


<span data-ttu-id="6b621-116">El flujo de trabajo autentica y autoriza el ejemplo para obtener acceso a recursos de Microsoft Graph, inicia sesión con su cuenta personal o profesional y, por último, envía un correo a un destinatario.</span><span class="sxs-lookup"><span data-stu-id="6b621-116">The workflow authenticates and authorizes the sample to access  Microsoft Graph resources, signs in with your work or personal account, and finally sends a mail to a recipient.</span></span>

<span data-ttu-id="6b621-p104">**¿No desea compilar una aplicación?** Use el [inicio rápido de Microsoft Graph](https://developer.microsoft.com/en-us/graph/quick-start) para ponerlo todo en funcionamiento de manera rápida.</span><span class="sxs-lookup"><span data-stu-id="6b621-p104">**Don't feel like building an app?** Use the [Microsoft Graph quick start](https://developer.microsoft.com/en-us/graph/quick-start) to get up and running fast.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6b621-119">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6b621-119">Prerequisites</span></span>

<span data-ttu-id="6b621-120">Para comenzar, necesitará:</span><span class="sxs-lookup"><span data-stu-id="6b621-120">To get started, you'll need:</span></span> 

* <span data-ttu-id="6b621-121">[Xcode](https://developer.apple.com/xcode/downloads/) de Apple</span><span class="sxs-lookup"><span data-stu-id="6b621-121">[Xcode](https://developer.apple.com/xcode/downloads/) from Apple</span></span>
* <span data-ttu-id="6b621-122">Instalación de [CocoaPods](https://guides.cocoapods.org/using/using-cocoapods.html) como un administrador de dependencias.</span><span class="sxs-lookup"><span data-stu-id="6b621-122">Installation of [CocoaPods](https://guides.cocoapods.org/using/using-cocoapods.html) as a dependency manager</span></span>
* <span data-ttu-id="6b621-123">Instalación de [Carthage](https://github.com/Carthage/Carthage) para importar y compilar la biblioteca de biblioteca de **MSAL**.</span><span class="sxs-lookup"><span data-stu-id="6b621-123">Installation of [Carthage](https://github.com/Carthage/Carthage) to import and build the **MSAL** library.</span></span>
* <span data-ttu-id="6b621-124">Instalación del elemento [PromiseKit 4.5.2](https://github.com/mxcl/PromiseKit/blob/master/Documentation/Installation.md) de CocoaPod.</span><span class="sxs-lookup"><span data-stu-id="6b621-124">Installation of the [PromiseKit 4.5.2](https://github.com/mxcl/PromiseKit/blob/master/Documentation/Installation.md) Cocoapod.</span></span> 
* <span data-ttu-id="6b621-125">Una [cuenta Microsoft](https://www.outlook.com/) o una [cuenta profesional o educativa](https://docs.microsoft.com/en-us/office/developer-program/office-365-developer-program-faq#account-types).</span><span class="sxs-lookup"><span data-stu-id="6b621-125">A [Microsoft account](https://www.outlook.com/) or a [work or school account](https://docs.microsoft.com/en-us/office/developer-program/office-365-developer-program-faq#account-types)</span></span>

## <a name="register-the-app"></a><span data-ttu-id="6b621-126">Registrar la aplicación</span><span class="sxs-lookup"><span data-stu-id="6b621-126">Register the app</span></span>
 
1. <span data-ttu-id="6b621-127">Inicie sesión en el [Portal de registro de aplicaciones](https://apps.dev.microsoft.com/) mediante su cuenta personal, profesional o educativa.</span><span class="sxs-lookup"><span data-stu-id="6b621-127">Sign into the [App Registration Portal](https://apps.dev.microsoft.com/) using either your personal or work or school account.</span></span>
2. <span data-ttu-id="6b621-128">Seleccione **Agregar una aplicación**.</span><span class="sxs-lookup"><span data-stu-id="6b621-128">Select **Add an app**.</span></span>
3. <span data-ttu-id="6b621-129">Escriba un nombre para la aplicación y seleccione **Crear aplicación**.</span><span class="sxs-lookup"><span data-stu-id="6b621-129">Enter a name for the app, and select **Create application**.</span></span>
    
    <span data-ttu-id="6b621-130">Se muestra la página de registro, indicando las propiedades de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6b621-130">The registration page displays, listing the properties of your app.</span></span>
 
4. <span data-ttu-id="6b621-131">En **Plataformas**, seleccione **Agregar plataforma**.</span><span class="sxs-lookup"><span data-stu-id="6b621-131">Under **Platforms**, select **Add platform**.</span></span>
5. <span data-ttu-id="6b621-132">Seleccione **Plataforma nativa**.</span><span class="sxs-lookup"><span data-stu-id="6b621-132">Select **Native platform**.</span></span>
6. <span data-ttu-id="6b621-p105">Copie el identificador de cliente en el Portapapeles. Deberá escribir este valor en la aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="6b621-p105">Copy the Client Id to the clipboard. You'll need to enter this value into the sample app.</span></span>

    <span data-ttu-id="6b621-135">El id. de la aplicación es un identificador único para su aplicación.</span><span class="sxs-lookup"><span data-stu-id="6b621-135">The app id is a unique identifier for your app.</span></span> 

7. <span data-ttu-id="6b621-136">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="6b621-136">Select **Save**.</span></span>

## <a name="importing-the-project-dependencies"></a><span data-ttu-id="6b621-137">Importar las dependencias del proyecto</span><span class="sxs-lookup"><span data-stu-id="6b621-137">Importing the project dependencies</span></span>

1. <span data-ttu-id="6b621-138">Clone este repositorio ([Ejemplo de conexión de Office 365 para iOS con el SDK de Microsoft Graph](https://github.com/microsoftgraph/ios-swift-connect-rest-sample)).</span><span class="sxs-lookup"><span data-stu-id="6b621-138">Clone this repository, [Office 365 Connect Sample for iOS Using the Microsoft Graph SDK](https://github.com/microsoftgraph/ios-swift-connect-rest-sample).</span></span> 


2. <span data-ttu-id="6b621-139">Use CocoaPods para importar las dependencias de PromiseKit.</span><span class="sxs-lookup"><span data-stu-id="6b621-139">Use CocoaPods to import the PromiseKit dependencies.</span></span> <span data-ttu-id="6b621-140">Esta aplicación de ejemplo ya contiene un podfile que recibirá los pods en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="6b621-140">This sample app already contains a podfile that will get the pods into the project.</span></span> <span data-ttu-id="6b621-141">Vaya a la carpeta raíz del proyecto en la aplicación **Terminal** y, desde **Terminal**, ejecute lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6b621-141">Navigate to the root folder of the project in the **Terminal** app, and from **Terminal** run:</span></span>

        pod install

   <span data-ttu-id="6b621-p107">Recibirá la confirmación de la importación de los pods al proyecto. Para obtener más información, vea [CocoaPods](https://guides.cocoapods.org/using/using-cocoapods.html)</span><span class="sxs-lookup"><span data-stu-id="6b621-p107">You will receive confirmation that the pods have been imported into the project. For more information, see [CocoaPods](https://guides.cocoapods.org/using/using-cocoapods.html)</span></span>

## <a name="install-the-msal-authentication-framework"></a><span data-ttu-id="6b621-144">Instalación del marco de autenticación de MSAL</span><span class="sxs-lookup"><span data-stu-id="6b621-144">Install the MSAL authentication framework</span></span>

<span data-ttu-id="6b621-145">La versión preliminar de MSAL se distribuye como archivos de símbolos y encabezado con Carthage.</span><span class="sxs-lookup"><span data-stu-id="6b621-145">The preview version of MSAL is distributed as header and symbol files using Carthage.</span></span> <span data-ttu-id="6b621-146">Para instalar MSAL en el proyecto, siga este procedimiento:</span><span class="sxs-lookup"><span data-stu-id="6b621-146">To install MSAL in the project, do these steps:</span></span>

1. <span data-ttu-id="6b621-147">Abra el terminal Bash y vaya a la carpeta raíz de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6b621-147">Open the Bash terminal and go to the app root folder.</span></span>
2. <span data-ttu-id="6b621-148">Cree un **cartfile**: copie `echo "github \"AzureAD/microsoft-authentication-library-for-objc\" \"master\"" > Cartfile` en el terminal y ejecute el comando.</span><span class="sxs-lookup"><span data-stu-id="6b621-148">Create a **cartfile**: Copy `echo "github \"AzureAD/microsoft-authentication-library-for-objc\" \"master\"" > Cartfile`  into the terminal and run the command.</span></span>
3. <span data-ttu-id="6b621-149">Compile la biblioteca de MSAL: copie `carthage update` en el terminal y ejecute el comando.</span><span class="sxs-lookup"><span data-stu-id="6b621-149">Build the MSAL library: Copy `carthage update` into the terminal and run the command.</span></span>


## <a name="enable-keychain-sharing"></a><span data-ttu-id="6b621-150">Habilitar el uso compartido de cadenas de claves</span><span class="sxs-lookup"><span data-stu-id="6b621-150">Enable keychain sharing</span></span>
 
<span data-ttu-id="6b621-p109">Para Xcode8, tendrá que agregar el grupo de cadenas de claves; de lo contrario, la aplicación no podrá obtener acceso a la cadena de claves. Para agregar el grupo de cadenas de claves:</span><span class="sxs-lookup"><span data-stu-id="6b621-p109">For Xcode8, you need to add the keychain group or your app will fail to access keychain. To add the keychain group:</span></span>
 
1. <span data-ttu-id="6b621-153">Seleccione el proyecto en el panel del administrador de proyectos de Xcode.</span><span class="sxs-lookup"><span data-stu-id="6b621-153">Select the project on the project manager panel in XCode.</span></span> <span data-ttu-id="6b621-154">(⌘ + 1).</span><span class="sxs-lookup"><span data-stu-id="6b621-154">(⌘ + 1).</span></span>
 
2. <span data-ttu-id="6b621-155">Seleccione el destino **O365-iOS-Microsoft-Graph-Connect-swift**.</span><span class="sxs-lookup"><span data-stu-id="6b621-155">Select the **O365-iOS-Microsoft-Graph-Connect-swift** target.</span></span>

3. <span data-ttu-id="6b621-156">En la pestaña **General**, en la sección **Firma**, asegúrese de que la casilla **Administrar automáticamente la firma** esté activada y que tenga un certificado de firma válido.</span><span class="sxs-lookup"><span data-stu-id="6b621-156">On the **General** tab and **Signing** section, verify that **Automatically manage signing** is checked and you have a valid signing certificate.</span></span>
 
3. <span data-ttu-id="6b621-157">En la pestaña **Funciones**, habilite la opción **Uso compartido de la cadena de claves**.</span><span class="sxs-lookup"><span data-stu-id="6b621-157">On the **Capabilities** tab, enable **Keychain Sharing**.</span></span>
 
4. <span data-ttu-id="6b621-158">Si **com.microsoft.O365-iOS-Microsoft-Graph-Connect-Swift-REST** no está en la lista de grupos de cadenas de claves, agréguelo.</span><span class="sxs-lookup"><span data-stu-id="6b621-158">If **com.microsoft.O365-iOS-Microsoft-Graph-Connect-Swift-REST** is not in the list of Keychain Groups, add it.</span></span>

## <a name="authenticating-with-microsoft-graph"></a><span data-ttu-id="6b621-159">Autenticación con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="6b621-159">Authenticating with Microsoft Graph</span></span>

<span data-ttu-id="6b621-160">El flujo de trabajo de la interfaz de usuario es el siguiente: la aplicación pide al usuario que se autentique.</span><span class="sxs-lookup"><span data-stu-id="6b621-160">The UI workflow is as follows: The app asks the user to authenticate.</span></span> <span data-ttu-id="6b621-161">Después de la autenticación, el usuario puede enviar un correo a otro usuario.</span><span class="sxs-lookup"><span data-stu-id="6b621-161">After authentication, the user can send a mail to another user.</span></span> <span data-ttu-id="6b621-162">Para realizar solicitudes con Microsoft Graph, en el ejemplo se usa la biblioteca de autenticación de **MSAL** para autenticar solicitudes HTTPS con un token de portador de OAuth 2.0 adecuado.</span><span class="sxs-lookup"><span data-stu-id="6b621-162">To make requests against Microsoft Graph, the sample uses the **MSAL** authentication library to authenticate HTTPS requests with an appropriate OAuth 2.0 bearer token.</span></span> <span data-ttu-id="6b621-163">En el proyecto de ejemplo, la clase **AuthenticationClass.swift**</span><span class="sxs-lookup"><span data-stu-id="6b621-163">In the sample project the **AuthenticationClass.swift.**</span></span> <span data-ttu-id="6b621-164">importa la biblioteca de **MSAL** y adquiere el token de acceso necesario para las operaciones de REST de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="6b621-164">class imports the **MSAL** library and acquires the access token needed for Microsoft Graph REST operations.</span></span>

1. <span data-ttu-id="6b621-165">Abra el área de trabajo del proyecto de **Xcode** (**Graph-iOS-Swift-Connect.xcworkspace**) y abra el archivo de clase **AuthenticationClass.swift**. Busque el código siguiente en esa clase.</span><span class="sxs-lookup"><span data-stu-id="6b621-165">Open the **XCode** project workspace (**Graph-iOS-Swift-Connect.xcworkspace**), and open the class file **AuthenticationClass.swift** Find the following code in that class.</span></span>


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


2. <span data-ttu-id="6b621-166">Llamaremos a la función **connectToGraph** desde **ConnectViewController.swift**.</span><span class="sxs-lookup"><span data-stu-id="6b621-166">We'll call the **connectToGraph** function from **ConnectViewController.swift**.</span></span> <span data-ttu-id="6b621-167">Este controlador es la vista predeterminada que la aplicación carga con un único botón denominado **Conectar** que el usuario pulsa para iniciar la autenticación.</span><span class="sxs-lookup"><span data-stu-id="6b621-167">This controller is the default view that the app loads with a single button named **Connect** that the user taps to start authenticating.</span></span> 

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

## <a name="send-an-email-with-microsoft-graph"></a><span data-ttu-id="6b621-168">Enviar un correo electrónico con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="6b621-168">Send an email with Microsoft Graph</span></span>

<span data-ttu-id="6b621-169">Después de conectar al usuario con Microsoft Graph, el ejemplo obtiene la dirección de correo electrónico, el nombre para mostrar y la foto de perfil del usuario autenticado.</span><span class="sxs-lookup"><span data-stu-id="6b621-169">After connecting the user to Microsoft Graph, the sample gets the authenticated user's email address, display name, and profile photo.</span></span> <span data-ttu-id="6b621-170">En el ejemplo, se carga la foto de perfil en la carpeta raíz de la cuenta de OneDrive del usuario y se solicita a OneDrive la URL para compartir de la imagen.</span><span class="sxs-lookup"><span data-stu-id="6b621-170">The sample uploads the profile photo to the user's OneDrive root folder and asks OneDrive for the sharing Url of the picture.</span></span> <span data-ttu-id="6b621-171">Por último, en el ejemplo se publica una solicitud REST a Microsoft Graph para enviar un mensaje de correo a la dirección de correo electrónico especificada.</span><span class="sxs-lookup"><span data-stu-id="6b621-171">Finally, the sample posts a REST request to Microsoft Graph to send a mail message to the provided email address.</span></span> 

<span data-ttu-id="6b621-172">El cuerpo del mensaje contiene el vínculo de uso compartido de imágenes y la imagen en sí como un archivo de imagen adjunto.</span><span class="sxs-lookup"><span data-stu-id="6b621-172">The message body contains the picture sharing link and the picture itself as an attached image file.</span></span> <span data-ttu-id="6b621-173">El destinatario predeterminado es el usuario autenticado, pero el ejemplo permite al usuario especificar la dirección de correo electrónico de cualquier otro usuario.</span><span class="sxs-lookup"><span data-stu-id="6b621-173">The default recipient is the authenticated user, but the sample allows the user to provide the email address of any other user.</span></span> 

<span data-ttu-id="6b621-174">El código con el que trabajaremos aquí está en la clase **SendMailViewController_WithPromise.swift**.</span><span class="sxs-lookup"><span data-stu-id="6b621-174">The code we'll work with here is in the class **SendMailViewController_WithPromise.swift.**</span></span> <span data-ttu-id="6b621-175">La función `viewDidLoad()` lee el valor `self.emailTextField.text` para obtener la dirección de correo electrónico del destinatario de correo y, después, inicia una **cadena de promesa** para obtener la imagen de perfil del usuario autenticado.</span><span class="sxs-lookup"><span data-stu-id="6b621-175">The `viewDidLoad()` function reads the `self.emailTextField.text` value to get the mail recipient's email address and then starts a **promise chain** to get the authenticated user's profile picture.</span></span> <span data-ttu-id="6b621-176">Si se rechaza la promesa, no se habilitará `sendMailButton`.</span><span class="sxs-lookup"><span data-stu-id="6b621-176">If the promise is rejected, the `sendMailButton` is not enabled.</span></span>

1. <span data-ttu-id="6b621-177">Abra **SendMailViewController_WithPromise.swift**</span><span class="sxs-lookup"><span data-stu-id="6b621-177">Open **SendMailViewController_WithPromise.swift.**</span></span> <span data-ttu-id="6b621-178">y busque la función `viewDidLoad`.</span><span class="sxs-lookup"><span data-stu-id="6b621-178">and find the `viewDidLoad` function.</span></span> <span data-ttu-id="6b621-179">Se llama a la función `self.userPictureWork` para iniciar la cadena de promesa.</span><span class="sxs-lookup"><span data-stu-id="6b621-179">The `self.userPictureWork` function is called to start the promise chain.</span></span>

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

   

1. <span data-ttu-id="6b621-180">Busque la función auxiliar de creación de solicitud del correo en la clase:</span><span class="sxs-lookup"><span data-stu-id="6b621-180">Find the mail request creation helper function in the class:</span></span>

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
2. <span data-ttu-id="6b621-181">Busque las siguientes funciones auxiliares para obtener la imagen de perfil del usuario, cargar la fotografía en OneDrive y solicitar un vínculo para compartir de la imagen:</span><span class="sxs-lookup"><span data-stu-id="6b621-181">Find the following helper functions for getting the user's profile picture,  uploading the photograph to OneDrive, and requesting a sharing link for the picture:</span></span>

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

3. <span data-ttu-id="6b621-182">Busque la siguiente función de envío de correo en la clase.</span><span class="sxs-lookup"><span data-stu-id="6b621-182">Find the following send mail function in the class.</span></span>  
 
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


## <a name="run-the-app"></a><span data-ttu-id="6b621-183">Ejecutar la aplicación</span><span class="sxs-lookup"><span data-stu-id="6b621-183">Run the app</span></span>
1. <span data-ttu-id="6b621-184">Antes de ejecutar el ejemplo, tendrá que proporcionar el id. de cliente que recibió del proceso de registro en la sección **Registrar la aplicación.**</span><span class="sxs-lookup"><span data-stu-id="6b621-184">Before running the sample you'll need to supply the client ID you received from the registration process in the section **Register the app.**</span></span> <span data-ttu-id="6b621-185">Abra **Info.plist** como código fuente.</span><span class="sxs-lookup"><span data-stu-id="6b621-185">Open **Info.plist** as source code.</span></span> 

   - <span data-ttu-id="6b621-186">Reemplace `ENTER_CLIENT_ID_HERE` por el **id. de cliente** del proceso de registro.</span><span class="sxs-lookup"><span data-stu-id="6b621-186">Replace  `ENTER_CLIENT_ID_HERE` with the **ClientID** from the registration process.</span></span> <span data-ttu-id="6b621-187">Asegúrese de no reemplazar `msal`.</span><span class="sxs-lookup"><span data-stu-id="6b621-187">Be sure that `msal` is not replaced.</span></span> <span data-ttu-id="6b621-188">Después de reemplazar la cadena, el valor de la cadena de la matriz es similar a `msal48d31887-5fad-4d73-a9f5-3c356e68a038`, donde la parte del GUID es **su** id. de cliente:</span><span class="sxs-lookup"><span data-stu-id="6b621-188">After you replace the string, the array string value looks like `msal48d31887-5fad-4d73-a9f5-3c356e68a038` where the GUID portion is **your** client Id:</span></span>  

   <span data-ttu-id="6b621-189">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="6b621-189">For example,</span></span> 

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

     <span data-ttu-id="6b621-190">se convierte en…</span><span class="sxs-lookup"><span data-stu-id="6b621-190">becomes...</span></span> 

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

> <span data-ttu-id="6b621-191">**Nota:** Verá que, en los siguientes ámbitos de permiso de configuración para este proyecto: `["https://graph.microsoft.com/Mail.ReadWrite","https://graph.microsoft.com/Mail.Send","https://graph.microsoft.com/Files.ReadWrite","https://graph.microsoft.com/User.ReadBasic.All"]`.</span><span class="sxs-lookup"><span data-stu-id="6b621-191">**Note:** You'll notice that the following permission scopes have been configured for this project: `["https://graph.microsoft.com/Mail.ReadWrite","https://graph.microsoft.com/Mail.Send","https://graph.microsoft.com/Files.ReadWrite","https://graph.microsoft.com/User.ReadBasic.All"]` .</span></span> <span data-ttu-id="6b621-192">Para realizar las llamadas de servicio usadas en este proyecto, enviar un correo a su cuenta de correo, recuperar parte de la información del perfil (nombre para mostrar, dirección de correo electrónico) y escribir en la carpeta raíz de la cuenta de OneDrive del usuario, se necesitan estos permisos para que la aplicación pueda ejecutarse sin que se produzcan errores de permisos.</span><span class="sxs-lookup"><span data-stu-id="6b621-192">The service calls used in this project, sending a mail to your mail account and retrieving some profile information (Display Name, Email Address), and writing to the user's OneDrive root require these permissions for the app to run without a permissions error.</span></span>

2. <span data-ttu-id="6b621-193">Ejecute el ejemplo, pulse **Conectar**, inicie sesión con su cuenta personal, profesional o educativa, y conceda los permisos solicitados.</span><span class="sxs-lookup"><span data-stu-id="6b621-193">Run the sample, tap **Connect,** sign in with your personal or work or school account, and grant the requested permissions.</span></span>

3. <span data-ttu-id="6b621-p120">Elija el botón **Enviar correo electrónico**. Cuando se envíe el correo, se mostrará un mensaje de operación correcta debajo del botón.</span><span class="sxs-lookup"><span data-stu-id="6b621-p120">Choose the **Send email** button. When the mail is sent, a success message is displayed below the button.</span></span>

## <a name="next-steps"></a><span data-ttu-id="6b621-196">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="6b621-196">Next steps</span></span>
- <span data-ttu-id="6b621-197">Pruebe la API de REST mediante el [Probador de Graph](https://graph.microsoft.io/graph-explorer).</span><span class="sxs-lookup"><span data-stu-id="6b621-197">Try out the REST API using the [Graph explorer](https://graph.microsoft.io/graph-explorer).</span></span>
- <span data-ttu-id="6b621-198">Busque ejemplos de operaciones comunes, tanto para REST como para SDK, en el [Ejemplo de fragmentos de código de Objective C para Microsoft Graph para iOS](https://github.com/microsoftgraph/ios-objectiveC-snippets-sample).</span><span class="sxs-lookup"><span data-stu-id="6b621-198">Find examples of common operations for SDK operations in the [Microsoft Graph iOS Objective C Snippets Sample](https://github.com/microsoftgraph/ios-objectiveC-snippets-sample).</span></span>

## <a name="see-also"></a><span data-ttu-id="6b621-199">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b621-199">See also</span></span>
- [<span data-ttu-id="6b621-200">Protocolos de Azure AD v2.0</span><span class="sxs-lookup"><span data-stu-id="6b621-200">Azure AD v2.0 protocols</span></span>](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-protocols/)
- [<span data-ttu-id="6b621-201">Tokens de Azure AD v2.0</span><span class="sxs-lookup"><span data-stu-id="6b621-201">Azure AD v2.0 tokens</span></span>](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-tokens/)
