---
title: Información general de Microsoft Graph
description: " Seguridad y Windows 10. "
ms.openlocfilehash: 7d8ed0d16ed24e20d1b48a1e44f573dce24d838f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092826"
---
# <a name="overview-of-microsoft-graph"></a>Información general de Microsoft Graph

Microsoft Graph es la puerta de enlace a datos y la inteligencia de Microsoft 365. Microsoft Graph proporciona un modelo de programación unificado que puede usar para aprovechar la gran cantidad de datos en Office 365, Enterprise Mobility + Security y Windows 10. 

Puede usar la API de Microsoft Graph para crear aplicaciones para las organizaciones y los consumidores que interactúan con los datos de millones de usuarios. Con Microsoft Graph, puede conectarse a una gran cantidad de recursos, relaciones e información, todo ello a través de un único punto de conexión: `https://graph.microsoft.com`.

## <a name="whats-in-the-graph"></a>¿Qué contiene el gráfico?
Microsoft Graph expone las API de REST y las bibliotecas de cliente para tener acceso a estos datos:

- Azure Active Directory
- Servicios de Office 365: SharePoint, OneDrive, Exchange y Outlook, Microsoft Teams, OneNote, Planner y Excel
- Servicios de Enterprise Mobility + Security: Identity Manager, Intune, Advanced Threat Analytics y protección contra amenazas avanzada.
- Servicios de Windows 10: actividades y dispositivos
- Educación

Para obtener más información, consulte [Principales servicios y características de Microsoft Graph](overview-major-services.md).

Microsoft Graph se conecta a todos los recursos en estos servicios mediante relaciones. Por ejemplo, un usuario puede conectarse a un grupo mediante una relación [memberOf](/graph/api/user-list-memberof?view=graph-rest-1.0) y a otro usuario a través de una [relación manager](/graph/api/user-list-manager?view=graph-rest-1.0). Su aplicación puede conectar estas relaciones para acceder a estos recursos conectados y realizar acciones en ellos a través de la API.

Desde Microsoft Graph, también puede obtener valiosas conclusiones e información sobre los datos. Por ejemplo, puede obtener los archivos populares [del entorno de](/graph/api/resources/insights-trending?view=graph-rest-beta) un usuario en particular o sus [contactos más relevantes](/graph/api/user-list-people?view=graph-rest-beta).

Descubra las posibilidades que ofrecen las relaciones en Microsoft Graph.

![Una imagen en la que se muestran los recursos y relaciones principales que forman parte del gráfico](images/microsoft-graph.png)

## <a name="what-can-you-do-with-microsoft-graph"></a>¿Qué puede hacer con Microsoft Graph? 

Puede usar Microsoft Graph para crear experiencias en torno al contexto único del usuario para ayudarle a aumentar su productividad. Imagine una aplicación que...

- Comprueba cuál es su próxima reunión y le ayuda a prepararse para ella proporcionándole la información de perfil de los asistentes, incluidos sus puestos y sus compañeros de trabajo, así como información sobre los documentos y los proyectos más recientes en los que trabajan.
- Examina su calendario y sugiere las mejores horas para la siguiente reunión de equipo.
- Captura el gráfico de proyección de ventas más recientes de un archivo de Excel en su OneDrive y le permite actualizar la previsión en tiempo real (todo ello desde el teléfono).
- Se suscribe a los cambios del calendario, le envía una alerta cuando está dedicando demasiado tiempo a reuniones y proporciona recomendaciones para las reuniones que se puede saltar o que podría delegar en función de lo relevantes que considere que son los asistentes.
- Le ayuda a ordenar la información personal y la laboral en su teléfono mediante acciones como la clasificación de las imágenes que deberían almacenarse en su OneDrive personal y de los documentos empresariales que deberían almacenarse en su OneDrive para la Empresa.

Puede realizar todas estas acciones, entre otras, con la API de Microsoft Graph.

