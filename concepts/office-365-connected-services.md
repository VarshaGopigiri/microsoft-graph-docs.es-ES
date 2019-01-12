---
title: Llamar a los servicios de Office 365 en Visual Studio 2017 con la API de Microsoft Graph
description: Puede utilizar Servicios conectados en Visual Studio a fin de configurar su aplicación para llamar a la API de Microsoft Graph. En este artículo se describe cómo obtener una foto de perfil del usuario que ha iniciado sesión, cargarla en OneDrive y enviar un correo electrónico con un vínculo para compartir a la foto.
localization_priority: Priority
ms.prod: reports
ms.openlocfilehash: 0a084fd7c4fa946854e3f932586f52cdcce370fd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27979239"
---
# <a name="call-office-365-services-in-visual-studio-2017-with-the-microsoft-graph-api"></a><span data-ttu-id="8ba53-104">Llamar a los servicios de Office 365 en Visual Studio 2017 con la API de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="8ba53-104">Call Office 365 services in Visual Studio 2017 with the Microsoft Graph API</span></span>

<span data-ttu-id="8ba53-p102">Puede utilizar Servicios conectados en Visual Studio a fin de configurar su aplicación para llamar a la API de Microsoft Graph. En este artículo se describe cómo obtener una foto de perfil del usuario que ha iniciado sesión, cargarla en OneDrive y enviar un correo electrónico con un vínculo para compartir a la foto.</span><span class="sxs-lookup"><span data-stu-id="8ba53-p102">You can use the Connected Services in Visual Studio to configure your app to call the Microsoft Graph API. This article describes how to get a signed in user's profile photo, upload it to OneDrive, and send an email with a sharing link to the photo.</span></span>

## <a name="get-set-up"></a><span data-ttu-id="8ba53-107">Para empezar</span><span class="sxs-lookup"><span data-stu-id="8ba53-107">Get set up</span></span>

<span data-ttu-id="8ba53-108">Para utilizar los servicios conectados de Office 365 con Microsoft Graph, debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8ba53-108">To use the Office 365 Connected Services with Microsoft Graph, you'll need to do the following:</span></span>

