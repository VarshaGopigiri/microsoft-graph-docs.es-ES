# <a name="get-started-with-microsoft-graph-in-an-ios-app"></a><span data-ttu-id="f7639-101">Introducción a Microsoft Graph en una aplicación de iOS</span><span class="sxs-lookup"><span data-stu-id="f7639-101">Get started with Microsoft Graph in an iOS App</span></span>

> <span data-ttu-id="f7639-p101">**¿Desea compilar aplicaciones para clientes empresariales?** Es posible que la aplicación no funcione si su cliente empresarial activa características de seguridad de movilidad empresarial como el <a href="https://azure.microsoft.com/en-us/documentation/articles/active-directory-conditional-access-device-policies/" target="_newtab">acceso condicional al dispositivo</a>. En casos así, es posible que no tenga constancia de esta activación y que sus clientes obtengan errores.</span><span class="sxs-lookup"><span data-stu-id="f7639-p101">**Building apps for enterprise customers?** Your app may not work if your enterprise customer turns on enterprise mobility security features like <a href="https://azure.microsoft.com/en-us/documentation/articles/active-directory-conditional-access-device-policies/" target="_newtab">conditional device access</a>. In this case, you may not know and your customers may experience errors.</span></span> 

> <span data-ttu-id="f7639-p102">Para admitir **todos los clientes empresariales** en **todos los escenarios de empresa**, deberá usar el punto de conexión de Azure AD y administrar las aplicaciones mediante el [Portal de administración de Azure](https://aka.ms/aadapplist). Para obtener más información, consulte [Decidir entre los puntos de conexión de Azure AD y Azure AD v2.0 ](../concepts/auth_overview.md#deciding-between-the-azure-ad-and-azure-ad-v20-endpoints).</span><span class="sxs-lookup"><span data-stu-id="f7639-p102">To support **all enterprise customers** across **all enterprise scenarios**, you must use the Azure AD endpoint and manage your apps using the [Azure Management Portal](https://aka.ms/aadapplist). For more information, see [Deciding between the Azure AD and Azure AD v2.0 endpoints](../concepts/auth_overview.md#deciding-between-the-azure-ad-and-azure-ad-v20-endpoints).</span></span>

<span data-ttu-id="f7639-p103">En este artículo se describen las tareas necesarias para obtener un token de acceso desde el punto de conexión de [Azure AD v2.0](https://developer.microsoft.com/en-us/graph/docs/concepts/converged_auth) y llamar a Microsoft Graph. Le guiará por el código del [Ejemplo Connect de Office 365 para iOS (SDK)](https://github.com/microsoftgraph/ios-objectivec-connect-sample) para explicar los conceptos principales que se deben implementar en una aplicación que use Microsoft Graph. Describe cómo obtener acceso a Microsoft Graph mediante el [SDK de Microsoft Graph para iOS](https://github.com/microsoftgraph/msgraph-sdk-ios).</span><span class="sxs-lookup"><span data-stu-id="f7639-p103">This article describes the tasks required to get an access token from the [Azure AD v2.0 endpoint](https://developer.microsoft.com/en-us/graph/docs/concepts/converged_auth) and call Microsoft Graph. It walks you through the code inside the [Office 365 Connect Sample for iOS (SDK)](https://github.com/microsoftgraph/ios-objectivec-connect-sample) to explain the main concepts that you have to implement in an app that uses Microsoft Graph. It describes how to access Microsoft Graph by using the [Microsoft Graph SDK for iOS](https://github.com/microsoftgraph/msgraph-sdk-ios).</span></span>

<span data-ttu-id="f7639-110">Puede descargar la versión de la aplicación que creará desde este repositorio de GitHub:</span><span class="sxs-lookup"><span data-stu-id="f7639-110">You can download the version of the app that you'll create from this GitHub repo:</span></span>

* [<span data-ttu-id="f7639-111">Ejemplo Connect de Office 365 para iOS con el SDK de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="f7639-111">Office 365 Connect Sample for iOS Using the Microsoft Graph SDK</span></span>](https://github.com/microsoftgraph/ios-objectivec-connect-sample)

<span data-ttu-id="f7639-112">En la imagen siguiente, se muestra la aplicación que va a crear.</span><span class="sxs-lookup"><span data-stu-id="f7639-112">The following image shows the app you'll create.</span></span>

![El tutorial de conexión de ejemplo, muestra cómo conectarse y enviar un correo en la aplicación.](./images/iOSConnectWalkthrough.png)


<span data-ttu-id="f7639-114">El flujo de trabajo será conectarse o autenticarse en Microsoft Graph, iniciar sesión con su cuenta personal o profesional y, por último, enviar un correo a un destinatario.</span><span class="sxs-lookup"><span data-stu-id="f7639-114">The workflow will be to connect/authenticate to Microsoft Graph, sign in with your work or personal account, and finally send a mail to a recipient.</span></span>

<span data-ttu-id="f7639-p104">**¿No desea compilar una aplicación?** Use el [inicio rápido de Microsoft Graph](https://graph.microsoft.io/en-us/getting-started) para ponerlo todo en funcionamiento de manera rápida.</span><span class="sxs-lookup"><span data-stu-id="f7639-p104">**Don't feel like building an app?** Use the [Microsoft Graph quick start](https://graph.microsoft.io/en-us/getting-started) to get up and running fast.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f7639-117">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f7639-117">Prerequisites</span></span>

<span data-ttu-id="f7639-118">Para comenzar, necesitará:</span><span class="sxs-lookup"><span data-stu-id="f7639-118">To get started, you'll need:</span></span> 

* <span data-ttu-id="f7639-119">[Xcode](https://developer.apple.com/xcode/downloads/) de Apple</span><span class="sxs-lookup"><span data-stu-id="f7639-119">[Xcode](https://developer.apple.com/xcode/downloads/) from Apple</span></span>
* <span data-ttu-id="f7639-120">La instalación de [CocoaPods](https://guides.cocoapods.org/using/using-cocoapods.html) como administrador de dependencias.</span><span class="sxs-lookup"><span data-stu-id="f7639-120">Installation of [CocoaPods](https://guides.cocoapods.org/using/using-cocoapods.html) as a dependency manager</span></span>
* <span data-ttu-id="f7639-121">Una [cuenta Microsoft](https://www.outlook.com/) o una [cuenta profesional o educativa](http://dev.office.com/devprogram)</span><span class="sxs-lookup"><span data-stu-id="f7639-121">A [Microsoft account](https://www.outlook.com/) or a [work or school account](http://dev.office.com/devprogram)</span></span>
* <span data-ttu-id="f7639-p105">[Proyecto inicial de Microsoft Graph para iOS](https://github.com/microsoftgraph/ios-objectivec-connect-sample). Esta plantilla contiene clases a las que agregará código. Para obtener este proyecto, clone o descargue el proyecto de ejemplo desde esta ubicación y trabajará con el área de trabajo de la carpeta **starter-project** (**O365-iOS-Microsoft-Graph-SDK.xcworkspace**).</span><span class="sxs-lookup"><span data-stu-id="f7639-p105">The [Microsoft Graph Starter Project for iOS](https://github.com/microsoftgraph/ios-objectivec-connect-sample). This template contains classes that you'll add code to. To get this project, clone or download the sample project from this location, and you'll work with the workspace inside the **starter-project** folder (**O365-iOS-Microsoft-Graph-SDK.xcworkspace**).</span></span>

## <a name="register-the-app"></a><span data-ttu-id="f7639-125">Registrar la aplicación</span><span class="sxs-lookup"><span data-stu-id="f7639-125">Register the app</span></span>
 
1. <span data-ttu-id="f7639-126">Inicie sesión en el [Portal de registro de aplicaciones](https://apps.dev.microsoft.com/) mediante su cuenta personal, profesional o educativa.</span><span class="sxs-lookup"><span data-stu-id="f7639-126">Sign into the [App Registration Portal](https://apps.dev.microsoft.com/) using either your personal or work or school account.</span></span>
2. <span data-ttu-id="f7639-127">Seleccione **Agregar una aplicación**.</span><span class="sxs-lookup"><span data-stu-id="f7639-127">Select **Add an app**.</span></span>
3. <span data-ttu-id="f7639-128">Escriba un nombre para la aplicación y seleccione **Crear aplicación**.</span><span class="sxs-lookup"><span data-stu-id="f7639-128">Enter a name for the app, and select **Create application**.</span></span>
    
    <span data-ttu-id="f7639-129">Se muestra la página de registro, indicando las propiedades de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f7639-129">The registration page displays, listing the properties of your app.</span></span>
 
4. <span data-ttu-id="f7639-130">En **Plataformas**, seleccione **Agregar plataforma**.</span><span class="sxs-lookup"><span data-stu-id="f7639-130">Under **Platforms**, select **Add platform**.</span></span>
5. <span data-ttu-id="f7639-131">Seleccione **Plataforma móvil**.</span><span class="sxs-lookup"><span data-stu-id="f7639-131">Select **Mobile platform**.</span></span>
6. <span data-ttu-id="f7639-p106">Copie el identificador de cliente en el Portapapeles. Deberá escribir este valor en la aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f7639-p106">Copy the Client Id to the clipboard. You'll need to enter this value into the sample app.</span></span>

    <span data-ttu-id="f7639-134">El id. de la aplicación es un identificador único para su aplicación.</span><span class="sxs-lookup"><span data-stu-id="f7639-134">The app id is a unique identifier for your app.</span></span> 

7. <span data-ttu-id="f7639-135">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="f7639-135">Select **Save**.</span></span>

## <a name="importing-the-project-dependencies"></a><span data-ttu-id="f7639-136">Importar las dependencias del proyecto</span><span class="sxs-lookup"><span data-stu-id="f7639-136">Importing the project dependencies</span></span>

1. <span data-ttu-id="f7639-p107">Clone este repositorio ([Ejemplo Connect de Office 365 para iOS con el SDK de Microsoft Graph](https://github.com/microsoftgraph/ios-objectivec-connect-sample)). **Recuerde que usará el ejemplo de la carpeta starter-project y no el ejemplo de la raíz del proyecto.**</span><span class="sxs-lookup"><span data-stu-id="f7639-p107">Clone this repository, [Office 365 Connect Sample for iOS Using the Microsoft Graph SDK](https://github.com/microsoftgraph/ios-objectivec-connect-sample). **Remember you will use the sample in the starter-project folder and not the sample at the root of the project.**</span></span>
2. <span data-ttu-id="f7639-p108">Use CocoaPods para importar el SDK de Microsoft Graph y las dependencias de autenticación. Esta aplicación de ejemplo ya contiene un podfile que recibirá los pods en el proyecto. Vaya a la carpeta **starter-project** de la aplicación **Terminal** y, desde **Terminal**, ejecute lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f7639-p108">Use CocoaPods to import the Microsoft Graph SDK and authentication dependencies. This sample app already contains a podfile that will get the pods into the project. Navigate to the folder **starter-project** in the **Terminal** app, and from **Terminal** run:</span></span>

        pod install

   <span data-ttu-id="f7639-p109">Recibirá la confirmación de la importación de los pods al proyecto. Para obtener más información, consulte [CocoaPods](https://guides.cocoapods.org/using/using-cocoapods.html).</span><span class="sxs-lookup"><span data-stu-id="f7639-p109">You will receive confirmation that the pods have been imported into the project. For more information, see [CocoaPods](https://guides.cocoapods.org/using/using-cocoapods.html)</span></span>


## <a name="enable-keychain-sharing"></a><span data-ttu-id="f7639-144">Habilitar el uso compartido de cadenas de claves</span><span class="sxs-lookup"><span data-stu-id="f7639-144">Enable keychain sharing</span></span>
 
<span data-ttu-id="f7639-p110">Para Xcode 8, deberá agregar el grupo de cadenas de claves o la aplicación no podrá obtener acceso a la cadena de claves. Para agregar el grupo de cadenas de claves:</span><span class="sxs-lookup"><span data-stu-id="f7639-p110">For Xcode8, you need to add the keychain group or your app will fail to access keychain. To add the keychain group:</span></span>
 
1. <span data-ttu-id="f7639-p111">Seleccione el proyecto en el panel de administración de proyectos de Xcode. (⌘ + 1).</span><span class="sxs-lookup"><span data-stu-id="f7639-p111">Select the project on the project manager panel in Xcode. (⌘ + 1).</span></span>
 
2. <span data-ttu-id="f7639-149">Seleccione **O365-iOS-Microsoft-Graph-SDK**.</span><span class="sxs-lookup"><span data-stu-id="f7639-149">Select **O365-iOS-Microsoft-Graph-SDK**.</span></span>
 
3. <span data-ttu-id="f7639-150">En la pestaña Funcionalidad, habilite **Uso compartido de cadenas de claves**.</span><span class="sxs-lookup"><span data-stu-id="f7639-150">On the Capabilities tab, enable **Keychain Sharing**.</span></span>
 
4. <span data-ttu-id="f7639-151">Agregue **com.microsoft.O365-iOS-Microsoft-Graph-SDK** a los grupos de cadenas de claves.</span><span class="sxs-lookup"><span data-stu-id="f7639-151">Add **com.microsoft.O365-iOS-Microsoft-Graph-SDK** to the Keychain Groups.</span></span>
 

## <a name="authenticating-with-microsoft-graph"></a><span data-ttu-id="f7639-152">Autenticación con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="f7639-152">Authenticating with Microsoft Graph</span></span>

<span data-ttu-id="f7639-p112">Para volver a visitar el flujo de trabajo de la interfaz de usuario, la aplicación va a solicitar al usuario que se autentique y, a continuación, este podrá enviar un correo al usuario especificado. Para realizar solicitudes en el servicio Microsoft Graph, se debe proporcionar un proveedor de autenticación que sea capaz de autenticar solicitudes HTTPS con un token de portador OAuth 2.0 adecuado. En el proyecto de ejemplo, hay una clase de autenticación que ya tiene código auxiliar que se llama **AuthenticationProvider.m.** Agregaremos una función para solicitar (y adquirir) un token de acceso para llamar a la API de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="f7639-p112">To revisit the UI workflow, the app is going to have the user authenticate, and then they'll have the ability to send a mail to a specified user. To make requests against the Microsoft Graph service, an authentication provider must be supplied which is capable of authenticating HTTPS requests with an appropriate OAuth 2.0 bearer token. In the sample project there's an authentication class already stubbed out called **AuthenticationProvider.m.** We will add a function to request, and acquire, an access token for calling the Microsoft Graph API.</span></span> 

1. <span data-ttu-id="f7639-p113">Abra el área de trabajo del proyecto Xcode (**O365-iOS-Microsoft-Graph-SDK.xcworkspace**) de la carpeta **starter-project** y vaya a la carpeta **Authentication** para abrir el archivo **AuthenticationProvider.m.** Agregue el código siguiente a esa clase.</span><span class="sxs-lookup"><span data-stu-id="f7639-p113">Open the Xcode project workspace (**O365-iOS-Microsoft-Graph-SDK.xcworkspace**) in the **starter-project** folder, and navigate to the **Authentication** folder and open the file **AuthenticationProvider.m.** Add the following code to that class.</span></span>

        -(void) connectToGraphWithClientId:(NSString *)clientId scopes:(NSArray *)scopes completion:(void (^)   (NSError *))completion{
            [NXOAuth2AuthenticationProvider setClientId:kClientId
                                              scopes:scopes];
    
    
            /**
            Obtains access token by performing login with UI, where viewController specifies the parent view controller.
            @param viewController The view controller to present the UI on.
             @param completionHandler The completion handler to be called when the authentication has completed.
            error should be non nil if there was no error, and should contain any error(s) that occurred.
             */

                if ([[NXOAuth2AuthenticationProvider sharedAuthProvider] loginSilent]) {
                completion(nil);
                }
                else {
                    [[NXOAuth2AuthenticationProvider sharedAuthProvider] loginWithViewController:nil completion:^(NSError *error) {
                    if (!error) {
                    NSLog(@"Authentication successful.");
                    completion(nil);
                    }
                 else {
                     NSLog(@"Authentication failed - %@", error.localizedDescription);
                    completion(error);
                    }
                }];
            }
    
        }

2. <span data-ttu-id="f7639-p114">A continuación, agregue el método al archivo de encabezado. Abra el archivo **AuthenticationProvider.h** y agregue el código siguiente a esta clase.</span><span class="sxs-lookup"><span data-stu-id="f7639-p114">Next add the method to the header file. Open the file **AuthenticationProvider.h** and add the following code to this class.</span></span>

        -(void) connectToGraphWithClientId:(NSString *)clientId
                            scopes:(NSArray *)scopes
                        completion:(void (^)(NSError *error))completion;



2. <span data-ttu-id="f7639-p115">Por último, llamaremos a este método desde **ConnectViewController.m**. Este controlador es la vista predeterminada que carga la aplicación y hay un único botón denominado **Conectar** que el usuario pulsará para iniciar el proceso de autenticación. Este método toma dos parámetros, el **Id. de cliente** y los **ámbitos**, que trataremos con más detalle a continuación. Agregue la siguiente acción a **ConnectViewController.m**.</span><span class="sxs-lookup"><span data-stu-id="f7639-p115">Finally we'll call this method from **ConnectViewController.m**. This controller is the default view that the app loads, and there is a single button named **Connect** that the user will tap that will initiate the authentication process. This method takes in two parameters, the **Client ID** and **scopes**, we'll discuss these in more detail below. Add the following action to **ConnectViewController.m**.</span></span>

        - (IBAction)connectTapped:(id)sender {
            [self showLoadingUI:YES];   
            NSArray *scopes = [kScopes componentsSeparatedByString:@","];
            [self.authProvider connectToGraphWithClientId:kClientId scopes:scopes completion:^(NSError *error) {
                if (!error) {
                    [self performSegueWithIdentifier:@"showSendMail" sender:nil];
                    [self showLoadingUI:NO];
                    NSLog(@"Authentication successful.");
                    }
                else{
                    NSLog(NSLocalizedString(@"CHECK_LOG_ERROR", error.localizedDescription));
                    [self showLoadingUI:NO];
                    };
                }];
        }

## <a name="send-an-email-with-microsoft-graph"></a><span data-ttu-id="f7639-165">Enviar un correo electrónico con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="f7639-165">Send an email with Microsoft Graph</span></span>

<span data-ttu-id="f7639-p116">Después de configurar el proyecto para que pueda autenticar, las siguientes tareas corresponderán al envío de un correo a un usuario mediante la API de Microsoft Graph. De forma predeterminada, el usuario que inició sesión será el destinatario, pero tiene la posibilidad de cambiarlo a cualquier otro destinatario. El código con el que trabajaremos aquí está ubicado en la carpeta **Controllers** y en la clase **SendMailViewController.m.** Verá que aquí hay otro código representado para la interfaz de usuario y un método auxiliar para recuperar la información del perfil del usuario desde el servicio Microsoft Graph. Nos concentraremos en los métodos para crear un mensaje de correo y enviarlo.</span><span class="sxs-lookup"><span data-stu-id="f7639-p116">After configuring the project to be able to authenticate, the next tasks are sending a mail to a user using the Microsoft Graph API. By default the logged in user will be the recipient, but you have the ability to change it to any other recipient. The code we'll work with here is located in the **Controllers** folder and in the class **SendMailViewController.m.** You'll see that there is other code represented here for the UI, and a helper method to retrieve user profile information from the Microsoft Graph service. We'll concentrate on the methods for creating a mail message and sending that message.</span></span>

1. <span data-ttu-id="f7639-p117">Abra el archivo **SendMailViewController.m.** de la carpeta Controllers y agregue el siguiente método auxiliar a la clase:</span><span class="sxs-lookup"><span data-stu-id="f7639-p117">Open **SendMailViewController.m.** in the Controllers folder and add the following helper method to the class:</span></span>

        // Create a sample test message to send to specified user account
        -(MSGraphMessage*) getSampleMessage{
            MSGraphMessage *message = [[MSGraphMessage alloc]init];
            MSGraphRecipient *toRecipient = [[MSGraphRecipient alloc]init];
            MSGraphEmailAddress *email = [[MSGraphEmailAddress alloc]init];
    
            email.address = self.emailAddress;
            toRecipient.emailAddress = email;
    
            NSMutableArray *toRecipients = [[NSMutableArray alloc]init];
            [toRecipients addObject:toRecipient];
    
            message.subject = NSLocalizedString(@"MAIL_SUBJECT", comment: "");
    
            MSGraphItemBody *emailBody = [[MSGraphItemBody alloc]init];
            NSString *htmlContentPath = [[NSBundle mainBundle] pathForResource:@"EmailBody" ofType:@"html"];
            NSString *htmlContentString = [NSString stringWithContentsOfFile:htmlContentPath encoding:NSUTF8StringEncoding error:nil];
    
            emailBody.content = htmlContentString;
            emailBody.contentType = [MSGraphBodyType html];
            message.body = emailBody;
    
            message.toRecipients = toRecipients;
    
            return message;
    
        }


2. <span data-ttu-id="f7639-p118">Abra el archivo **SendMailViewController.m.** Agregue a la clase el siguiente método para enviar correo.</span><span class="sxs-lookup"><span data-stu-id="f7639-p118">Open **SendMailViewController.m.** Add the following send mail method to the class.</span></span>  

        //Send mail to the specified user in the email text field
        -(void) sendMail {   
            MSGraphMessage *message = [self getSampleMessage];
            MSGraphUserSendMailRequestBuilder *requestBuilder = [[self.graphClient me]sendMailWithMessage:message saveToSentItems:true];
            NSLog(@"%@", requestBuilder);
            MSGraphUserSendMailRequest *mailRequest = [requestBuilder request];
            [mailRequest executeWithCompletion:^(NSDictionary *response, NSError *error) {
                if(!error){
                    NSLog(@"response %@", response);
                    NSLog(NSLocalizedString(@"ERROR", ""), error.localizedDescription);
            
                    dispatch_async(dispatch_get_main_queue(), ^{
                        self.statusTextView.text = NSLocalizedString(@"SEND_SUCCESS", comment: "");
                });
            }
            else {
                NSLog(NSLocalizedString(@"ERROR", ""), error.localizedDescription);
                self.statusTextView.text = NSLocalizedString(@"SEND_FAILURE", comment: "");
                }
            }];
    
        }

<span data-ttu-id="f7639-p119">Así, **getSampleMessage** creará un borrador HTML de ejemplo para usar con fines de demostración. A continuación, el siguiente método, **sendMail**, toma ese mensaje y ejecuta la solicitud de enviarlo. Una vez más, el destinatario predeterminado es el usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="f7639-p119">So **getSampleMessage** creates a draft HTML sample mail to use for demo purposes. The next method, **sendMail**, then takes that message and executes the request to send it. Again the default recipient is the signed-in user.</span></span>


## <a name="run-the-app"></a><span data-ttu-id="f7639-178">Ejecutar la aplicación</span><span class="sxs-lookup"><span data-stu-id="f7639-178">Run the app</span></span>
1. <span data-ttu-id="f7639-p120">Antes de ejecutar el ejemplo, deberá proporcionar el identificador de cliente que recibió del proceso de registro en la sección **Registrar la aplicación.** Abra el archivo **AuthenticationConstants.m** de la carpeta **Application**. Verá que el ClientID del proceso de registro se puede agregar a la parte superior del archivo:</span><span class="sxs-lookup"><span data-stu-id="f7639-p120">Before running the sample you'll need to supply the client ID you received from the registration process in the section **Register the app.** Open **AuthenticationConstants.m** under the **Application** folder. You'll see that the ClientID from the registration process can be added to the top of the file.:</span></span>  

        // You will set your application's clientId
        NSString * const kClientId    = @"ENTER_CLIENT_ID_HERE";
        NSString * const kScopes = @"https://graph.microsoft.com/Mail.Send, https://graph.microsoft.com/User.Read, offline_access";
<span data-ttu-id="f7639-p121">Nota: Observará que se han configurado los siguientes ámbitos de permiso para este proyecto: **"https://graph.microsoft.com/Mail.Send", "https://graph.microsoft.com/User.Read", "offline_access"**. Las llamadas de servicio usadas en este proyecto, el envío de un correo a su cuenta de correo y la recuperación de parte de la información de perfil (nombre para mostrar, dirección de correo electrónico) requieren estos permisos para que la aplicación se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="f7639-p121">Note: You'll notice that the following permission scopes have been configured for this project: **"https://graph.microsoft.com/Mail.Send", "https://graph.microsoft.com/User.Read", "offline_access"**. The service calls used in this project, sending a mail to your mail account and retrieving some profile information (Display Name, Email Address) require these permissions for the app to run properly.</span></span>

2. <span data-ttu-id="f7639-184">Ejecute el ejemplo, pulse **Conectar**, inicie sesión con su cuenta personal, profesional o educativa y conceda los permisos solicitados.</span><span class="sxs-lookup"><span data-stu-id="f7639-184">Run the sample, tap **Connect,** sign in with your personal or work or school account, and grant the requested permissions.</span></span>

3. <span data-ttu-id="f7639-p122">Elija el botón **Enviar correo electrónico**. Cuando se envíe el correo, se mostrará un mensaje de operación correcta debajo del botón.</span><span class="sxs-lookup"><span data-stu-id="f7639-p122">Choose the **Send email** button. When the mail is sent, a success message is displayed below the button.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f7639-187">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="f7639-187">Next steps</span></span>
- <span data-ttu-id="f7639-188">Pruebe la API de REST mediante el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).</span><span class="sxs-lookup"><span data-stu-id="f7639-188">Try out the REST API using the [Graph explorer](https://developer.microsoft.com/graph/graph-explorer).</span></span>
- <span data-ttu-id="f7639-189">Busque ejemplos de operaciones comunes tanto para REST como para SDK en el [Ejemplo de fragmentos de código de Objective C para Microsoft Graph para iOS](https://github.com/microsoftgraph/ios-objectiveC-snippets-sample). </span><span class="sxs-lookup"><span data-stu-id="f7639-189">Find examples of common operations for both REST and SDK operations in the [Microsoft Graph iOS Objective C Snippets Sample](https://github.com/microsoftgraph/ios-objectiveC-snippets-sample).</span></span>

## <a name="see-also"></a><span data-ttu-id="f7639-190">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f7639-190">See also</span></span>
- [<span data-ttu-id="f7639-191">SDK de Microsoft Graph para iOS</span><span class="sxs-lookup"><span data-stu-id="f7639-191">Microsoft Graph SDK for iOS</span></span>](https://github.com/microsoftgraph/msgraph-sdk-ios)
- [<span data-ttu-id="f7639-192">Protocolos de Azure AD v2.0</span><span class="sxs-lookup"><span data-stu-id="f7639-192">Azure AD v2.0 protocols</span></span>](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-protocols/)
- [<span data-ttu-id="f7639-193">Tokens de Azure AD v2.0</span><span class="sxs-lookup"><span data-stu-id="f7639-193">Azure AD v2.0 tokens</span></span>](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-tokens/)
