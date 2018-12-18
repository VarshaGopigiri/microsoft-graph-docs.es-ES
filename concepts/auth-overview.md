---
title: Obtener tokens de acceso para llamar a Microsoft Graph
description: 'Para llamar a Microsoft Graph, su aplicación debe adquirir un token de acceso de Azure Active Directory (Azure AD), el servicio de identidad en la nube de Microsoft. El token de acceso contiene información (o notificaciones) sobre la aplicación y los permisos que tiene para los recursos y las API disponibles a través de Microsoft Graph. Para obtener un token de acceso, la aplicación debe poder autenticarse con Azure AD y disponer de la autorización de un usuario o un administrador para tener acceso a los recursos de Microsoft Graph que necesita. '
author: jackson-woods
ms.openlocfilehash: 2352802393d3e36c611dfab1d767e6bd76d69d8b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334304"
---
# <a name="get-access-tokens-to-call-microsoft-graph"></a>Obtener tokens de acceso para llamar a Microsoft Graph

Para llamar a Microsoft Graph, su aplicación debe adquirir un token de acceso de Azure Active Directory (Azure AD), el servicio de identidad en la nube de Microsoft. El token de acceso contiene información (o notificaciones) sobre la aplicación y los permisos que tiene para los recursos y las API disponibles a través de Microsoft Graph. Para obtener un token de acceso, la aplicación debe poder autenticarse con Azure AD y disponer de la autorización de un usuario o un administrador para tener acceso a los recursos de Microsoft Graph que necesita. 