- <span data-ttu-id="8ba53-p103">Descargue [Visual Studio 2017 Preview](https://www.visualstudio.com/vs/preview/) si no lo ha hecho ya. Si está usando una versión anterior de Visual Studio, puede utilizar Visual Studio 2017 Preview en paralelo con la versión actual.</span><span class="sxs-lookup"><span data-stu-id="8ba53-p103">Download the [Visual Studio 2017 Preview](https://www.visualstudio.com/vs/preview/), if you haven't already. If you're using an earlier version of Visual Studio, you can use Visual Studio 2017 Preview side by side with your current version.</span></span>

- <span data-ttu-id="8ba53-p104">Consiga una suscripción a Office 365. Para obtener una versión de prueba gratuita, únase al [programa Office 365 Developer](https://dev.office.com/devprogram).</span><span class="sxs-lookup"><span data-stu-id="8ba53-p104">Get an Office 365 subscription. To get a free trial, join the [Office 365 Developer program](https://dev.office.com/devprogram).</span></span>

## <a name="get-the-starter-project"></a><span data-ttu-id="8ba53-113">Obtener el proyecto de inicio</span><span class="sxs-lookup"><span data-stu-id="8ba53-113">Get the starter project</span></span>

<span data-ttu-id="8ba53-p105">Descargue el [ejemplo de Servicios conectados de Microsoft Graph ASP.NET](https://github.com/microsoftgraph/aspnet-connect-sample/archive/Office365connectedservice.zip). Este ejemplo incluye las referencias que necesita para autenticarse en Microsoft Graph. Después de descargar el proyecto de inicio, descomprímalo y abra el ejemplo en Visual Studio 2017 Preview.</span><span class="sxs-lookup"><span data-stu-id="8ba53-p105">Download the [Microsoft Graph ASP.NET Connected Services Sample](https://github.com/microsoftgraph/aspnet-connect-sample/archive/Office365connectedservice.zip). This sample includes the references that you need to authenticate against Microsoft Graph. After you download the starter project, unzip, and open the sample in Visual Studio 2017 Preview.</span></span>

## <a name="add-the-connected-service"></a><span data-ttu-id="8ba53-117">Agregar el Servicio conectado</span><span class="sxs-lookup"><span data-stu-id="8ba53-117">Add the Connected Service</span></span>

<span data-ttu-id="8ba53-118">Ahora está listo para agregar el servicio de Microsoft Graph a su proyecto de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8ba53-118">You're now ready to add the Microsoft Graph service to your Visual Studio project.</span></span> 

1. <span data-ttu-id="8ba53-119">En el explorador de soluciones, elija **Servicios conectados** para abrir la pestaña Servicios conectados.</span><span class="sxs-lookup"><span data-stu-id="8ba53-119">In Solution Explorer, choose **Connected Services** to open the Connected Services tab.</span></span> 

2. <span data-ttu-id="8ba53-p106">Elija el proveedor en **Acceder a los servicios de Office 365 con Microsoft Graph**. Siga las instrucciones del asistente. Seleccione los siguientes permisos (puede cambiar los permisos más adelante):</span><span class="sxs-lookup"><span data-stu-id="8ba53-p106">Choose the **Access Office 365 Services with Microsoft Graph** provider. Follow the wizard. Select the following permissions (you can change the permisssions later):</span></span>

    - <span data-ttu-id="8ba53-123">Para las API de **File**, establezca los permisos en **Tener acceso completo a los archivos**.</span><span class="sxs-lookup"><span data-stu-id="8ba53-123">For the **File** APIs, set permissions to **Have full access to your files**.</span></span>
    - <span data-ttu-id="8ba53-124">Para las API de **Mail**, establezca los permisos en **Enviar correo en su nombre**.</span><span class="sxs-lookup"><span data-stu-id="8ba53-124">For the **Mail** APIs, set permissions to **Send mail as you**.</span></span>
    - <span data-ttu-id="8ba53-125">Para las API de **User**, establezca los permisos en **Iniciar sesión y leer su perfil**.</span><span class="sxs-lookup"><span data-stu-id="8ba53-125">For the **User** APIs, set permissions to **Sign you in and read your profile**.</span></span>

## <a name="call-the-microsoft-graph-api"></a><span data-ttu-id="8ba53-126">Llamar a la API de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="8ba53-126">Call the Microsoft Graph API</span></span>

<span data-ttu-id="8ba53-p107">El ejemplo de inicio está configurado para enviar un correo electrónico simple. Puede utilizar Microsoft Graph para actualizar el ejemplo y enviar un correo electrónico con un vínculo a la foto de perfil del usuario que ha iniciado sesión en OneDrive.</span><span class="sxs-lookup"><span data-stu-id="8ba53-p107">The starter sample is configured to send a simple email. You can use Microsoft Graph to update the sample to send an email with a link to the signed-in user's profile photo in OneDrive.</span></span>

1. <span data-ttu-id="8ba53-129">Vaya a "Models\GraphService.cs", que hospeda el código para llamar a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="8ba53-129">Go to 'Models\GraphService.cs', which hosts the code to call Microsoft Graph.</span></span>

2. <span data-ttu-id="8ba53-p108">Busque y **quite las marcas de comentarios** a las llamadas al SDK en los métodos siguientes. Muestra cómo llamar a Microsoft Graph para obtener una foto de perfil, cargar un archivo en OneDrive y obtener un enlace para compartir.</span><span class="sxs-lookup"><span data-stu-id="8ba53-p108">Find and **Uncomment** calls to the SDK in the following methods. This shows how to call Microsoft Graph to get a profile photo, upload a file to OneDrive, and get a sharing link.</span></span>

    ```csharp
        GetCurrentUserPhotoStream(GraphServiceClient graphClient)
    ```
    
    ```csharp
        UploadFileToOneDrive(GraphServiceClient graphClient, byte[] file)
    ```

    ```csharp
        GetSharingLink(GraphServiceClient graphClient, string Id)
    ```
 
> <span data-ttu-id="8ba53-132">**Sugerencia:** Cada comentario empieza con "//Uncomment:"</span><span class="sxs-lookup"><span data-stu-id="8ba53-132">**Tip:** Each comment starts with '//Uncomment:'</span></span>
 

## <a name="run-the-sample"></a><span data-ttu-id="8ba53-133">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="8ba53-133">Run the sample</span></span>
<span data-ttu-id="8ba53-p109">Compile y ejecute el ejemplo. Luego, elija el vínculo de **inicio de sesión** situado en la esquina superior derecha y elija **Obtener la dirección de correo electrónico** seguido de **Enviar correo electrónico**.</span><span class="sxs-lookup"><span data-stu-id="8ba53-p109">Build and run the sample. Next, choose the **Sign-in** link on the top right, and then choose **Get email address** followed by **Send email**.</span></span>

<span data-ttu-id="8ba53-136">Esto enviará un correo electrónico que incluya un vínculo a la foto de su perfil.</span><span class="sxs-lookup"><span data-stu-id="8ba53-136">This will send an email that includes a link to your profile photo.</span></span>

><span data-ttu-id="8ba53-137">**Notas**:</span><span class="sxs-lookup"><span data-stu-id="8ba53-137">**Notes:**</span></span>

>- <span data-ttu-id="8ba53-138">Si detiene y vuelve a ejecutar el ejemplo desde Visual Studio, necesitará cerrar la sesión explícitamente para que el ejemplo funcione.</span><span class="sxs-lookup"><span data-stu-id="8ba53-138">If you stop and rerun the sample from Visual Studio, you might need to explicitly sign out for the sample to work.</span></span>
>- <span data-ttu-id="8ba53-139">Si se muestra una excepción que indica que el usuario no está autenticado, puede que necesite repetir el paso de [Agregar el servicio conectado](#add-the-connected-service).</span><span class="sxs-lookup"><span data-stu-id="8ba53-139">If you get an exception that indicates that the User is not authenticated, you might need to repeat the [Add the Connected Service](#add-the-connected-service) step.</span></span>
    

## <a name="explore-the-code"></a><span data-ttu-id="8ba53-140">Examinar el código</span><span class="sxs-lookup"><span data-stu-id="8ba53-140">Explore the code</span></span>

<span data-ttu-id="8ba53-p110">Ahora puede utilizar Visual Studio 2017 para conectarse y configurar los servicios. El ejemplo de inicio crea el scaffolding y las referencias.</span><span class="sxs-lookup"><span data-stu-id="8ba53-p110">You can now use Visual Studio 2017 to connect to and configure your services. The starter sample creates the scaffolding and references for you.</span></span>  

<span data-ttu-id="8ba53-143">El ejemplo de inicio incluye los siguientes archivos:</span><span class="sxs-lookup"><span data-stu-id="8ba53-143">The starter sample includes the following files:</span></span>

- <span data-ttu-id="8ba53-144">[Startup.Auth.cs](https://github.com/microsoftgraph/aspnet-connect-sample/tree/Office365connectedservice/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Microsoft%20Graph%20SDK%20ASPNET%20Sample/App_Start/Startup.Auth.cs): autentica al usuario actual e inicializa la memoria caché del token del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8ba53-144">[Startup.Auth.cs](https://github.com/microsoftgraph/aspnet-connect-sample/tree/Office365connectedservice/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Microsoft%20Graph%20SDK%20ASPNET%20Sample/App_Start/Startup.Auth.cs) - Authenticates the current user and initializes the sample's token cache.</span></span>

- <span data-ttu-id="8ba53-p111">Modelos\\[SessionTokenCache.cs](https://github.com/microsoftgraph/aspnet-connect-sample/tree/Office365connectedservice/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Microsoft%20Graph%20SDK%20ASPNET%20Sample/TokenStorage/SessionTokenCache.cs): almacena la información del token del usuario. Se puede reemplazar por su memoria caché de token personalizada. Más información en [Almacenamiento en la memoria caché de los tokens de acceso en una aplicación de varios inquilinos](https://azure.microsoft.com/es-ES/documentation/articles/guidance-multitenant-identity-token-cache/).</span><span class="sxs-lookup"><span data-stu-id="8ba53-p111">Models\\[SessionTokenCache.cs](https://github.com/microsoftgraph/aspnet-connect-sample/tree/Office365connectedservice/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Microsoft%20Graph%20SDK%20ASPNET%20Sample/TokenStorage/SessionTokenCache.cs) - Stores the user's token information. You can replace this with your own custom token cache. For more information, see [Caching access tokens in a multitenant application](https://azure.microsoft.com/es-ES/documentation/articles/guidance-multitenant-identity-token-cache/).</span></span>

- <span data-ttu-id="8ba53-148">Modelos\\[SampleAuthProvider.cs](https://github.com/microsoftgraph/aspnet-connect-sample/tree/Office365connectedservice/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Helpers/SampleAuthProvider.cs): implementa la interfaz IAuthProvider local y obtiene un token de acceso.</span><span class="sxs-lookup"><span data-stu-id="8ba53-148">Models\\[SampleAuthProvider.cs](https://github.com/microsoftgraph/aspnet-connect-sample/tree/Office365connectedservice/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Helpers/SampleAuthProvider.cs) - Implements the local IAuthProvider interface, and gets an access token.</span></span> 

- <span data-ttu-id="8ba53-149">Aplicación auxiliar \\[SDKHelper.cs](https://github.com/microsoftgraph/aspnet-connect-sample/tree/Office365connectedservice/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Helpers/SDKHelper.cs): inicializa **GraphServiceClient** desde la [Biblioteca cliente de Microsoft Graph .NET](https://github.com/microsoftgraph/msgraph-sdk-dotnet) que se usa para interactuar con Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="8ba53-149">Helpers\\[SDKHelper.cs](https://github.com/microsoftgraph/aspnet-connect-sample/tree/Office365connectedservice/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Helpers/SDKHelper.cs) - Initializes the **GraphServiceClient** from the [Microsoft Graph .NET Client Library](https://github.com/microsoftgraph/msgraph-sdk-dotnet) that is used to interact with the Microsoft Graph.</span></span>

- <span data-ttu-id="8ba53-150">Controlador \\[HomeController.cs](https://github.com/microsoftgraph/aspnet-connect-sample/tree/Office365connectedservice/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Controllers/HomeController.cs): contiene métodos que usan **GraphServiceClient** para crear y enviar llamadas al servicio Microsoft Graph y procesar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8ba53-150">Controllers\\[HomeController.cs](https://github.com/microsoftgraph/aspnet-connect-sample/tree/Office365connectedservice/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Controllers/HomeController.cs) - Contains methods that use the **GraphServiceClient** to build and send calls to the Microsoft Graph service and to process the response.</span></span>

- <span data-ttu-id="8ba53-151">Vistas \\Inicio\\[Graph.cshtml](https://github.com/microsoftgraph/aspnet-connect-sample/tree/Office365connectedservice/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Views/Home/Graph.cshtml): contiene la interfaz de usuario como ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8ba53-151">Views\\Home\\[Graph.cshtml](https://github.com/microsoftgraph/aspnet-connect-sample/tree/Office365connectedservice/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Views/Home/Graph.cshtml) - Contains the UI for the sample.</span></span> 


## <a name="need-help"></a><span data-ttu-id="8ba53-152">¿Necesita ayuda?</span><span class="sxs-lookup"><span data-stu-id="8ba53-152">Need help?</span></span>

<span data-ttu-id="8ba53-p112">Si necesita ayuda, publique sus preguntas en [StackOverflow](https://stackoverflow.com/questions/tagged/microsoftgraph?sort=newest). Etiquete sus preguntas con {microsoftgraph}.</span><span class="sxs-lookup"><span data-stu-id="8ba53-p112">If you need help, post your questions on [StackOverflow](https://stackoverflow.com/questions/tagged/microsoftgraph?sort=newest). Tag your post with {microsoftgraph}.</span></span>

