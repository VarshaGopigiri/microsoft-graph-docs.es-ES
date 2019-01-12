---
title: 'Crear aplicaciones para varios dispositivos con tecnología de Project Rome '
description: 'Puede usar Project Rome para crear experiencias transversales entre dispositivos y plataformas sin problemas, lo que reduce la fricción para los usuarios y contribuye a fomentar la interacción de las aplicaciones. Para que las aplicaciones compartan datos entre varios dispositivos y plataformas con las API de Project Rome, debe configurar una aplicación para varios dispositivos que incluya información sobre las aplicaciones específicas de la plataforma. '
localization_priority: Normal
ms.prod: project-rome
ms.openlocfilehash: f54f38c5d047d2b5d790e5bea48fdb27f54b4004
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987086"
---
# <a name="build-cross-device-apps-powered-by-project-rome"></a>Crear aplicaciones para varios dispositivos con tecnología de Project Rome 

Puede usar Project Rome para crear experiencias transversales entre dispositivos y plataformas sin problemas, lo que reduce la fricción para los usuarios y contribuye a fomentar la interacción de las aplicaciones. Para que las aplicaciones compartan datos entre varios dispositivos y plataformas con las API de Project Rome, debe configurar una aplicación para varios dispositivos que incluya información sobre las aplicaciones específicas de la plataforma. 

Una aplicación para varios dispositivos le permite: 

- Usar la API de fuente de actividades de Project Rome en Microsoft Graph  
- Leer y escribir las actividades de usuario publicadas por un grupo de aplicaciones específicas de una plataforma mediante el SDK de Project Rome para Windows, Android o iOS.
-  Destinar aplicaciones a través de las funcionalidades de retransmisión de dispositivos de Project Rome mediante el SDK de Project Rome para Windows, Android o iOS.

**Retomar el trabajo donde lo dejó en dispositivos con la API de fuente de actividades**

Puede configurar una aplicación para varios dispositivos que asocie las aplicaciones para Windows, iOS, Android y la web a fin de que la aplicación de cada plataforma pueda leer y escribir las actividades de usuario que publique cualquier aplicación del grupo. 

Por ejemplo, una usuaria está terminando un comunicado de prensa en su PC en el trabajo antes de cenar con sus amigos. En el restaurante, recibe una notificación de su jefe sobre un error ortográfico que debe solucionarse cuanto antes. Abre la aplicación en su teléfono Android y ve una tarjeta que muestra el comunicado de prensa que estaba editando antes. Puntea la tarjeta para abrirla y corregir el comunicado inmediatamente y volver con sus amigos. 
 
Con esta configuración de aplicación para varios dispositivos, la fuente de actividades del usuario se sincroniza fácilmente entre dispositivos y plataformas para poder crear experiencias que ayuden a los usuarios a retomar tareas importantes donde las dejaron en cualquier superficie de aplicación. 

**Elegir la pantalla adecuada en el momento oportuno con la API de retransmisión de dispositivo**

Puede configurar una aplicación para varios dispositivos con credenciales de notificación push en cada una de las plataformas en las que su aplicación está disponible, de modo que pueda recibirse un comando o notificación en cualquier dispositivo en el que se use la aplicación, independientemente de la plataforma. 

Por ejemplo, una usuaria está viendo un video en el autobús que lo lleva a su casa desde el trabajo. Al llegar a casa, puntea la aplicación para iniciar el vídeo en la Xbox One y poder seguir viéndola en la gran pantalla. 

Al asociar las credenciales de notificación de inserción a cada una de las plataformas en las que la aplicación está disponible con la aplicación para varios dispositivos, la aplicación del usuario podrá enviar comandos a varios dispositivos, para que se puedan crear experiencias transversales entre pantallas o pasar un flujo de trabajo de un dispositivo a otro en tiempo real. 

