---
title: Llamar a los servicios de Office 365 en Visual Studio 2017 con la API de Microsoft Graph
description: Puede utilizar Servicios conectados en Visual Studio a fin de configurar su aplicación para llamar a la API de Microsoft Graph. En este artículo se describe cómo obtener una foto de perfil del usuario que ha iniciado sesión, cargarla en OneDrive y enviar un correo electrónico con un vínculo para compartir a la foto.
ms.openlocfilehash: 33469dec7014d81ed55c2efceb96a26c2651d239
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092845"
---
# <a name="call-office-365-services-in-visual-studio-2017-with-the-microsoft-graph-api"></a>Llamar a los servicios de Office 365 en Visual Studio 2017 con la API de Microsoft Graph

Puede utilizar Servicios conectados en Visual Studio a fin de configurar su aplicación para llamar a la API de Microsoft Graph. En este artículo se describe cómo obtener una foto de perfil del usuario que ha iniciado sesión, cargarla en OneDrive y enviar un correo electrónico con un vínculo para compartir a la foto.

## <a name="get-set-up"></a>Para empezar

Para utilizar los servicios conectados de Office 365 con Microsoft Graph, debe hacer lo siguiente:

- Descargue [Visual Studio 2017 Preview](https://www.visualstudio.com/vs/preview/) si no lo ha hecho ya. Si está usando una versión anterior de Visual Studio, puede utilizar Visual Studio 2017 Preview en paralelo con la versión actual.

- Consiga una suscripción a Office 365. Para obtener una versión de prueba gratuita, únase al [programa Office 365 Developer](https://dev.office.com/devprogram).

## <a name="get-the-starter-project"></a>Obtener el proyecto de inicio

Descargue el [ejemplo de Servicios conectados de Microsoft Graph ASP.NET](https://github.com/microsoftgraph/aspnet-connect-sample/archive/Office365connectedservice.zip). Este ejemplo incluye las referencias que necesita para autenticarse en Microsoft Graph. Después de descargar el proyecto de inicio, descomprímalo y abra el ejemplo en Visual Studio 2017 Preview.

## <a name="add-the-connected-service"></a>Agregar el Servicio conectado

Ahora está listo para agregar el servicio de Microsoft Graph a su proyecto de Visual Studio. 

1. En el explorador de soluciones, elija **Servicios conectados** para abrir la pestaña Servicios conectados. 

2. Elija el proveedor en **Acceder a los servicios de Office 365 con Microsoft Graph**. Siga las instrucciones del asistente. Seleccione los siguientes permisos (puede cambiar los permisos más adelante):

    - Para las API de **File**, establezca los permisos en **Tener acceso completo a los archivos**.
    - Para las API de **Mail**, establezca los permisos en **Enviar correo en su nombre**.
    - Para las API de **User**, establezca los permisos en **Iniciar sesión y leer su perfil**.

## <a name="call-the-microsoft-graph-api"></a>Llamar a la API de Microsoft Graph

El ejemplo de inicio está configurado para enviar un correo electrónico simple. Puede utilizar Microsoft Graph para actualizar el ejemplo y enviar un correo electrónico con un vínculo a la foto de perfil del usuario que ha iniciado sesión en OneDrive.

1. Vaya a "Models\GraphService.cs", que hospeda el código para llamar a Microsoft Graph.

2. Busque y **quite las marcas de comentarios** a las llamadas al SDK en los métodos siguientes. Muestra cómo llamar a Microsoft Graph para obtener una foto de perfil, cargar un archivo en OneDrive y obtener un enlace para compartir.

    ```csharp
        GetCurrentUserPhotoStream(GraphServiceClient graphClient)
    ```
    
    ```csharp
        UploadFileToOneDrive(GraphServiceClient graphClient, byte[] file)
    ```

    ```csharp
        GetSharingLink(GraphServiceClient graphClient, string Id)
    ```
 
> **Sugerencia:** Cada comentario empieza con "//Uncomment:"
 

## <a name="run-the-sample"></a>Ejecutar el ejemplo
Compile y ejecute el ejemplo. Luego, elija el vínculo de **inicio de sesión** situado en la esquina superior derecha y elija **Obtener la dirección de correo electrónico** seguido de **Enviar correo electrónico**.

Esto enviará un correo electrónico que incluya un vínculo a la foto de su perfil.

>**Notas**:

>- Si detiene y vuelve a ejecutar el ejemplo desde Visual Studio, necesitará cerrar la sesión explícitamente para que el ejemplo funcione.
>- Si se muestra una excepción que indica que el usuario no está autenticado, puede que necesite repetir el paso de [Agregar el servicio conectado](#add-the-connected-service).
    

## <a name="explore-the-code"></a>Examinar el código

Ahora puede utilizar Visual Studio 2017 para conectarse y configurar los servicios. El ejemplo de inicio crea el scaffolding y las referencias.  

El ejemplo de inicio incluye los siguientes archivos:

- [Startup.Auth.cs](https://github.com/microsoftgraph/aspnet-connect-sample/tree/Office365connectedservice/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Microsoft%20Graph%20SDK%20ASPNET%20Sample/App_Start/Startup.Auth.cs): autentica al usuario actual e inicializa la memoria caché del token del ejemplo.

- Modelos\\[SessionTokenCache.cs](https://github.com/microsoftgraph/aspnet-connect-sample/tree/Office365connectedservice/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Microsoft%20Graph%20SDK%20ASPNET%20Sample/TokenStorage/SessionTokenCache.cs): almacena la información del token del usuario. Se puede reemplazar por su memoria caché de token personalizada. Más información en [Almacenamiento en la memoria caché de los tokens de acceso en una aplicación de varios inquilinos](https://azure.microsoft.com/es-ES/documentation/articles/guidance-multitenant-identity-token-cache/).

- Modelos\\[SampleAuthProvider.cs](https://github.com/microsoftgraph/aspnet-connect-sample/tree/Office365connectedservice/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Helpers/SampleAuthProvider.cs): implementa la interfaz IAuthProvider local y obtiene un token de acceso. 

- Aplicación auxiliar \\[SDKHelper.cs](https://github.com/microsoftgraph/aspnet-connect-sample/tree/Office365connectedservice/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Helpers/SDKHelper.cs): inicializa **GraphServiceClient** desde la [Biblioteca cliente de Microsoft Graph .NET](https://github.com/microsoftgraph/msgraph-sdk-dotnet) que se usa para interactuar con Microsoft Graph.

- Controlador \\[HomeController.cs](https://github.com/microsoftgraph/aspnet-connect-sample/tree/Office365connectedservice/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Controllers/HomeController.cs): contiene métodos que usan **GraphServiceClient** para crear y enviar llamadas al servicio Microsoft Graph y procesar la respuesta.

- Vistas \\Inicio\\[Graph.cshtml](https://github.com/microsoftgraph/aspnet-connect-sample/tree/Office365connectedservice/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Microsoft%20Graph%20SDK%20ASPNET%20Sample/Views/Home/Graph.cshtml): contiene la interfaz de usuario como ejemplo. 


## <a name="need-help"></a>¿Necesita ayuda?

Si necesita ayuda, publique sus preguntas en [StackOverflow](https://stackoverflow.com/questions/tagged/microsoftgraph?sort=newest). Etiquete sus preguntas con {microsoftgraph}.