En este tema se proporciona información general sobre los tokens de acceso, Azure AD y la manera en que la aplicación puede obtener tokens de acceso. Si ya está familiarizado con la integración de una aplicación con Azure AD para obtener tokens, puede ir directamente a [Pasos siguientes](#next-steps) para obtener información y ejemplos específicos de Microsoft Graph. 

> **Importante:**  Cómo se aplican las directivas de acceso condicional a Microsoft Graph es algo que está cambiando. Las aplicaciones deben actualizarse para administrar los escenarios donde se configuran las directivas de acceso condicional. Para obtener más información y directrices, vea [Instrucciones para desarrolladores para Acceso condicional de Azure Active Directory](https://docs.microsoft.com/azure/active-directory/develop/active-directory-conditional-access-developer).

## <a name="what-is-an-access-token-and-how-do-i-use-it"></a>¿Qué es un token de acceso y cómo se usa?

Los tokens de acceso emitidos por Azure AD son JSON Web Tokens (JWT) codificados en base 64. Contienen información (notificaciones) que las API web protegidas por Azure AD, como Microsoft Graph, usan para validar al llamador y para garantizar que este tiene los permisos adecuados para realizar la operación que solicita. Al llamar a Microsoft Graph, puede tratar los tokens de acceso como opacos. Siempre debe transmitir los tokens de acceso por un canal seguro, como Seguridad de la capa de transporte (HTTPS).

A continuación se muestra un ejemplo de un token de acceso de Azure AD:

`EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==`

Para llamar a Microsoft Graph, asocie el token de acceso como token de portador al encabezado de autorización de una solicitud HTTP. Por ejemplo, a continuación se muestra una llamada que devuelve la información de perfil del usuario que ha iniciado sesión (el token de acceso se ha truncado para mejorar la legibilidad):

```
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: graph.microsoft.com`
GET https://graph.microsoft.com/v1.0/me/
```

## <a name="what-are-microsoft-graph-permissions"></a>¿Qué son los permisos de Microsoft Graph?
Microsoft Graph expone un amplio conjunto de permisos pormenorizados para los recursos que controla. Estos permisos se expresan como cadenas y conceden a las aplicaciones acceso a los recursos de Microsoft Graph, como usuarios, grupos, correo de usuario, etc. Por ejemplo:

- _User.Read_ permite que una aplicación lea el perfil del usuario que ha iniciado sesión.
- _Mail.Send_ permite que una aplicación envíe correos en nombre del usuario que ha iniciado sesión.

Existen dos tipos de permisos:

- Los permisos delegados los usan las aplicaciones que se ejecutan con un usuario presente. Los privilegios del usuario se delegan a la aplicación, que realiza llamadas en nombre del usuario a Microsoft Graph. El usuario puede aceptar muchos de estos permisos, pero otros requieren el consentimiento del administrador.  
- Los permisos de la aplicación los usan las aplicaciones que se ejecutan sin un usuario. Estos suelen conceder a una aplicación amplios privilegios dentro de la organización y siempre requieren el consentimiento de un administrador.

Para obtener una lista completa de los permisos de Microsoft Graph, así como las diferencias entre los permisos delegados y de la aplicación, vea la [Referencia de permisos](permissions-reference.md).

## <a name="where-does-my-app-get-an-access-token"></a>¿Dónde obtiene mi aplicación un token de acceso?
Su aplicación obtiene tokens de acceso de Azure Active Directory (Azure AD), el servicio de identidad en la nube de Microsoft. Para obtener un token de acceso, la aplicación intercambia solicitudes y respuestas HTTP con Azure AD mediante protocolos estándar del sector definidos en las especificaciones OAuth 2.0 y OpenID Connect 1.0. Estos protocolos describen los puntos de conexión de Azure AD y los intercambios con ellos (o flujos de autenticación) que la aplicación usa para autenticarse de forma segura con Azure AD y obtener tokens de acceso.  

En pocas palabras, para obtener un token de acceso, la aplicación intercambia solicitudes HTTP con los puntos de conexión siguientes:

- El punto de conexión `/authorize`, adonde la aplicación puede enviar a un usuario para autenticarse con Azure AD y dar su consentimiento a los permisos que la aplicación necesita.
- El punto de conexión `/token`, donde la aplicación puede obtener un token de acceso una vez que se ha concedido el consentimiento del usuario.

(Nota: Estas definiciones son flexibles. Según el protocolo que use la aplicación, esta puede obtener tokens de acceso directamente del punto de conexión `/authorize` o puede autenticarse directamente con el punto de conexión `/token`). 

A continuación se muestra un ejemplo de un conjunto de los puntos de conexión `/authorize` y `/token` expuestos por Azure AD v2.0:

```
https://login.microsoftonline.com/common/oauth2/v2.0/authorize
https://login.microsoftonline.com/common/oauth2/v2.0/token

```
Azure AD expone dos conjuntos de puntos de conexión, Azure AD y Azure AD v2.0. La diferencia principal entre ellos es que el punto de conexión de Azure AD solo admite cuentas profesionales o educativas (es decir, cuentas asociadas a un inquilino de Azure AD), mientras que Azure AD v2.0 también admite cuentas de Microsoft, como cuentas de _Live.com_ o _outlook.com_. Esto significa que si usa el punto de conexión de Azure AD, su aplicación solo puede tener como destino organizaciones, pero con Azure AD v2.0 puede tener como destino tanto consumidores como organizaciones. 

Los tokens del punto de conexión de Azure AD no se pueden intercambiar con los del punto de conexión de Azure AD v2.0. Por esta razón, antes de empezar a trabajar en una aplicación para la producción, debe elegir un tipo de puntos de conexión. Dado que el punto de conexión de Azure AD v2.0 es más reciente y todavía se le están agregando características, existen algunas limitaciones importantes que debe tener en cuenta al decidir qué punto de conexión usará para la aplicación en producción. Para obtener más información, vea [Decidir entre los puntos de conexión de Azure AD y Azure AD v2.0](#deciding-between-the-azure-ad-and-azure-ad-v20-endpoints).

## <a name="whats-the-difference-between-oauth-20-and-openid-connect"></a>¿Cuál es la diferencia entre OAuth 2.0 y OpenID Connect?

OAuth 2.0 es un protocolo de autorización. Define la forma en que la aplicación puede obtener tokens de acceso mediante la autenticación directa con Azure AD o mediante el redireccionamiento de un usuario para que se autentique con Azure AD y dé su consentimiento a los permisos que la aplicación solicita. En el primer caso, la aplicación obtiene un token de acceso que puede usar para llamar a Microsoft Graph por sí misma. En el segundo caso, la aplicación obtiene un token de acceso que puede usar para llamar a Microsoft Graph en nombre de un usuario. En cambio, con OAuth 2.0, la aplicación no recibe información sobre el usuario ni sobre la manera en que lo ha autenticado Azure AD. Los flujos de OAuth 2.0 suelen usarlos las aplicaciones móviles o nativas, que ya conocen la identidad del usuario, o aplicaciones como servicios en segundo plano o demonios, que llaman a Microsoft Graph con su propia identidad y no en nombre de un usuario.

OpenID Connect extiende OAuth 2.0 para proporcionar un nivel de identidad. Con OpenID Connect, además de un token de acceso, la aplicación también puede obtener un token de identificación de Azure AD. Los tokens de identificación de OpenID Connect contienen notificaciones sobre la identidad del usuario y detalles sobre cómo y dónde se ha autenticado. Los flujos de OpenID Connect suelen usarlos las aplicaciones web, incluidas las aplicaciones de página única (SPA). Estas aplicaciones pueden usar el token de identificación para personalizar su comportamiento para el usuario para el que han solicitado un token de acceso y, en muchos casos, delegan el inicio de sesión de sus usuarios en Azure AD y permiten experiencias como el inicio de sesión único (SSO).

## <a name="what-kind-of-apps-can-i-call-microsoft-graph-from"></a>¿Desde qué aplicaciones puedo llamar a Microsoft Graph?
Puede llamar a Microsoft Graph desde los siguientes tipos de aplicaciones: 

- **Aplicaciones nativas**: aplicaciones que se ejecutan en un dispositivo, como un dispositivo de escritorio, una tableta o un teléfono móvil. Estas aplicaciones usan el sistema operativo (SO) nativo del dispositivo, como iOS, Android o Windows, para la presentación del usuario y para realizar llamadas a Microsoft Graph en nombre de un usuario.
- **Aplicaciones web**: aplicaciones que se ejecutan en un servidor e interactúan con el usuario que ha iniciado sesión a través de un agente de usuario, normalmente un explorador web. La mayor parte del nivel de presentación se controla en el servidor, y las llamadas a Microsoft Graph se realizan desde el servidor en nombre de un usuario.
- **Aplicaciones de página única (SPA)**: aplicaciones web con experiencias de usuario enriquecidas que controlan gran parte del nivel de presentación mediante scripting del lado cliente en el explorador. Las llamadas a Microsoft Graph se realizan desde scripts del lado cliente mediante tecnologías como AJAX y marcos como Angular.js. Las llamadas se realizan en nombre de un usuario.
- **Servicios y demonios en segundo plano**: servicios y demonios en segundo plano que se ejecutan en un servidor sin la presencia de un usuario y realizan llamadas a Microsoft Graph con su propia identidad.
- **API web**: una aplicación cliente llama a una API web (protegida por Azure AD) que, después, llama a Microsoft Graph, todo ello en nombre de un usuario. Es compatible con el punto de conexión de Azure AD. Para el punto de conexión de Azure AD v2.0, solo se admite si el cliente y la API web tienen el mismo id. de aplicación (por ejemplo, una aplicación nativa que realiza una llamada al back-end de una API web). 

## <a name="how-do-i-get-my-app-talking-to-azure-ad-and-microsoft-graph"></a>¿Cómo consigo que mi aplicación se comunique con Azure AD y Microsoft Graph?
Para que la aplicación pueda obtener un token de Azure AD, debe estar registrada. En el caso del punto de conexión de Azure AD v2.0, use el [Portal de registro de aplicaciones de Microsoft](https://apps.dev.microsoft.com/) para registrar su aplicación. En el caso del punto de conexión de Azure AD, use [Azure Portal](https://portal.azure.com/). Mediante el registro, la aplicación se integra con Azure AD y se establecen las coordenadas y los identificadores que usa para obtener tokens. Son:

- **Id. de aplicación**: identificador único asignado por Azure AD. 
- **URI/URL de redireccionamiento**: uno o más puntos de conexión en los que la aplicación recibirá respuestas de Azure AD. (En el caso de las aplicaciones móviles y nativas, es un URI asignado por Azure AD).
- **Secreto de aplicación**: contraseña o par de claves pública y privada que la aplicación usa para autenticarse con Azure AD. (No necesario para aplicaciones móviles o nativas).

En el caso de las aplicaciones que usan el punto de conexión de Azure AD, también se configurarán previamente los permisos de Microsoft Graph que la aplicación necesita durante el registro. En el caso de las aplicaciones que usan el punto de conexión de Azure AD v2.0, puede necesitar o no configurar previamente los permisos. 

Las propiedades configuradas durante el registro se usan en la conexión. Por ejemplo, en la siguiente solicitud de token: *client_id* es el *id. de aplicación*; *redirect_uri* es uno de los *URI de redireccionamiento* registrados de la aplicación; y *client_secret* es el *secreto de aplicación*. 

```
// Line breaks for legibility only

POST /common/oauth2/v2.0/token HTTP/1.1
Host: https://login.microsoftonline.com
Content-Type: application/x-www-form-urlencoded

client_id=6731de76-14a6-49ae-97bc-6eba6914391e
&scope=user.read%20mail.read
&code=OAAABAAAAiL9Kn2Z27UubvWFPbm0gLWQJVzCTE9UkP3pSx1aXxUjq3n8b2JRLk4OxVXr...
&redirect_uri=http%3A%2F%2Flocalhost%2Fmyapp%2F
&grant_type=authorization_code
&client_secret=JqQX2PNo9bpM0uEihUPzyrh    // NOTE: Only required for web apps
```

## <a name="are-there-authentication-libraries-available"></a>¿Hay disponibles bibliotecas de autenticación?
Al igual que la mayoría de los desarrolladores, probablemente usará bibliotecas de autenticación para administrar las interacciones con Azure AD. Las bibliotecas de autenticación extraen muchos detalles del protocolo del desarrollador, como la validación, la administración de cookies, el almacenamiento en caché de tokens y el mantenimiento de conexiones seguras, lo que le permite centrarse en el desarrollo de la aplicación. Microsoft publica bibliotecas de cliente de código abierto y software intermedio de servidor para los puntos de conexión de Azure AD y Azure AD v2.0. 

Para el punto de conexión de Azure AD v2.0: 

- Hay bibliotecas de cliente de la Biblioteca de autenticación de Microsoft (MSAL) disponibles para. NET, JavaScript, Android y Objective-C. Todas las plataformas se encuentran en versión preliminar compatible con la producción y, en el caso de que se introduzcan cambios importantes, Microsoft garantiza una ruta de actualización.
- El software intermedio de servidor de Microsoft está disponible para .NET Core y ASP.NET (OpenID Connect y OAuth de OWIN) y para Node.js (Passport.js de Microsoft Azure AD). 
- El punto de conexión de v2.0 es compatible con muchas bibliotecas de autenticación de terceros.

Para obtener una lista completa de las bibliotecas de cliente de Microsoft, el software intermedio de servidor de Microsoft y las bibliotecas de terceros compatibles, vea [Bibliotecas de autenticación de Azure Active Directory v2.0](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-libraries).

Para el punto de conexión de Azure AD:

- Hay bibliotecas de cliente de la Biblioteca de autenticación de Active Directory (ADAL) disponibles en un número ligeramente mayor de plataformas. 
- El software intermedio de servidor de Microsoft está disponible para .NET Core y ASP.NET, así como Node.js. 

Para obtener una lista completa de las bibliotecas de cliente de Microsoft y el software intermedio de servidor, vea [Bibliotecas de autenticación de Azure Active Directory](https://docs.microsoft.com/azure/active-directory/develop/active-directory-authentication-libraries).

## <a name="deciding-between-the-azure-ad-and-azure-ad-v20-endpoints"></a>Decidir entre los puntos de conexión de Azure AD y Azure AD v2.0

Azure AD expone dos conjuntos de puntos de conexión, Azure AD y Azure AD v2.0, donde puede obtener tokens de acceso para usarlos al llamar a Microsoft Graph. Los tokens recibidos de cada punto de conexión no son intercambiables. Para ejecutar ejemplos o explorar las funcionalidades de Microsoft Graph, la elección de los puntos de conexión de Azure AD no es importante. Pero antes de comenzar el desarrollo de una aplicación de producción, debe decidir qué punto de conexión es más adecuado para el escenario. En la descripción siguiente se proporcionan instrucciones generales que pueden ayudarle a tomar una decisión, pero para conocer la información más actual y completa debe ver el tema [¿Debo usar el punto de conexión v2.0?](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-limitations) en la documentación de Azure Active Directory. 

Las principales diferencias entre Azure AD y Azure AD v2.0 son las siguientes:

* Azure AD solo admite cuentas profesionales o educativas, es decir, cuentas asociadas con un inquilino de Azure AD. Esto significa que la aplicación solo puede tener como destino organizaciones.
* Azure AD v2.0 admite cuentas profesionales y educativas y cuentas de Microsoft, como cuentas de _live.com_ o _outlook.com_. Esto significa que la aplicación puede tener como destino tanto consumidores como organizaciones que usen el punto de conexión v2.0. 

Existen algunas ventajas adicionales con Azure AD v2.0. Por ejemplo:

* La aplicación puede usar un mismo id. de aplicación para varias plataformas. Esto simplifica la administración de aplicaciones para desarrolladores y administradores.
* [Compatibilidad con el consentimiento dinámico e incremental](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-compare#incremental-and-dynamic-consent). Con esta característica, la aplicación puede solicitar permisos adicionales durante el tiempo de ejecución y emparejar la solicitud de consentimiento del usuario con la funcionalidad que lo requiere. Esto proporciona una experiencia mucho más cómoda para los usuarios que tener que dar su consentimiento a una larga lista de permisos cuando inician sesión por primera vez.  

Dado que Azure AD v2.0 es más reciente que Azure AD y todavía se le están agregando características, existen algunas limitaciones en el punto de conexión v2.0 que debe tener en cuenta al tomar una decisión. Por ejemplo:

* Algunas características podrían no estar todavía completamente implementadas en v2.0. Por ejemplo, es posible que la aplicación no funcione si su cliente empresarial activa características de seguridad de movilidad empresarial, como el [acceso condicional al dispositivo](https://azure.microsoft.com/documentation/articles/active-directory-conditional-access-device-policies).
* No puede llamar a Microsoft Graph desde una [API web independiente](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-limitations#restrictions-on-app-types). 
* No puede llamar a aplicaciones del Proveedor de soluciones en la nube.
* No se admite la [autenticación integrada de Windows para los inquilinos federados](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-limitations#restrictions-for-work-and-school-accounts). Esto significa que los usuarios de inquilinos federados de Azure AD no podrán autenticarse silenciosamente con su instancia de Active Directory local. Tendrán que volver a especificar sus credenciales.

Para obtener más información sobre las diferencias entre el punto de conexión de Azure AD v2.0 y el de Azure AD, vea [¿Qué hay diferente en el punto de conexión v2.0?](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-compare)

>**Importante**
>
>**Antes de tomar una decisión sobre qué punto de conexión va a usar al desarrollar una aplicación para la producción, vea [¿Debo usar el punto de conexión v2.0?](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-limitations).**

## <a name="next-steps"></a>Pasos siguientes

Una vez que haya registrado la aplicación, ya puede empezar a trabajar.

- Para conocer los pasos rápidos para conseguir un token de acceso para aplicaciones que llaman a Microsoft Graph en nombre de un usuario, vea [Get access on behalf of users](auth-v2-user.md) (Obtener acceso en nombre de los usuarios).
- Para conocer los pasos rápidos para conseguir un token de acceso para aplicaciones que llaman a Microsoft Graph sin un usuario, vea [Get access without a user](auth-v2-service.md) (Obtener acceso sin un usuario).
- Para ver los permisos que se pueden usar con Microsoft Graph, vea la referencia sobre los [permisos](permissions-reference.md).
- Si es un Proveedor de soluciones en la nube de Microsoft y le interesa tener acceso a los datos de clientes administrados por el asociado a través de Microsoft Graph, vea [Manage app access (CSPs)](auth-cloudsolutionprovider.md) (Administrar el acceso de la aplicación (CSP)).


Si ya está listo para ir directamente al código, puede usar los recursos siguientes como ayuda para implementar la autenticación y la autorización con Azure AD en la aplicación.

### <a name="microsoft-graph-training-and-samples"></a>Aprendizaje y ejemplos de Microsoft Graph
Para ayudarle a empezar a trabajar rápidamente, hemos creado una serie de módulos de aprendizaje y otros recursos que muestran cómo autenticar y usar la API en una amplia variedad de plataformas. 

- Use la página [Introducción](https://developer.microsoft.com/es-ES/graph/get-started) para obtener ejemplos, bibliotecas, contenido de aprendizaje y otros recursos de su plataforma favorita. 
- Para ponerlo todo en marcha rápidamente con una muestra preconfigurada de la plataforma, consulte el [inicio rápido de Microsoft Graph](https://developer.microsoft.com/es-ES/graph/quick-start).
- Explore nuestros [ejemplos de Microsoft Graph](https://github.com/microsoftgraph?utf8=%E2%9C%93&q=sample&type=&language=) en GitHub.


### <a name="azure-active-directory-samples-and-documentation"></a>Ejemplos y documentación de Azure Active Directory 
La documentación de Azure AD contiene artículos y ejemplos que se centran específicamente en la autenticación y la autorización con Azure AD.

Para el punto de conexión de Azure AD v2.0: 

- El mejor punto de partida es la [documentación del punto de conexión de Azure AD v2.0](https://docs.microsoft.com/azure/active-directory/develop/active-directory-appmodel-v2-overview). Este artículo contiene vínculos a información general, documentación de protocolos y artículos de introducción para diversas plataformas, todo ello organizado según el tipo de aplicación que se desarrolle. 
- Para obtener ejemplos ordenados por biblioteca de autenticación de cliente o de servidor, vea [Bibliotecas de autenticación de Azure Active Directory v2.0](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-libraries). 
- También puede explorar ejemplos de Azure AD por plataforma en la [Galería de código de Azure](https://azure.microsoft.com/resources/samples/?service=active-directory). Nota: No se puede organizar la búsqueda por versión del punto de conexión. 

Para el punto de conexión de Azure AD: 

- El mejor punto de partida es [Azure Active Directory para desarrolladores](https://docs.microsoft.com/azure/active-directory/develop/active-directory-developers-guide). Este artículo contiene vínculos a información general, documentación de protocolos y artículos de introducción para diversas plataformas, todo ello organizado según el tipo de aplicación que se desarrolle. 
- Para consultar los ejemplos ordenados por biblioteca de autenticación de cliente o de servidor, vea [Bibliotecas de autenticación de Azure Active Directory](https://docs.microsoft.com/azure/active-directory/develop/active-directory-authentication-libraries). 
- Para obtener ejemplos organizados por tipo de aplicación y plataforma, vea [Ejemplos de código de Azure Active Directory](https://docs.microsoft.com/azure/active-directory/develop/active-directory-code-samples).
- También puede explorar ejemplos de Azure AD por plataforma en la [Galería de código de Azure](https://azure.microsoft.com/resources/samples/?service=active-directory). Nota: No se puede organizar la búsqueda por versión del punto de conexión. 


## <a name="see-also"></a>Recursos adicionales

- [Documentación sobre el punto de conexión de Azure Active Directory](https://docs.microsoft.com/azure/active-directory/develop/active-directory-developers-guide)
- [Documentación sobre el punto de conexión de Azure Active Directory v2.0](https://docs.microsoft.com/azure/active-directory/develop/active-directory-appmodel-v2-overview)