>**Note:** Al usar la API de Microsoft Graph, acepta las [Condiciones de uso de Microsoft Graph](https://developer.microsoft.com/graph/docs/misc/terms-of-use) y la [Declaración de privacidad de Microsoft](https://go.microsoft.com/fwlink/?LinkId=521839).

### <a name="popular-requests"></a>Solicitudes populares

Consulte algunos escenarios comunes para trabajar con la API de Microsoft Graph. Los vínculos le llevan al [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).

| **Operación** | **URL** |
|:--------------------------|:----------------------------------------|
|   OBTENER mi perfil |    [`https://graph.microsoft.com/v1.0/me`](https://developer.microsoft.com/graph/graph-explorer/?request=me&version=v1.0) |
|   OBTENER mis archivos | [`https://graph.microsoft.com/v1.0/me/drive/root/children`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fdrive%2Froot%2Fchildren&version=v1.0) |
|   OBTENER mi foto | [`https://graph.microsoft.com/v1.0/me/photo/$value`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fphoto%2F%24value&version=v1.0) |
|   OBTENER mi correo |   [`https://graph.microsoft.com/v1.0/me/messages`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fmessages&version=v1.0) |
|   OBTENER mi correo electrónico de importancia alta | [`https://graph.microsoft.com/v1.0/me/messages?$filter=importance%20eq%20'high'`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fmessages%3F%24filter%3Dimportance%2520eq%2520'high'&version=v1.0) |
|   OBTENER mis eventos de calendario |    [`https://graph.microsoft.com/v1.0/me/events`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fevents&version=v1.0) |
|   OBTENER mi administrador  | [`https://graph.microsoft.com/v1.0/me/manager`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fmanager&version=v1.0) |
|   OBTENER el último usuario que modificó el archivo foo.txt |  [`https://graph.microsoft.com/v1.0/me/drive/root/children/foo.txt/lastModifiedByUser`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fdrive%2Froot%2Fchildren%2Ffoo.txt%2FlastModifiedByUser&version=v1.0) |
|   OBTENER grupos de Office 365 de los que soy miembro| [`https://graph.microsoft.com/v1.0/me/memberOf/$/microsoft.graph.group?$filter=groupTypes/any(a:a%20eq%20'unified')`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2FmemberOf%2F%24%2Fmicrosoft.graph.group%3F%24filter%3DgroupTypes%2Fany(a%3Aa%2520eq%2520'unified')&version=v1.0) |
|   OBTENER usuarios de mi organización     | [`https://graph.microsoft.com/v1.0/users`](https://developer.microsoft.com/graph/graph-explorer/?request=users&version=v1.0) |
|   OBTENER grupos de mi organización | [`https://graph.microsoft.com/v1.0/groups`](https://developer.microsoft.com/graph/graph-explorer/?request=groups&version=v1.0) |
|   OBTENER usuarios relacionados conmigo    | [`https://graph.microsoft.com/v1.0/me/people`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fpeople&version=beta)  |
|   OBTENER elementos de tendencias a mi alrededor |  [`https://graph.microsoft.com/beta/me/insights/trending`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Finsights%2Ftrending&version=beta) |
|   GET mis notas |  [`https://graph.microsoft.com/v1.0/me/onenote/notebooks`](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fonenote%2Fnotebooks&version=beta) |

## <a name="access-microsoft-graph-at-scale"></a>Obtener acceso a Microsoft Graph a escala


La conexión de datos de Microsoft Graph permite el acceso masivo, en lugar de un acceso tradicional y transaccional, a los datos de Office 365. Con el conjunto masivo de datos de Office 365, puede usar herramientas de Azure para crear aplicaciones inteligentes que:

- Buscan el experto más cercano sobre un tema de la organización 
- Automatizan la creación del knowledge base
- Analizan las convocatorias de reunión para proporcionar información sobre el uso de la sala de conferencias
- Detectan el fraude con datos de comunicación y productividad

## <a name="when-should-i-use-microsoft-graph-data-connect"></a>Introducción a la conexión de datos de Microsoft Graph

La conexión de datos de Microsoft Graph proporciona una nueva forma de interactuar con los datos y está disponible mediante las API de Microsoft Graph. Además de proporcionar un acceso escalable a los datos de Office 365, la conexión de datos de Microsoft Graph también proporciona un único conjunto de capacidades que simplifican la creación de aplicaciones inteligentes, todo ello desde la nube de Microsoft.

|**Característica**| **API de Microsoft Graph** | **Conexión de datos de Microsoft Graph** |
|:----------|:------------------------|:--------------------------------------|
| **Ámbito de acceso** | Usuario único o espacio empresarial | Muchos usuarios o grupos |
| **Patrón de acceso** | Tiempo real | Programación recurrente |
| **Operaciones de datos** | Funciona en el patrón de datos | Funciona en una caché de los datos |
| **Protección de datos** | Los datos están protegidos en Microsoft 365 | La protección de datos se extiende a la caché de datos de su suscripción de Azure |
| **Consentimiento del usuario** | Sí mismo<br>Tipos de recursos | Ninguno |
| **Consentimiento del administrador** | Toda la organización<br>Tipos de recursos | Seleccione los usuarios de los grupos<br>Propiedades y tipos de recursos<br>Excluye los usuarios |
| **Herramientas de acceso** | Consultas web RESTful | Azure Data Factory |

Para más información sobre la conexión de datos de Microsoft Graph, consulte [Conexión de datos de Microsoft Graph](data-connect-overview.md). Para empezar, consulte [Introducción a la conexión de datos de Microsoft Graph](data-connect-concept-overview.md) 

## <a name="next-steps"></a>Pasos siguientes

- Consulte algunos [escenarios destacados](https://developer.microsoft.com/graph/examples).
- Pruebe una solicitud de ejemplo en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).
- Use el [inicio rápido](https://developer.microsoft.com/graph/quick-start) para configurar una aplicación de ejemplo lista para ejecutar.
- En la tabla de contenido, busque en **Aprender** para obtener información sobre los servicios y las características que puede usar en los escenarios. 
- Descubra cómo [obtener un token de autenticación](auth-overview.md) en su aplicación.
- Empiece a [usar la API](use-the-api.md).

## <a name="feedback"></a>¿Quiere realizar algún comentario?

Su opinión es importante para nosotros. Póngase en contacto con nosotros en [Stack Overflow](https://stackoverflow.com/questions/tagged/office365+or+microsoftgraph). Etiquete sus preguntas con {MicrosoftGraph}.