## <a name="select-the-right-hosting-method-for-your-cross-device-app-configuration"></a>Seleccionar el método de hospedaje correcto para la configuración de aplicación para varios dispositivos
Puede hospedar la configuración de aplicación para varios dispositivos como archivo JSON en su dominio o como perfil configurable a través del [Centro de desarrollo de Windows](https://developer.microsoft.com/es-ES/windows). Elija una opción de hospedaje según las funcionalidades de Project Rome que quiera habilitar en las aplicaciones. 

### <a name="windows-dev-center-profile-recommended"></a>Perfil del Centro de desarrollo de Windows (opción recomendada) 
Con una aplicación para varios dispositivos administrada en el [Centro de desarrollo de Windows](https://developer.microsoft.com/es-ES/windows), tiene acceso a todas las funcionalidades de Project Rome. El Centro de desarrollo de Windows también ofrece la *mejor* forma de administrar los cambios de la configuración de aplicación para varios dispositivos. Puede guardar las actualizaciones en un perfil existente de forma más segura hasta que tenga todo listo para publicar los cambios efectuados en producción. Cuando publique cambios en una aplicación para varios dispositivos existente en el Centro de desarrollo, el nuevo perfil será efectivo después de aproximadamente **una hora**.  

### <a name="externally-hosted-json-file-limited"></a>Archivo JSON hospedado externamente (limitado) 
Puede utilizar las siguientes funcionalidades de Project Rome en todas las plataformas compatibles con una aplicación para varios dispositivos administrada como archivo JSON hospedado externamente:  

* Leer y escribir actividades de usuario en todas las plataformas con la [API de fuente de actividades](/graph/api/resources/activity-feed-api-overview?view=graph-rest-1.0)
* Escriba actividades de usuario en todas las plataformas (Windows, iOS, Android, web) con los SDK de Project Rome.

Si **solo** tiene acceso a estas funcionalidades, puede hospedar la configuración de aplicación para varios dispositivos externamente en el dominio como archivo JSON.

## <a name="configure-a-cross-device-app-using-the-windows-dev-center"></a>Configurar una aplicación para varios dispositivos con el Centro de desarrollo de Windows
Un identificador de aplicación para varios dispositivos se representa como dominio de su propiedad. El dominio apunta a una asignación de los identificadores de aplicaciones específicos de su plataforma almacenados como archivo JSON hospedado en su dominio o configurable a través del Centro de desarrollo de Windows. Después de identificar el dominio que se usará para representar el identificador de aplicación para varios dispositivos, tendrá que recopilar información para configurar el perfil asociado. 

### <a name="step-1-select-a-secure-domain-for-your-cross-device-app-id-and-enable-domain-verification"></a>Paso 1: Seleccionar un dominio seguro para el identificador de aplicación para varios dispositivos y habilitar la comprobación del dominio
El dominio que utilice como identificador de aplicación para varios dispositivos tiene que ser un dominio de primer nivel o un subdominio y ha de protegerse mediante TLS. Por ejemplo: https://contoso.com o https://myapp.contoso.com, pero NO https://myapp.contoso.com/somepath. **Debe tener un dominio único (o subdominio) por aplicación para varios dispositivos.** Pero será usted quién decida qué aplicaciones se asocien a una sola aplicación para varios dispositivos en función del comportamiento multiplataforma que quiera compatibilizar. 

Por ejemplo, un desarrollador de aplicaciones con un conjunto de aplicaciones de juego podría utilizar un subdominio separado para cada una a fin de asegurarse de que cada aplicación solo se suscriba a las actividades de usuario que puede reanudar al leer datos en distintos dispositivos y plataformas. Por otro lado, un desarrollador de aplicaciones con un conjunto de aplicaciones de productividad diseñadas para trabajar juntas podría usar un solo dominio para todas, de modo que cualquier aplicación pueda iniciar un miembro del conjunto de aplicaciones en todos los dispositivos.  

#### <a name="assert-domain-ownership-with-the-windows-dev-center"></a>Declarar la propiedad del dominio con el Centro de desarrollo de Windows
Si usa el Centro de desarrollo de Windows para administrar la configuración de aplicación para varios dispositivos, el dominio que represente el identificador de aplicación para varios dispositivos se almacenará como parte del perfil de aplicación para varios dispositivos a fin de que Microsoft pueda comprobar que usted es el propietario del dominio. La propiedad del dominio **debe comprobarse** para terminar de publicar la configuración de aplicación para varios dispositivos, por lo que es conveniente abordar esto primero.Si aún no se ha comprobado el dominio, puede guardar los detalles de la aplicación para varios dispositivos y ejecutar de nuevo la comprobación después de completar este paso para poder publicar la aplicación para varios dispositivos.

Para declarar la propiedad del dominio de la aplicación para varios dispositivos, tendrá que agregar una entrada [TXT de DNS](https://go.microsoft.com/fwlink/?linkid=871417) para el dominio con un valor único que le proporcione el Centro de desarrollo. Este valor es único para cada aplicación para varios dispositivos. Para buscar el valor único de la aplicación, inicie sesión en el Centro de desarrollo de Windows y elija **Experiencias entre dispositivos** en el menú izquierdo para empezar a configurar una nueva aplicación y dispositivos. Cuando asigne un nombre a la nueva aplicación para varios dispositivos, seleccione **Verify your cross-device app domain** (Comprobar el dominio de la aplicación para varios dispositivos) en el submenú. En esta página se mostrarán instrucciones con un valor único  **insertado** (por ejemplo, MS=95ff4557-813f-45a5-b2f6-1f94170b979f). Asegúrese de copiar el valor completo, incluido "MS =".

### <a name="step-2-collect-your-platform-specific-application-ids"></a>Paso 2: Recopilar los identificadores de aplicación específicos de una plataforma
Recopile los identificadores de aplicación específicos de una plataforma para cada aplicación y plataforma que use las [API de Project Rome](/graph/api/resources/project-rome-overview?view=graph-rest-1.0).

Debe recopilar todos los identificadores de aplicación para varios dispositivos específicos de una plataforma para asociarlos a su identidad de aplicación para varios dispositivos. Con el Centro de desarrollo de Windows, podrá seleccionar entre las aplicaciones de la Plataforma universal de Windows (UWP) asociadas a su cuenta de desarrollador, pero tendrá que especificar manualmente los identificadores de aplicación de cualquiera de sus aplicaciones win32, iOS o Android e identificar la dirección URL principal de las aplicaciones web asociadas. Puede asociar hasta 10 identificadores por plataforma. 

Para buscar los identificadores:

* **windows_universal**: especifique un AUMID por aplicación para UWP. Para más información, vea [Find the Application User Model ID of an installed app (Industry 8.1)](https://docs.microsoft.com/en-us/previous-versions/windows/embedded/dn449300(v=winembedded.82)) (Buscar el identificador de modelo de usuario de la aplicación de una aplicación instalada [Industry 8.1]) y [Application](https://docs.microsoft.com/es-ES/uwp/schemas/appxpackage/appxmanifestschema/element-application) (Aplicación).
* **windows_win32**: especifique un AUMID por aplicación. En aplicaciones win32, tendrá que usar un script para recuperar esta información. Para más información, vea [Find the Application User Model ID of an installed app (Industry 8.1)](https://docs.microsoft.com/en-us/previous-versions/windows/embedded/dn449300(v=winembedded.82)) (Buscar el identificador de modelo de usuario de la aplicación de una aplicación instalada [Industry 8.1]).
* **android**: para más información, vea [Cambiar el nombre de paquete](https://developer.android.com/studio/build/application-id.html#change_the_package_name). 
* **ios**: para más información, vea [Bundle](https://developer.apple.com/documentation/foundation/bundle) y [Required, localizable, and editable properties](https://help.apple.com/itunes-connect/developer/#/devfc3066644) (Propiedades requeridas, localizables y editables).
* **msa**: inicie sesión en el [Portal de registro de aplicaciones](https://apps.dev.microsoft.com). Puede ver el identificador de aplicación y el identificador de cliente de cualquiera de las aplicaciones. Se admiten tanto los identificadores del SDK de Live (valores hexadecimales) como los de aplicaciones convergentes (GUID).   

### <a name="step-3-configure-support-for-microsoft-account-or-azure-ad"></a>Paso 3: Configurar la compatibilidad con una cuenta de Microsoft o de Azure AD
Para habilitar experiencias entre dispositivos, los usuarios de la aplicación deben iniciar sesión con una  [cuenta de Microsoft](https://account.microsoft.com/account) o una cuenta de [Azure Active Directory](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-developers-guide) (Azure AD). Especifique el identificador de aplicación y los identificadores de cliente para admitir la autenticación como parte de la configuración de aplicación para varios dispositivos a fin de habilitar la compatibilidad multiplataforma. Puede especificar un máximo de 10 instancias.

Para encontrar el identificador de aplicación y los identificadores de cliente existentes o aprovisionar unos nuevos, inicie sesión en el [Portal de registro de aplicaciones](https://apps.dev.microsoft.com) con su cuenta de desarrollador. Al iniciar sesión en el portal, puede ver el identificador de cliente y el identificador de aplicación de cualquiera de las aplicaciones. Se admiten tanto los identificadores del SDK de Live (valores hexadecimales) como los de aplicaciones convergentes (GUID).   

Si va a crear una aplicación que admite usuarios de Azure AD y no usa un identificador de aplicación convergente emitido por el [Portal de registro de aplicaciones](https://apps.dev.microsoft.com), tendrá que especificar el GUID del identificador de la aplicación de Azure. Para buscar el GUID del espacio empresarial: 

1. Inicie sesión en [Azure Portal](https://portal.azure.com). 
2. Seleccione **Azure Active Directory**.
3. En **Administrar**, seleccione **Registros de aplicaciones**. 
4. Seleccione la aplicación de la lista y vea el identificador de aplicación (GUID) que aparece en **Essentials**.

### <a name="step-4-configure-support-for-cross-platform-push-notifications-optional"></a>Paso 4: Configurar la compatibilidad con notificaciones de inserción multiplataforma (opcional) 
Si ha decidido configurar la aplicación para varios dispositivos en el Centro de desarrollo de Windows, puede habilitar la compatibilidad con notificaciones de inserción multiplataforma especificando las credenciales que usa con las API en las plataformas de mensajes de inserción iOS y Android. Estas son necesarias si usa los SDK de Project Rome para iOS y Android y quiere hacer algo más que publicar actividades de usuario. Si usa las API de Project Rome solo para Microsoft Graph, no necesita realizar este paso. Se pueden asociar hasta 10 conjuntos de credenciales por plataforma. 

>**Importante:** No almacene credenciales de notificación de inserción en un archivo JSON hospedado externamente.

Para buscar los identificadores:

* 
  **Servicio de notificaciones de Windows**: vea [Registering your app and receiving the credentials for your cloud service](https://docs.microsoft.com/en-us/previous-versions/windows/apps/hh913756(v=win.10)#registering-your-app-and-receiving-the-credentials-for-your-cloud-service) (Registrar la aplicación y recibir las credenciales del servicio en la nube) y el [Portal de registro de aplicaciones](https://apps.dev.microsoft.com).
* **Apple Push Notification Service**: vea [APNs Overview](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html) (Información general sobre el APNs).
* **Google Cloud Messaging**: vea [Firebase Cloud Messaging](https://firebase.google.com/docs/cloud-messaging/).

**Nota:** Si usa Firebase para enviar notificaciones a dispositivos iOS con credenciales de Android, deberá especificar las credenciales de APNs como parte de la configuración de aplicación para varios dispositivos. 

## <a name="configure-a-cross-device-app-using-an-externally-hosted-json-file"></a>Configurar una aplicación para varios dispositivos con un archivo JSON hospedado externamente
Un identificador de aplicación para varios dispositivos se representa como dominio de su propiedad. El dominio apunta a una asignación de los identificadores de aplicaciones específicos de su plataforma almacenados como archivo JSON hospedado en su dominio o configurable a través del Centro de desarrollo de Windows. Después de identificar el dominio que se usará para representar el identificador de aplicación para varios dispositivos, tendrá que recopilar información para configurar el perfil asociado. 

### <a name="step-1-select-a-secure-domain-for-your-cross-device-app-id"></a>Paso 1: Seleccionar un dominio seguro para el identificador de aplicación para varios dispositivos
Un identificador de aplicación para varios dispositivos se representa como dominio de su propiedad. Este tiene que ser un dominio de primer nivel o un subdominio y ha de protegerse mediante TLS. Por ejemplo: https://contoso.com o https://myapp.contoso.com, pero NO https://myapp.contoso.com/somepath. Debe tener un dominio único (o subdominio) por aplicación para varios dispositivos. Pero será usted quién decida qué aplicaciones se asocien a una sola aplicación para varios dispositivos en función del comportamiento multiplataforma que quiera compatibilizar. 

Por ejemplo, un desarrollador de aplicaciones con un conjunto de aplicaciones de juego podría utilizar un subdominio separado para cada una a fin de asegurarse de que cada aplicación solo se suscriba a las actividades de usuario que puede reanudar al leer datos en distintos dispositivos y plataformas. Un desarrollador de aplicaciones con un conjunto de aplicaciones de productividad diseñadas para trabajar juntas podría usar un solo dominio para todas, de modo que cualquier aplicación pueda iniciar un miembro del conjunto de aplicaciones en todos los dispositivos.  

#### <a name="assert-domain-ownership-with-an-externally-hosted-json-file"></a>Declarar la propiedad del dominio con un archivo JSON hospedado externamente 
Si usa un archivo JSON hospedado externamente para administrar la aplicación para varios dispositivos, declare la propiedad del dominio incluyendo su cuenta Microsoft o los identificadores de aplicación de Azure AD en el archivo cross-platform-app-identifiers. La propiedad del dominio se comprobará como parte del proceso de publicación cuando se usa la API de fuente de actividades para crear actividades de usuario.

El sistema almacenará el contenido del archivo JSON en caché para evitar que se generen solicitudes frecuentes en el dominio. Si se configura, el servicio respetará los encabezados HTTP de caché al evaluar cuándo actualizar la caché. Si no está configurado, el servicio se actualizará cada 24 horas. 

### <a name="step-2-collect-your-platform-specific-application-ids-and-construct-your-json-file"></a>Paso 2: Recopilar los identificadores de aplicación específicos de una plataforma y crear el archivo JSON
Recopile los identificadores de aplicación específicos de una plataforma para cada aplicación y plataforma que use la API de fuente de actividades o de retransmisión de dispositivo. 

Debe recopilar todos los identificadores de aplicación para varios dispositivos específicos de una plataforma para asociarlos a su identidad de aplicación para varios dispositivos. Si usa un archivo JSON hospedado externamente, tendrá que recopilar los identificadores de aplicación de cada una de las aplicaciones específicas de la plataforma para configurarlos como parte de la aplicación para varios dispositivos y agruparlos en el formato especificado. Puede asociar hasta 10 identificadores por plataforma. 

#### <a name="constructing-your-cross-platform-app-identifiers-file"></a>Crear el archivo cross-platform-app-identifiers
Es necesario que el propio archivo JSON tenga el nombre **cross-platform-app-identifiers** y se hospede en la raíz del dominio HTTPS. El contenido del archivo es una matriz JSON de asignaciones entre las plataformas admitidas por la aplicación y los identificadores de aplicación en esas plataformas. Al crear el archivo, incluya un objeto JSON para cada aplicación y plataforma que use las API de Project Rome. 
 
El archivo admite varios objetos JSON con el mismo identificador de plataforma. Por ejemplo, una aplicación para iPhone y una aplicación para iPad se mostrarán como objetos JSON independientes entre sí, cada uno con un valor de plataforma de iOS. El identificador de la plataforma web se muestra en el siguiente ejemplo.
 
No es necesario incluir un objeto JSON en todas las plataformas. Incluya solo objetos JSON en las plataformas en las que la aplicación utilice las API de Project Rome.Por ejemplo, si no tiene un cliente de la aplicación de la plataforma Android, no necesita una entrada en el archivo para Android.
 
En el ejemplo siguiente se incluyen todos los identificadores de plataforma válidos actualmente aceptados. Los objetos JSON que incluyan un valor de plataforma no válido se eliminarán.  

```[
{"platform":"windows_universal", "application":"Microsoft.Contoso_8wekyb3d8bbwe"},
{"platform":"windows_win32", "application":"DefaultBrowser_NOPUBLISHERID!Microsoft.Contoso.Default"},
{"platform":"android","application":"com.example.myapp"},
{"platform":"ios", "application":"com.example.myapp"},
{"platform":"web", "application":"https://contoso.com"},
{"platform":"web", "application":"https://chat.contoso.com"},
{"platform":"msa", "application":"00000000603E0BF"},
{"platform":"msa", "application":"48932b46-98b1-4020-9be4-cc7a65643c9e"},
]
```

Para buscar los identificadores:

* **windows_universal**: especifique un AUMID por aplicación para UWP. Para más información, vea [Find the Application User Model ID of an installed app (Industry 8.1)](https://docs.microsoft.com/en-us/previous-versions/windows/embedded/dn449300(v=winembedded.82)) (Buscar el identificador de modelo de usuario de la aplicación de una aplicación instalada [Industry 8.1]) y [Application](https://docs.microsoft.com/es-ES/uwp/schemas/appxpackage/appxmanifestschema/element-application) (Aplicación).
* **windows_win32**: especifique un AUMID por aplicación. En aplicaciones win32, tendrá que usar un script para recuperar esta información. Para más información, vea [Find the Application User Model ID of an installed app (Industry 8.1)](https://docs.microsoft.com/en-us/previous-versions/windows/embedded/dn449300(v=winembedded.82)) (Buscar el identificador de modelo de usuario de la aplicación de una aplicación instalada [Industry 8.1]).
* **android**: para más información, vea [Cambiar el nombre de paquete](https://developer.android.com/studio/build/application-id.html#change_the_package_name). 
* **ios**: para más información, vea [Bundle](https://developer.apple.com/documentation/foundation/bundle) y [Required, localizable, and editable properties](https://help.apple.com/itunes-connect/developer/#/devfc3066644) (Propiedades requeridas, localizables y editables).
* **msa**: inicie sesión en el [Portal de registro de aplicaciones](https://apps.dev.microsoft.com). Puede ver el identificador de aplicación y el identificador de cliente de cualquiera de las aplicaciones. Se admiten tanto los identificadores del SDK de Live (valores hexadecimales) como los de aplicaciones convergentes (GUID).   

### <a name="step-3-configure-support-for-microsoft-account-or-azure-ad"></a>Paso 3: Configurar la compatibilidad con una cuenta de Microsoft o de Azure AD
Para habilitar experiencias entre dispositivos, los usuarios de la aplicación deben iniciar sesión con una cuenta de Microsoft o una cuenta de Azure AD. Especifique el identificador de aplicación y los identificadores de cliente para admitir la autenticación como parte de la configuración de aplicación para varios dispositivos a fin de habilitar la compatibilidad multiplataforma. Puede especificar un máximo de 10 instancias.

```[
{"platform":"windows_universal", "application":"Microsoft.Contoso_8wekyb3d8bbwe"},
{"platform":"windows_win32", "application":"DefaultBrowser_NOPUBLISHERID!Microsoft.Contoso.Default"},
{"platform":"android","application":"com.example.myapp"},
{"platform":"ios", "application":"com.example.myapp"},
{"platform":"web", "application":"https://contoso.com"},
{"platform":"web", "application":"https://chat.contoso.com"},
{"platform":"msa", "application":"00000000603E0BF"},
{"platform":"msa", "application":"48932b46-98b1-4020-9be4-cc7a65643c9e"},
]
```

Para encontrar el identificador de aplicación y los identificadores de cliente existentes o aprovisionar unos nuevos, inicie sesión en el  [Portal de registro de aplicaciones](https://apps.dev.microsoft.com) con su cuenta de desarrollador. Al iniciar sesión, puede ver el identificador de cliente y el identificador de aplicación de cualquiera de las aplicaciones. Se admiten tanto los identificadores del SDK de Live (valores hexadecimales) como los de aplicaciones convergentes (GUID). Use el tipo de plataforma "msa" al agregar los identificadores utilizados para habilitar la compatibilidad con una cuenta de Microsoft o de Azure AD, tal y como se muestra en el ejemplo anterior.  

>**Nota:** Si va a crear una aplicación que admite usuarios de Azure AD y no usa un identificador de aplicación convergente emitido por el  [Portal de registro de aplicaciones](https://apps.dev.microsoft.com), tendrá que proporcionar el GUID del identificador de la aplicación de Azure. Este tipo de identificador también debería configurarse como tipo de plataforma "msa". 

Para encontrar el GUID del espacio empresarial en Azure Portal: 

1. Inicie sesión en [Azure Portal](https://portal.azure.com).
2. Seleccione **Azure Active Directory**. 
3. En **Administrar**, seleccione **Registros de aplicaciones**.
4. Seleccione la aplicación de la lista. El identificador de aplicación (GUID) puede verse en **Essentials**.

#### <a name="encoding-the-cross-platform-app-identifiers-file"></a>Codificar el archivo cross-platform-app-identifiers 
Si no ve que las actividades se reanudan en las aplicaciones nativas correctas en todas las plataformas, o no puede leer las actividades publicadas por todos los miembros del grupo, es posible que el archivo JSON no se esté analizando adecuadamente. Al generar este archivo, asegúrese de guardar el archivo cross-platform-app-identifiers con codificación "Unicode (UTF-8 sin signatura) - Página de códigos 65001".

#### <a name="updating-the-cross-platform-app-identifiers-json-file"></a>Actualizar el archivo JSON cross-platform-app-identifiers 
El sistema almacenará el contenido del archivo JSON en caché para evitar que se generen solicitudes frecuentes en el dominio. Si se configura, el servicio respetará los encabezados HTTP de caché al evaluar cuándo actualizar la caché. Si no está configurado, el servicio se actualizará cada 24 horas. 

## <a name="configure-your-app-client"></a>Configurar el cliente de la aplicación 
Si utiliza las API del lado cliente para Windows, iOS o Android, tendrá que asegurarse de que el cliente de la aplicación esté configurado con el valor del host que representa la identidad de la aplicación para varios dispositivos (por ejemplo, contoso.com).

### <a name="microsoft-graph-apps"></a>Aplicaciones de Microsoft Graph 
Si tiene una aplicación que usa la API de fuente de actividades en Microsoft Graph, tiene que especificar el valor de host en la propiedad **activitySourceHost**. Para más información, vea [activity resource type](/graph/api/resources/projectrome-activity?view=graph-rest-1.0) (tipo de recurso de actividad).

### <a name="universal-windows-apps"></a>Aplicaciones universales de Windows
Si tiene una aplicación de Windows, debe configurar el valor de host en el manifiesto de la aplicación antes de publicar los datos. Para más información, vea [uap5:UserActivity](https://docs.microsoft.com/es-ES/uwp/schemas/appxpackage/uapmanifestschema/element-uap5-useractivity). 

<!-- Removing until we add the details.
### iOS & Android apps
*Details coming soon.*
-->

## <a name="maintaining-your-cross-device-app-configuration"></a>Mantener la configuración de aplicación para varios dispositivos
Al publicar una nueva aplicación que genere actividades de usuario, es importante actualizar con antelación la aplicación para varios dispositivos con los nuevos valores de configuración para que las nuevas actividades que se publiquen se asocien correctamente a la aplicación para varios dispositivos. La configuración de aplicación para varios dispositivos asociada a las actividades de usuario que se han publicado antes de un cambio de configuración no se actualizará automáticamente. Pero una operación de actualización que se realice en cualquier actividad con una configuración anterior se actualizará a la versión más reciente del archivo.  

## <a name="troubleshooting"></a>Solución de problemas

Estos son algunos problemas comunes que pueden producirse con la API de fuente de actividades.

### <a name="activities-are-not-available-to-read-and-write-for-all-apps-in-the-cross-device-app-configuration"></a>Las actividades de lectura y escritura no están disponibles para todas las aplicaciones en la configuración de aplicación para varios dispositivos
La API de fuente de actividades ingiere la configuración de aplicación para varios dispositivos asincrónicamente, por lo que es posible que los errores de configuración no sean evidentes al publicar las actividades de usuario. En caso de que el servicio no pueda ingerir el archivo JSON, ya sea debido a un error de formato o de TLS, las actividades que se hayan publicado se atribuirán solo al ID de aplicación que publicó la actividad. En el caso de actividades publicadas a través de Microsoft Graph, se trata del identificador de aplicación de la cuenta de Microsoft utilizado para autorizar solicitudes a Microsoft Graph. En el caso de actividades publicadas a través de las API del lado cliente, activity.applicationId solo registrará el identificador de aplicación específico de la plataforma que publicó la actividad. Esto impedirá leer y escribir operaciones en actividades de cualquier otra aplicación específica de la plataforma que se identifique en la configuración de aplicación para varios dispositivos. 

### <a name="platform-will-not-initialize-on-android-or-ios"></a>La plataforma no se inicializará en Android o iOS
La API de retransmisión de dispositivos para Android o iOS requiere la configuración de aplicación para varios dispositivos para crear instancias de conexiones a la aplicación Android o iOS. En caso de que no se pueda iniciar correctamente la plataforma, asegúrese de haber identificado correctamente los identificadores de aplicación y las credenciales de notificación de inserción de la cuenta de Microsoft empleada al configurar la aplicación para varios dispositivos en el Centro de desarrollo de Windows y configure el valor de host de las aplicaciones cliente con el dominio que identifica la aplicación para varios dispositivos. 
