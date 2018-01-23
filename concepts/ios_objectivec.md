# <a name="get-started-with-microsoft-graph-in-an-objectve-c-ios-app"></a><span data-ttu-id="e4029-101">Introducción a Microsoft Graph en una aplicación de Objective C de iOS</span><span class="sxs-lookup"><span data-stu-id="e4029-101">Get started with Microsoft Graph in an Objectve C iOS App</span></span>

> <span data-ttu-id="e4029-p101">**¿Desea compilar aplicaciones para clientes empresariales?** Es posible que la aplicación no funcione si su cliente empresarial activa características de seguridad de movilidad empresarial como el <a href="https://azure.microsoft.com/en-us/documentation/articles/active-directory-conditional-access-device-policies/" target="_newtab">acceso condicional al dispositivo</a>. En casos así, es posible que no tenga constancia de esta activación y que sus clientes obtengan errores.</span><span class="sxs-lookup"><span data-stu-id="e4029-p101">**Building apps for enterprise customers?** Your app may not work if your enterprise customer turns on enterprise mobility security features like <a href="https://azure.microsoft.com/en-us/documentation/articles/active-directory-conditional-access-device-policies/" target="_newtab">conditional device access</a>. In this case, you may not know and your customers may experience errors.</span></span> 

> <span data-ttu-id="e4029-p102">Para ser compatible con **todos los clientes empresariales** en **todos los escenarios de empresa**, tiene que usar el punto de conexión de AD de Azure y administrar las aplicaciones mediante [Azure Portal](https://aka.ms/aadapplist). Para más información, vea [Decidir entre los puntos de conexión de Azure AD y Azure AD v2.0](../concepts/auth_overview.md#deciding-between-the-azure-ad-and-azure-ad-v20-endpoints).</span><span class="sxs-lookup"><span data-stu-id="e4029-p102">To support **all enterprise customers** across **all enterprise scenarios**, you must use the Azure AD endpoint and manage your apps using the [Azure Management Portal](https://aka.ms/aadapplist). For more information, see [Deciding between the Azure AD and Azure AD v2.0 endpoints](../concepts/auth_overview.md#deciding-between-the-azure-ad-and-azure-ad-v20-endpoints).</span></span>

<span data-ttu-id="e4029-p103">En este artículo se describen las tareas necesarias para obtener un token de acceso desde el punto de conexión de [Azure AD v2.0](https://developer.microsoft.com/es-ES/graph/docs/concepts/converged_auth) y llamar a Microsoft Graph. Le guiará por el código del [Ejemplo Connect de Office 365 para iOS (SDK)](https://github.com/microsoftgraph/ios-objectivec-connect-sample) para explicar los conceptos principales que se deben implementar en una aplicación que use Microsoft Graph. Describe cómo obtener acceso a Microsoft Graph mediante el [SDK de Microsoft Graph para iOS](https://github.com/microsoftgraph/msgraph-sdk-ios).</span><span class="sxs-lookup"><span data-stu-id="e4029-p103">This article describes the tasks required to get an access token from the [Azure AD v2.0 endpoint](https://developer.microsoft.com/es-ES/graph/docs/concepts/converged_auth) and call Microsoft Graph. It walks you through the code inside the [Office 365 Connect Sample for iOS (SDK)](https://github.com/microsoftgraph/ios-objectivec-connect-sample) to explain the main concepts that you have to implement in an app that uses Microsoft Graph. It describes how to access Microsoft Graph by using the [Microsoft Graph SDK for iOS](https://github.com/microsoftgraph/msgraph-sdk-ios).</span></span>

<span data-ttu-id="e4029-110">Puede descargar la versión de la aplicación que creará desde este repositorio de GitHub:</span><span class="sxs-lookup"><span data-stu-id="e4029-110">You can download the version of the app that you'll create from this GitHub repo:</span></span>

* [<span data-ttu-id="e4029-111">Ejemplo Connect de Office 365 para iOS con el SDK de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="e4029-111">Office 365 Connect Sample for iOS Using the Microsoft Graph SDK</span></span>](https://github.com/microsoftgraph/ios-objectivec-connect-sample)

<span data-ttu-id="e4029-112">En la imagen siguiente, se muestra la aplicación que va a crear.</span><span class="sxs-lookup"><span data-stu-id="e4029-112">The following image shows the app you'll create.</span></span>

![El tutorial de conexión de ejemplo, muestra cómo conectarse y enviar un correo en la aplicación.](./images/iOSConnectWalkthrough.png)


<span data-ttu-id="e4029-114">El flujo de trabajo será conectarse o autenticarse en Microsoft Graph, iniciar sesión con su cuenta personal o profesional y, por último, enviar un correo a un destinatario.</span><span class="sxs-lookup"><span data-stu-id="e4029-114">The workflow will be to connect/authenticate to Microsoft Graph, sign in with your work or personal account, and finally send a mail to a recipient.</span></span>

<span data-ttu-id="e4029-p104">**¿No desea compilar una aplicación?** Use el [inicio rápido de Microsoft Graph](https://graph.microsoft.io/es-ES/getting-started) para ponerlo todo en funcionamiento de manera rápida.</span><span class="sxs-lookup"><span data-stu-id="e4029-p104">**Don't feel like building an app?** Use the [Microsoft Graph quick start](https://graph.microsoft.io/es-ES/getting-started) to get up and running fast.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e4029-117">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e4029-117">Prerequisites</span></span>

<span data-ttu-id="e4029-118">Para comenzar, necesitará:</span><span class="sxs-lookup"><span data-stu-id="e4029-118">To get started, you'll need:</span></span> 

* <span data-ttu-id="e4029-119">[Xcode](https://developer.apple.com/xcode/downloads/) de Apple</span><span class="sxs-lookup"><span data-stu-id="e4029-119">[Xcode](https://developer.apple.com/xcode/downloads/) from Apple</span></span>
* <span data-ttu-id="e4029-120">La instalación de [CocoaPods](https://guides.cocoapods.org/using/using-cocoapods.html) como administrador de dependencias.</span><span class="sxs-lookup"><span data-stu-id="e4029-120">Installation of [CocoaPods](https://guides.cocoapods.org/using/using-cocoapods.html) as a dependency manager</span></span>
* <span data-ttu-id="e4029-121">Una [cuenta Microsoft](https://www.outlook.com/) o una [cuenta profesional o educativa](http://dev.office.com/devprogram)</span><span class="sxs-lookup"><span data-stu-id="e4029-121">A [Microsoft account](https://www.outlook.com/) or a [work or school account](http://dev.office.com/devprogram)</span></span>
* <span data-ttu-id="e4029-122">[Proyecto inicial de Microsoft Graph para iOS](https://github.com/microsoftgraph/ios-objectivec-connect-sample).</span><span class="sxs-lookup"><span data-stu-id="e4029-122">The [Microsoft Graph Starter Project for iOS](https://github.com/microsoftgraph/ios-objectivec-connect-sample).</span></span> <span data-ttu-id="e4029-123">Esta plantilla contiene clases a las que agregará código.</span><span class="sxs-lookup"><span data-stu-id="e4029-123">This template contains classes that you'll add code to.</span></span> <span data-ttu-id="e4029-124">Para obtener este proyecto, clone o descargue el proyecto de ejemplo desde esta ubicación y trabajará con el área de trabajo de la carpeta **starter-project** (**ios-objectivec-connect-sample.xcworkspace**).</span><span class="sxs-lookup"><span data-stu-id="e4029-124">To get this project, clone or download the sample project from this location, and you'll work with the workspace inside the **starter-project** folder (**ios-objectivec-connect-sample.xcworkspace**).</span></span>

## <a name="register-the-app"></a><span data-ttu-id="e4029-125">Registrar la aplicación</span><span class="sxs-lookup"><span data-stu-id="e4029-125">Register the app</span></span>
 
1. <span data-ttu-id="e4029-126">Inicie sesión en el [Portal de registro de aplicaciones](https://apps.dev.microsoft.com/) mediante su cuenta personal, profesional o educativa.</span><span class="sxs-lookup"><span data-stu-id="e4029-126">Sign into the [App Registration Portal](https://apps.dev.microsoft.com/) using either your personal or work or school account.</span></span>
2. <span data-ttu-id="e4029-127">Seleccione **Agregar una aplicación**.</span><span class="sxs-lookup"><span data-stu-id="e4029-127">Select **Add an app**.</span></span>
3. <span data-ttu-id="e4029-128">Escriba un nombre para la aplicación y seleccione **Crear aplicación**.</span><span class="sxs-lookup"><span data-stu-id="e4029-128">Enter a name for the app, and select **Create application**.</span></span>
    
    <span data-ttu-id="e4029-129">Se muestra la página de registro, indicando las propiedades de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e4029-129">The registration page displays, listing the properties of your app.</span></span>
 
4. <span data-ttu-id="e4029-130">En **Plataformas**, seleccione **Agregar plataforma**.</span><span class="sxs-lookup"><span data-stu-id="e4029-130">Under **Platforms**, select **Add platform**.</span></span>
5. <span data-ttu-id="e4029-131">Seleccione **Plataforma nativa**.</span><span class="sxs-lookup"><span data-stu-id="e4029-131">Select **Native platform**.</span></span>
6. <span data-ttu-id="e4029-p106">Copie el identificador de cliente en el Portapapeles. Deberá escribir este valor en la aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e4029-p106">Copy the Client Id to the clipboard. You'll need to enter this value into the sample app.</span></span>

    <span data-ttu-id="e4029-134">El id. de la aplicación es un identificador único para su aplicación.</span><span class="sxs-lookup"><span data-stu-id="e4029-134">The app id is a unique identifier for your app.</span></span> 

7. <span data-ttu-id="e4029-135">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="e4029-135">Select **Save**.</span></span>

## <a name="importing-the-project-dependencies"></a><span data-ttu-id="e4029-136">Importar las dependencias del proyecto</span><span class="sxs-lookup"><span data-stu-id="e4029-136">Importing the project dependencies</span></span>

1. <span data-ttu-id="e4029-137">Clone este repositorio ([Ejemplo Connect de Office 365 para iOS con el SDK de Microsoft Graph](https://github.com/microsoftgraph/ios-objectivec-connect-sample)).</span><span class="sxs-lookup"><span data-stu-id="e4029-137">Clone this repository, [Office 365 Connect Sample for iOS Using the Microsoft Graph SDK](https://github.com/microsoftgraph/ios-objectivec-connect-sample).</span></span> 
><span data-ttu-id="e4029-138">IMPORTANTE: use el ejemplo de la carpeta starter-project y no el ejemplo de la raíz del proyecto.</span><span class="sxs-lookup"><span data-stu-id="e4029-138">IMPORTANT: Use the sample in the starter-project folder and not the sample at the root of the project.</span></span>

2. <span data-ttu-id="e4029-p107">Use CocoaPods para importar el SDK de Microsoft Graph y las dependencias de autenticación. Esta aplicación de ejemplo ya contiene un podfile que recibirá los pods en el proyecto. Vaya a la carpeta **starter-project** de la aplicación **Terminal** y, desde **Terminal**, ejecute lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e4029-p107">Use CocoaPods to import the Microsoft Graph SDK and authentication dependencies. This sample app already contains a podfile that will get the pods into the project. Navigate to the folder **starter-project** in the **Terminal** app, and from **Terminal** run:</span></span>

        pod install

   <span data-ttu-id="e4029-p108">Recibirá la confirmación de la importación de los pods al proyecto. Para obtener más información, consulte [CocoaPods](https://guides.cocoapods.org/using/using-cocoapods.html).</span><span class="sxs-lookup"><span data-stu-id="e4029-p108">You will receive confirmation that the pods have been imported into the project. For more information, see [CocoaPods](https://guides.cocoapods.org/using/using-cocoapods.html)</span></span>


## <a name="enable-keychain-sharing"></a><span data-ttu-id="e4029-144">Habilitar el uso compartido de cadenas de claves</span><span class="sxs-lookup"><span data-stu-id="e4029-144">Enable keychain sharing</span></span>
 
<span data-ttu-id="e4029-p109">Para Xcode 8, deberá agregar el grupo de cadenas de claves o la aplicación no podrá obtener acceso a la cadena de claves. Para agregar el grupo de cadenas de claves:</span><span class="sxs-lookup"><span data-stu-id="e4029-p109">For Xcode8, you need to add the keychain group or your app will fail to access keychain. To add the keychain group:</span></span>
 
1. <span data-ttu-id="e4029-p110">Seleccione el proyecto en el panel de administración de proyectos de Xcode. (⌘ + 1).</span><span class="sxs-lookup"><span data-stu-id="e4029-p110">Select the project on the project manager panel in Xcode. (⌘ + 1).</span></span>
 
2. <span data-ttu-id="e4029-149">Seleccione **iOS-ObjectiveC-Connect-Sample**.</span><span class="sxs-lookup"><span data-stu-id="e4029-149">Select **iOS-ObjectiveC-Connect-Sample**.</span></span>
 
3. <span data-ttu-id="e4029-150">En la pestaña Funcionalidad, habilite **Uso compartido de cadenas de claves**.</span><span class="sxs-lookup"><span data-stu-id="e4029-150">On the Capabilities tab, enable **Keychain Sharing**.</span></span>
 
4. <span data-ttu-id="e4029-151">Agregue **com.microsoft.ios-objectivec-connect-sample** a los grupos de llaves.</span><span class="sxs-lookup"><span data-stu-id="e4029-151">Add **com.microsoft.ios-objectivec-connect-sample** to the Keychain Groups.</span></span>
 

## <a name="authenticating-with-microsoft-graph"></a><span data-ttu-id="e4029-152">Autenticación con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="e4029-152">Authenticating with Microsoft Graph</span></span>

<span data-ttu-id="e4029-p111">Para volver a visitar el flujo de trabajo de la interfaz de usuario, la aplicación va a solicitar al usuario que se autentique y, a continuación, este podrá enviar un correo al usuario especificado. Para realizar solicitudes en el servicio Microsoft Graph, se debe proporcionar un proveedor de autenticación que sea capaz de autenticar solicitudes HTTPS con un token de portador OAuth 2.0 adecuado. En el proyecto de ejemplo, hay una clase de autenticación que ya tiene código auxiliar que se llama **AuthenticationProvider.m.** Agregaremos una función para solicitar (y adquirir) un token de acceso para llamar a la API de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="e4029-p111">To revisit the UI workflow, the app is going to have the user authenticate, and then they'll have the ability to send a mail to a specified user. To make requests against the Microsoft Graph service, an authentication provider must be supplied which is capable of authenticating HTTPS requests with an appropriate OAuth 2.0 bearer token. In the sample project there's an authentication class already stubbed out called **AuthenticationProvider.m.** We will add a function to request, and acquire, an access token for calling the Microsoft Graph API.</span></span> 

1. <span data-ttu-id="e4029-157">Abra el área de trabajo del proyecto Xcode (**iOS-ObjectiveC-Connect-Sample.xcworkspace**) de la carpeta **starter-project** y vaya a la carpeta **Authentication** para abrir el archivo **AuthenticationProvider.m.**</span><span class="sxs-lookup"><span data-stu-id="e4029-157">Open the Xcode project workspace (**iOS-ObjectiveC-Connect-Sample.xcworkspace**) in the **starter-project** folder, and navigate to the **Authentication** folder and open the file **AuthenticationProvider.m.**</span></span> <span data-ttu-id="e4029-158">Agregue el código siguiente a esa clase.</span><span class="sxs-lookup"><span data-stu-id="e4029-158">Add the following code to that class.</span></span>

```objectivec
   -(void) connectToGraphWithClientId:(NSString *)clientId scopes:(NSArray *)scopes completion:(void (^)    (NSError *))completion{
      [NXOAuth2AuthenticationProvider setClientId:kClientId scopes:scopes];
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
```     

2. <span data-ttu-id="e4029-p113">A continuación, agregue el método al archivo de encabezado. Abra el archivo **AuthenticationProvider.h** y agregue el código siguiente a esta clase.</span><span class="sxs-lookup"><span data-stu-id="e4029-p113">Next add the method to the header file. Open the file **AuthenticationProvider.h** and add the following code to this class.</span></span>
   ```objectivec
   -(void) connectToGraphWithClientId:(NSString *)clientId
                               scopes:(NSArray *)scopes
                           completion:(void (^)(NSError *error))completion;
   ```

2. <span data-ttu-id="e4029-p114">Por último, llamaremos a este método desde **ConnectViewController.m**. Este controlador es la vista predeterminada que carga la aplicación y hay un único botón denominado **Conectar** que el usuario pulsará para iniciar el proceso de autenticación. Este método toma dos parámetros, el **Id. de cliente** y los **ámbitos**, que trataremos con más detalle a continuación. Agregue la siguiente acción a **ConnectViewController.m**.</span><span class="sxs-lookup"><span data-stu-id="e4029-p114">Finally we'll call this method from **ConnectViewController.m**. This controller is the default view that the app loads, and there is a single button named **Connect** that the user will tap that will initiate the authentication process. This method takes in two parameters, the **Client ID** and **scopes**, we'll discuss these in more detail below. Add the following action to **ConnectViewController.m**.</span></span>

```objectivec
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
```     

## <a name="send-an-email-with-microsoft-graph"></a><span data-ttu-id="e4029-165">Enviar un correo electrónico con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="e4029-165">Send an email with Microsoft Graph</span></span>

<span data-ttu-id="e4029-p115">Después de configurar el proyecto para que pueda autenticar, las siguientes tareas corresponderán al envío de un correo a un usuario mediante la API de Microsoft Graph. De forma predeterminada, el usuario que inició sesión será el destinatario, pero tiene la posibilidad de cambiarlo a cualquier otro destinatario. El código con el que trabajaremos aquí está ubicado en la carpeta **Controllers** y en la clase **SendMailViewController.m.** Verá que aquí hay otro código representado para la interfaz de usuario y un método auxiliar para recuperar la información del perfil del usuario desde el servicio Microsoft Graph. Nos concentraremos en los métodos para crear un mensaje de correo y enviarlo.</span><span class="sxs-lookup"><span data-stu-id="e4029-p115">After configuring the project to be able to authenticate, the next tasks are sending a mail to a user using the Microsoft Graph API. By default the logged in user will be the recipient, but you have the ability to change it to any other recipient. The code we'll work with here is located in the **Controllers** folder and in the class **SendMailViewController.m.** You'll see that there is other code represented here for the UI, and a helper method to retrieve user profile information from the Microsoft Graph service. We'll concentrate on the methods for creating a mail message and sending that message.</span></span>

1. <span data-ttu-id="e4029-171">Abra el archivo **SendMailViewController.m** de la carpeta Controllers y agregue el siguiente código al método **viewDidLoad**, después de `self.graphClient = [MSGraphClient client]`.</span><span class="sxs-lookup"><span data-stu-id="e4029-171">Open **SendMailViewController.m** in the Controllers folder and add the following code to the **viewDidLoad** method, after `self.graphClient = [MSGraphClient client]`</span></span>
   ```objectivec
       [self getUserInfo:(self.emailAddress) completion:^( NSError *error) {
        if (!error) {
            [self getUserPicture:(self.emailAddress)  completion:^(UIImage *image, NSError *error) {
                if (!error) {
                    self.userPicture = image;
                } else {
                    //get the test image out of the project resources
                    self.userPicture = [UIImage imageNamed:(@"test.png")];
                }
                [self uploadPictureToOneDrive:(self.userPicture) completion:^(NSString *webUrl, NSError *error) {
                    if (!error) {
                        self.pictureWebUrl = webUrl;
                        dispatch_async(dispatch_get_main_queue(), ^{
                            self.sendMailButton.enabled = true;
                        });
                    } else {
                        dispatch_async(dispatch_get_main_queue(), ^{
                            NSLog(NSLocalizedString(@"ERROR", ""), error.localizedDescription);
                            self.statusTextView.text = NSLocalizedString(@"PICTURE_UPLOAD_FAILURE", comment: "");
                        });
                    }
                }];
            }];
        }
    }];
   ```

1. <span data-ttu-id="e4029-172">Abra el archivo **SendMailViewController.m.**</span><span class="sxs-lookup"><span data-stu-id="e4029-172">Open **SendMailViewController.m.**</span></span> <span data-ttu-id="e4029-173">de la carpeta Controllers y agregue el siguiente método auxiliar a la clase</span><span class="sxs-lookup"><span data-stu-id="e4029-173">in the Controllers folder and add the following helper method to the class</span></span>
```objectivec
  //Create a sample test message to send to specified user account
  -(MSGraphMessage*) getSampleMessage{
      MSGraphMessage *message = [[MSGraphMessage alloc]init];
      MSGraphRecipient *toRecipient = [[MSGraphRecipient alloc]init];
      MSGraphEmailAddress *email = [[MSGraphEmailAddress alloc]init];
    
      //need to get email text field for send to!
    
      email.address = self.emailAddress;
      toRecipient.emailAddress = email;
    
      NSMutableArray *toRecipients = [[NSMutableArray alloc]init];
      [toRecipients addObject:toRecipient];
    
      message.subject = NSLocalizedString(@"MAIL_SUBJECT", comment: "");
    
      MSGraphItemBody *emailBody = [[MSGraphItemBody alloc]init];
      NSString *htmlContentPath = [[NSBundle mainBundle] pathForResource:@"EmailBody" ofType:@"html"];
      NSString *htmlContentString = [NSString stringWithContentsOfFile:htmlContentPath encoding:NSUTF8StringEncoding error:nil];
    
      emailBody.content = htmlContentString;
      NSString *replaceString = @"a href=";
      replaceString = [replaceString stringByAppendingString:(self.pictureWebUrl)];
      emailBody.content = [emailBody.content stringByReplacingOccurrencesOfString:(@"a href=%s") withString:(replaceString)];
      emailBody.contentType = [MSGraphBodyType html];
      message.body = emailBody;
    
      message.toRecipients = toRecipients;
    
      MSGraphFileAttachment *fileAttachment= [[MSGraphFileAttachment alloc]init];
      fileAttachment.oDataType = @"#microsoft.graph.fileAttachment";
      fileAttachment.contentType = @"image/png";
    
      NSString *decodedString = [UIImagePNGRepresentation(self.userPicture) base64EncodedStringWithOptions:NSDataBase64EncodingEndLineWithCarriageReturn];
    
      fileAttachment.contentBytes = decodedString;
      fileAttachment.name = @"me.png";
      message.attachments = [message.attachments arrayByAddingObject:(fileAttachment)];
      return message;
    
    }
```
3. <span data-ttu-id="e4029-174">Abra el archivo **SendMailViewController.m.** Agregue a la clase el siguiente método.</span><span class="sxs-lookup"><span data-stu-id="e4029-174">Open **SendMailViewController.m** Add the following method to the class.</span></span>
<span data-ttu-id="e4029-175">**uploadPictureToOneDrive** carga la imagen de perfil del [usuario](https://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/resources/user) desde la información de [usuario](https://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/resources/user) y devuelve la dirección URL de uso compartido de web para incrustarla en el cuerpo del correo electrónico que envía el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e4029-175">**uploadPictureToOneDrive** uploads the [user](https://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/resources/user)'s profile picture from their [user](https://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/resources/user) information and returns the web sharing Url to be embedded in the body of the email that is sent by the sample.</span></span>

  ```objectivec
  -(void) uploadPictureToOneDrive: (UIImage *) image completion:(void(^) (NSString*, NSError*))completionBlock{
    
    NSData *data = UIImagePNGRepresentation(image);
    [[[[[[[self.graphClient me]
          drive]
         root]
        children]
       driveItem:(@"me.png")]
      contentRequest]
     uploadFromData:(data) completion:^(MSGraphDriveItem *response, NSError *error) {
         
         if (!error) {
             NSString *webUrl = response.webUrl;
             completionBlock(webUrl, error);
         } else {
             dispatch_async(dispatch_get_main_queue(), ^{
                 self.statusTextView.text =  NSLocalizedString(@"USER_GET_PICTURE_FAILURE", comment: "");
                 NSLog(NSLocalizedString(@"ERROR", ""), error.localizedDescription);
             });
         }
     }];
    }
  ```
4. <span data-ttu-id="e4029-176">Abra el archivo **SendMailViewController.m.** y agregue a la clase el siguiente método.</span><span class="sxs-lookup"><span data-stu-id="e4029-176">Open **SendMailViewController.m** and add the following method to the class.</span></span> 
<span data-ttu-id="e4029-177">**getUserPicture** devuelve la imagen de perfil del [usuario](https://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/resources/user), si está disponible.</span><span class="sxs-lookup"><span data-stu-id="e4029-177">**getUserPicture** returns the [user](https://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/resources/user)'s profile picture if it is available.</span></span>
   ```objectivec
   -(void) getUserPicture: (NSString *)url completion:(void(^) (UIImage*, NSError*))completionBlock {
    
    [[[self.graphClient me] photoValue] downloadWithCompletion:^(NSURL *location, NSURLResponse *response, NSError *error) {
        //code
        if (!error) {
            NSData *data = [NSData dataWithContentsOfURL:location];
            UIImage *img = [[UIImage alloc] initWithData:data];
            completionBlock(img, error);
        } else{
            completionBlock(nil, error);

        }
    }];
    }

   ```
3. <span data-ttu-id="e4029-178">Abra el archivo **SendMailViewController.m.** y agregue a la clase el siguiente método.</span><span class="sxs-lookup"><span data-stu-id="e4029-178">Open **SendMailViewcontroller.m** and add the following method to the class.</span></span>
<span data-ttu-id="e4029-179">Este método obtiene el recurso del [usuario](https://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/resources/user) que representa al usuario autenticado y captura los campos necesarios para obtener la imagen de perfil del usuario y enviar un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e4029-179">This method gets the [user](https://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/resources/user) resource representing the authenticated user and caches the fields necessary to get the user's profile picture and send an email.</span></span>
   ```objectivec
   //Retrieve the logged in user's display name and email address
   -(void) getUserInfo: (NSString *)url completion:(void(^) ( NSError*))completionBlock{
    
    [[[self.graphClient me]request]getWithCompletion:^(MSGraphUser *response, NSError *error) {
        if(!error){
            dispatch_async(dispatch_get_main_queue(), ^{
                self.emailAddress = response.userPrincipalName;
                self.emailTextField.text = self.emailAddress;
                self.headerLabel.text = [NSString stringWithFormat:(NSLocalizedString(@"HI_USER", comment "")), response.displayName];
                self.statusTextView.text =  NSLocalizedString(@"USER_INFO_LOAD_SUCCESS", comment: "");
            });

            completionBlock(nil);
        }
        else{
            dispatch_async(dispatch_get_main_queue(), ^{
                self.statusTextView.text =  NSLocalizedString(@"USER_INFO_LOAD_FAILURE", comment: "");
                NSLog(NSLocalizedString(@"ERROR", ""), error.localizedDescription);
            });
            completionBlock(error);
        }
    }];
    
   }

   ```
3. <span data-ttu-id="e4029-180">Abra el archivo **SendMailViewController.m**. Agregue a la clase el siguiente método para enviar correo.</span><span class="sxs-lookup"><span data-stu-id="e4029-180">Open **SendMailViewController.m** Add the following send mail method to the class.</span></span>
<span data-ttu-id="e4029-181">**getSampleMessage** crea un borrador HTML de ejemplo para usar con fines de demostración.</span><span class="sxs-lookup"><span data-stu-id="e4029-181">**getSampleMessage** creates a draft HTML sample mail to use for demo purposes.</span></span> <span data-ttu-id="e4029-182">A continuación, el siguiente método, **sendMail**, toma ese mensaje y ejecuta la solicitud de enviarlo.</span><span class="sxs-lookup"><span data-stu-id="e4029-182">The next method, **sendMail**, then takes that message and executes the request to send it.</span></span> <span data-ttu-id="e4029-183">Una vez más, el destinatario predeterminado es el usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="e4029-183">Again the default recipient is the signed-in user.</span></span>


  ```objectivec
   //Send mail to the specified user in the email text field
   -(void) sendMail {
    MSGraphMessage *message = [self getSampleMessage];
    MSGraphUserSendMailRequestBuilder *requestBuilder = [[self.graphClient me]sendMailWithMessage:message saveToSentItems:true];
    NSLog(@"%@", requestBuilder);
    MSGraphUserSendMailRequest *mailRequest = [requestBuilder request];
    [mailRequest executeWithCompletion:^(NSDictionary *response, NSError *error) {
        if(!error){
            NSLog(@"response %@", response);
             dispatch_async(dispatch_get_main_queue(), ^{
                self.statusTextView.text = NSLocalizedString(@"SEND_SUCCESS", comment: "");
                self.descriptionLabel.text = @"Check your inbox. You have a new message :)";
            });
        }
        else {
            dispatch_async(dispatch_get_main_queue(), ^{
                NSLog(NSLocalizedString(@"ERROR", ""), error.localizedDescription);
                self.statusTextView.text = NSLocalizedString(@"SEND_FAILURE", comment: "");
            });
        }
    }];
   }
   ```



## <a name="run-the-app"></a><span data-ttu-id="e4029-184">Ejecutar la aplicación</span><span class="sxs-lookup"><span data-stu-id="e4029-184">Run the app</span></span>
1. <span data-ttu-id="e4029-p121">Antes de ejecutar el ejemplo, deberá proporcionar el identificador de cliente que recibió del proceso de registro en la sección **Registrar la aplicación.** Abra el archivo **AuthenticationConstants.m** de la carpeta **Application**. Verá que el ClientID del proceso de registro se puede agregar a la parte superior del archivo:</span><span class="sxs-lookup"><span data-stu-id="e4029-p121">Before running the sample you'll need to supply the client ID you received from the registration process in the section **Register the app.** Open **AuthenticationConstants.m** under the **Application** folder. You'll see that the ClientID from the registration process can be added to the top of the file.:</span></span>  
   ```objectivec
   // You will set your application's clientId
   NSString * const kClientId    = @"ENTER_YOUR_CLIENT_ID";
   NSString * const kScopes = @"https://graph.microsoft.com/User.Read, https://graph.microsoft.com/Mail.ReadWrite, https://graph.microsoft.com/Mail.Send, https://graph.microsoft.com/Files.ReadWrite";
   ```      

><span data-ttu-id="e4029-p122">Nota: Observará que se han configurado los siguientes ámbitos de permiso para este proyecto: **"https://graph.microsoft.com/Mail.Send", "https://graph.microsoft.com/User.Read", "offline_access"**. Las llamadas de servicio usadas en este proyecto, el envío de un correo a su cuenta de correo y la recuperación de parte de la información de perfil (nombre para mostrar, dirección de correo electrónico) requieren estos permisos para que la aplicación se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="e4029-p122">Note: You'll notice that the following permission scopes have been configured for this project: **"https://graph.microsoft.com/Mail.Send", "https://graph.microsoft.com/User.Read", "offline_access"**. The service calls used in this project, sending a mail to your mail account and retrieving some profile information (Display Name, Email Address) require these permissions for the app to run properly.</span></span>

2. <span data-ttu-id="e4029-190">Ejecute el ejemplo, pulse **Conectar**, inicie sesión con su cuenta personal, profesional o educativa y conceda los permisos solicitados.</span><span class="sxs-lookup"><span data-stu-id="e4029-190">Run the sample, tap **Connect,** sign in with your personal or work or school account, and grant the requested permissions.</span></span>

3. <span data-ttu-id="e4029-p123">Elija el botón **Enviar correo electrónico**. Cuando se envíe el correo, se mostrará un mensaje de operación correcta debajo del botón.</span><span class="sxs-lookup"><span data-stu-id="e4029-p123">Choose the **Send email** button. When the mail is sent, a success message is displayed below the button.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e4029-193">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="e4029-193">Next steps</span></span>
- <span data-ttu-id="e4029-194">Pruebe la API de REST mediante el [Probador de Graph](https://graph.microsoft.io/graph-explorer).</span><span class="sxs-lookup"><span data-stu-id="e4029-194">Try out the REST API using the [Graph explorer](https://graph.microsoft.io/graph-explorer).</span></span>
- <span data-ttu-id="e4029-195">Busque ejemplos de operaciones comunes tanto para REST como para SDK en el [Ejemplo de fragmentos de código de Objective C para Microsoft Graph para iOS](https://github.com/microsoftgraph/ios-objectiveC-snippets-sample). </span><span class="sxs-lookup"><span data-stu-id="e4029-195">Find examples of common operations for both REST and SDK operations in the [Microsoft Graph iOS Objective C Snippets Sample](https://github.com/microsoftgraph/ios-objectiveC-snippets-sample).</span></span>

## <a name="see-also"></a><span data-ttu-id="e4029-196">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e4029-196">See also</span></span>
- [<span data-ttu-id="e4029-197">SDK de Microsoft Graph para iOS</span><span class="sxs-lookup"><span data-stu-id="e4029-197">Microsoft Graph SDK for iOS</span></span>](https://github.com/microsoftgraph/msgraph-sdk-ios)
- [<span data-ttu-id="e4029-198">Protocolos de Azure AD v2.0</span><span class="sxs-lookup"><span data-stu-id="e4029-198">Azure AD v2.0 protocols</span></span>](https://azure.microsoft.com/es-ES/documentation/articles/active-directory-v2-protocols/)
- [<span data-ttu-id="e4029-199">Tokens de Azure AD v2.0</span><span class="sxs-lookup"><span data-stu-id="e4029-199">Azure AD v2.0 tokens</span></span>](https://azure.microsoft.com/es-ES/documentation/articles/active-directory-v2-tokens/)
