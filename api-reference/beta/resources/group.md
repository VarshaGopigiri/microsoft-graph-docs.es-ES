---
title: Tipo de recurso group
description: Representa un grupo de Azure Active Directory (AD Azure), que puede ser un grupo de Office 365, un equipo en Microsoft Teams, un grupo dinámico o un grupo de seguridad.
localization_priority: Priority
ms.openlocfilehash: 928eb9887665b117535bcf4fa13cf6a95b8ff283
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866895"
---
# <a name="group-resource-type"></a>Tipo de recurso group

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un grupo de Azure Active Directory (AD Azure), que puede ser un grupo de Office 365, un equipo en Microsoft Teams, un grupo dinámico o un grupo de seguridad.
Se hereda de [directoryObject](directoryobject.md).

Este recurso admite:

- Adición de sus propios datos a las propiedades personalizadas como [extensiones](/graph/extensibility-overview).
- Suscribirse a [las notificaciones de cambios](/graph/webhooks).
- que use una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/user-delta.md).

> **Los equipos de Microsoft y los grupos de Office 365 admiten la colaboración de grupo**. Puede utilizar la mayoría de los grupos de Office 365 API con Microsoft Teams. Para crear un [equipo](team.md), primera [Crear grupo](../api/group-post-groups.md) y, a continuación, [Agregue un equipo a ella](../api/team-put-teams.md). Para obtener información detallada, vea la [información general de los equipos de Microsoft](teams-api-overview.md).

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|**Administración de grupos**| | |
|[Crear grupo](../api/group-post-groups.md) | [grupo](group.md) |Crear un nuevo grupo tal como se especifica. Puede ser un grupo de Office 365, el grupo dinámico, el grupo de seguridad o el equipo.|
|[Obtener grupo](../api/group-get.md) | [grupo](group.md) |Propiedades de lectura y las relaciones de objeto de grupo.|
|[Grupo de actualización](../api/group-update.md) | Ninguno |Actualiza las propiedades de un objeto de grupo. |
|[Eliminar grupo](../api/group-delete.md) | Ninguno |Elimina el objeto de grupo. |
|[delta](../api/group-delta.md)|Colección group| Obtiene los cambios incrementales de grupos. |
|[Mostrar groupLifecyclePolicies](../api/group-list-grouplifecyclepolicies.md) |Colección de [groupLifecyclePolicy](grouplifecyclepolicy.md)| Muestra las directivas de ciclo de vida del grupo. |
|[Enumerar propietarios](../api/group-list-owners.md) |Colección [directoryObject](directoryobject.md)| Obtiene los propietarios del grupo desde la propiedad de navegación **owners**.|
|[Agregar propietario](../api/group-post-owners.md) |[directoryObject](directoryobject.md)| Agrega un nuevo propietario al grupo al publicarlo en la propiedad de navegación **owners** (se admite solo para grupos de seguridad y grupos de seguridad habilitados para correo).|
|[Eliminar propietario](../api/group-delete-owners.md) | Ninguno |Elimina a un propietario de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **owners**.|
|[Enumerar miembros](../api/group-list-members.md) |Colección [directoryObject](directoryobject.md)| Obtiene los usuarios y grupos que son miembros directos de este grupo desde la propiedad de navegación **members**.|
|[Lista de miembros transitiva](../api/group-list-transitivemembers.md) |Colección [directoryObject](directoryobject.md)| Obtenga el a los usuarios, grupos, dispositivos y entidades de seguridad de servicio que son miembros, incluyendo a anidados los miembros de este grupo.|
|[Agregar miembro](../api/group-post-members.md) |[directoryObject](directoryobject.md)| Agrega un usuario o grupo a este grupo publicándolo en la propiedad de navegación **members** (compatible solo con grupos de seguridad y grupos de seguridad habilitados para correo).|
|[Eliminar miembro](../api/group-delete-members.md) | Ninguno |Elimina a un miembro de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **members**. Puede eliminar usuarios u otros grupos. |
|[Enumerar memberOf](../api/group-list-memberof.md) |Colección [directoryObject](directoryobject.md)| Obtener los grupos y unidades administrativas que este grupo es miembro directo de la propiedad de navegación de miembro.|
|[Miembro de lista transitiva](../api/group-list-transitivememberof.md) |Colección [directoryObject](directoryobject.md)| Lista de los grupos y unidades administrativas que este usuario es un miembro de. Esta operación es transitiva e incluye los grupos que este grupo es un miembro anidado de. |
|[checkMemberGroups](../api/group-checkmembergroups.md)|Colección string|Compruebe si la pertenencia a una lista de grupos. La función es transitiva.|
|[getMemberGroups](../api/group-getmembergroups.md)|Colección string|Devuelve todos los grupos de los que el grupo es miembro. La función es transitiva.|
|[getMemberObjects](../api/group-getmemberobjects.md)|Colección string|Devolver todos los grupos y unidades administrativas que el grupo es un miembro de. La función es transitiva. |
|[Create setting](../api/directorysetting-post-settings.md) | [Establecer](directorysetting.md) |Crear un objeto de configuración basado en un directorySettingTemplate. La solicitud POST debe proporcionar settingValues para toda la configuración definida en la plantilla. Sólo las plantillas específicas de grupos se pueden usar para esta operación.|
|[Get setting](../api/directorysetting-get.md) | [Establecer](directorysetting.md) |Lee las propiedades de un objeto de configuración específico.|
|[List settings](../api/directorysetting-list.md) | colección de [establecer](directorysetting.md) |Enumera las propiedades de todos los objetos de configuración.|
|[Configuración de actualización](../api/directorysetting-update.md) | [Establecer](directorysetting.md)  |Actualiza el objeto de configuración. |
|[Delete setting](../api/directorysetting-delete.md) | Ninguno |Elimina un objeto de configuración. |
|[Extremos de lista](../api/group-list-endpoints.md) |colección de [extremo](endpoint.md)| Obtener una colección de objetos de extremo. |
|[Obtener el extremo](../api/endpoint-get.md) | [extremo](endpoint.md) | Leer las propiedades y relaciones de un objeto de extremo. |
|[delta](../api/group-delta.md)|Colección group| Obtiene los cambios incrementales de grupos. |
|[validateProperties](../api/group-validateproperties.md)|JSON| Validar el nombre para mostrar de un grupo de Office 365 o alias de correo cumplen con las políticas de nomenclatura. | 
|**Calendario**| | |
|[Crear evento](../api/group-post-events.md) |[evento](event.md)| Crea un evento al publicarlo en la colección de eventos.|
|[Obtener evento](../api/group-get-event.md) |[evento](event.md)|Lee las propiedades de un objeto de evento.|
|[Lista de eventos](../api/group-list-events.md) |Colección [event](event.md)| Obtiene una colección de objetos de evento.|
|[Actualizar evento](../api/group-update-event.md) |Ninguno|Actualiza las propiedades del objeto de evento.|
|[Eliminar evento](../api/group-delete-event.md) |Ninguno|Elimina el objeto de evento.|
|[Lista de calendarView](../api/group-list-calendarview.md) |Colección de [eventos](event.md)| Obtiene una colección de eventos en un intervalo de tiempo especificado.|
|**Conversaciones**| | |
|[Crear conversación](../api/group-post-conversations.md) |[conversation](conversation.md)| Crea una conversación al publicarla en la colección de conversaciones.|
|[Obtener conversación](../api/group-get-conversation.md) |[conversación](conversation.md)| Lee las propiedades de un objeto de conversación.|
|[Lista de conversaciones](../api/group-list-conversations.md) |Colección de [conversaciones](conversation.md)| Obtiene una colección de objetos de conversación.|
|[Eliminar conversación](../api/group-delete-conversation.md) |Ninguno|Elimina un objeto de conversación.|
|[Obtener conversación](../api/group-get-thread.md) |[conversationThread](conversationthread.md)| Lee las propiedades de un objeto de conversación.|
|[Lista de conversaciones](../api/group-list-threads.md) |Colección [conversationThread](conversationthread.md)| Obtiene todas las conversaciones de un grupo.|
|[Actualizar conversación](../api/group-update-thread.md) |Ninguno| Actualiza las propiedades de un objeto de conversación.|
|[Eliminar conversación](../api/group-delete-thread.md) |Ninguno| Eliminar el objeto de subproceso
|[Lista de acceptedSenders](../api/group-list-acceptedsenders.md) |Colección [directoryObject](directoryobject.md)| Obtiene una lista de usuarios o grupos que se encuentran en la lista de acceptedSenders de este grupo.|
|[Agregar acceptedSenders](../api/group-post-acceptedsenders.md) |[directoryObject](directoryobject.md)| Agrega un usuario o grupo a la colección acceptSenders.|
|[Eliminar acceptedSender](../api/group-delete-acceptedsenders.md) |[directoryObject](directoryobject.md)| Elimina a un usuario o grupo de la colección acceptedSenders.|
|[Enumerar rejectedSenders](../api/group-list-rejectedsenders.md) |Colección [directoryObject](directoryobject.md)| Obtiene una lista de usuarios o grupos que se encuentran en la lista de rejectedSenders de este grupo.|
|[Agregar rejectedSender](../api/group-post-rejectedsenders.md) |[directoryObject](directoryobject.md)| Agrega un nuevo usuario o grupo a la colección rejectedSenders.|
|[Eliminar rejectedSender](../api/group-delete-rejectedsenders.md) |[directoryObject](directoryobject.md)| Elimina un nuevo usuario o grupo de la colección rejectedSenders.|
|**Extensiones abiertas**| | |
|[Crear extensión abierta](../api/opentypeextension-post-opentypeextension.md) |[openTypeExtension](opentypeextension.md)| Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o un recurso existente.|
|[Obtener extensión abierta](../api/opentypeextension-get.md) |Colección [openTypeExtension](opentypeextension.md)| Obtiene una extensión abierta identificada por el nombre de extensión.|
|**Extensiones de esquema**| | |
|[Agregar valores de extensión de esquema](/graph/extensibility-schema-groups) || Crea una definición de extensión de esquema y, después, la usa para agregar datos escritos personalizados a un recurso.|
|**Otros recursos de grupo**| | |
|[Enumerar fotos](../api/group-list-photos.md) |Colección [profilePhoto](photo.md)| Obtiene una colección de fotos de perfil para el grupo.|
|[Enumerar plannerPlans](../api/plannergroup-list-plans.md) |Colección [plannerPlan](plannerplan.md)| Obtiene planes de Planner que pertenecen al grupo.|
|**Configuración de usuario**| | |
|[addFavorite](../api/group-addfavorite.md)|Ninguno|Agrega el grupo a la lista de grupos favoritos del usuario actual. Compatible solo con grupos de Office 365.|
|[removeFavorite](../api/group-removefavorite.md)|Ninguno|Quita el grupo de la lista de grupos favoritos del usuario actual. Solo es compatible con Grupos de Office 365.|
|[Enumerar memberOf](../api/group-list-memberof.md) |Colección [directoryObject](directoryobject.md)| Obtiene los grupos y las unidades administrativas de los que el usuario es miembro directo desde la propiedad de navegación **memberOf**.|
|[Enumerar joinedTeams](../api/user-list-joinedteams.md) |Colección [group](group.md)| Obtenga el Teams Microsoft que el usuario es miembro directo.|
|[subscribeByMail](../api/group-subscribebymail.md)|Ninguno|Establezca la propiedad isSubscribedByMail en **true**. Permitiendo al usuario actual recibir las conversaciones de correo electrónico. Compatible con sólo los grupos de Office 365.|
|[unsubscribeByMail](../api/group-unsubscribebymail.md)|Ninguno|Establezca la propiedad isSubscribedByMail en **false**. Deshabilitar al usuario actual de las conversaciones de correo electrónico de recepción. Compatible con sólo los grupos de Office 365.|
|[resetUnseenCount](../api/group-resetunseencount.md)|Ninguno|Restablecer la unseenCount en 0 de todas las entradas del blog que el usuario actual no ha visto desde la última visita. Compatible con sólo los grupos de Office 365.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|allowExternalSenders|Booleano|El valor predeterminado es **false**. Indica si los usuarios externos a la organización pueden enviar mensajes al grupo.|
|assignedLicenses|Colección [assignedLicense](assignedlicense.md)|Las licencias que están asignadas al grupo. Solo lectura.|
|autoSubscribeNewMembers|Booleano|El valor predeterminado es **false**. Indica si los miembros agregados al grupo se suscribirán de forma automática para recibir notificaciones por correo electrónico. Puede establecer esta propiedad en una solicitud PATCH del grupo; no la establezca en la solicitud POST inicial que crea el grupo.|
|classification|String|Describe una clasificación para el grupo (como impacto en el negocio bajo, medio o alto). Los valores válidos para esta propiedad se definen mediante la creación de un valor [setting](directorysetting.md) ClassificationList, basado en la [definición de plantilla](directorysettingtemplate.md).|
|createdDateTime|DateTimeOffset| Marca de tiempo de cuando se creó el grupo. El valor no puede modificarse y se rellena automáticamente al crear el grupo. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura. |
|description|Cadena|Una descripción opcional del grupo.|
|displayName|Cadena|El nombre para mostrar del grupo. Esta propiedad es necesaria cuando se crea un grupo y no se puede borrar durante las actualizaciones. Es compatible con $filter y $orderby.|
|groupTypes|Colección String| Especifica el tipo de grupo para crear. Los valores posibles son `Unified` para crear un grupo de Office 365, o `DynamicMembership` para grupos dinámicos.  Para otro grupo de todos los tipos, como los grupos de seguridad y grupos de seguridad habilitados para correo electrónico, no establezca esta propiedad.|
|id|String|El identificador único del grupo. Heredado de [directoryObject](directoryobject.md). Clave. No admite valores NULL. Solo lectura.|
|isSubscribedByMail|Booleano|El valor predeterminado es **true**. Indica si el usuario actual está suscrito para recibir conversaciones de correo electrónico.|
|licenseProcessingState|Cadena|Indica el estado de la asignación de licencias de grupo a todos los miembros del grupo. Solo lectura. Valores posibles: `QueuedForProcessing`, `ProcessingInProgress`, y `ProcessingComplete`.|
|mail|Cadena|La dirección SMTP del grupo, por ejemplo: "serviceadmins@contoso.onmicrosoft.com". Solo lectura. Es compatible con $filter.|
|mailEnabled|Boolean|Especifica si el grupo está habilitado para correo. Si la propiedad **securityEnabled** también es **true**, el grupo es un grupo de seguridad habilitado para correo electrónico; en caso contrario, el grupo es un grupo de distribución de Microsoft Exchange.|
|mailNickname|String|Alias de correo del grupo, único en la organización. Esta propiedad debe especificarse al crear un grupo. Admite $filter.|
|membershipRule|Cadena|La regla que determina los miembros de este grupo si el grupo es un grupo dinámico (contiene groupTypes `DynamicMembership`). Para obtener más información acerca de la sintaxis de la regla de pertenencia, vea [sintaxis de reglas de pertenencia](https://azure.microsoft.com/en-us/documentation/articles/active-directory-accessmanagement-groups-with-advanced-rules/)|
|membershipRuleProcessingState|Cadena|Indica si el procesamiento de pertenencia dinámica está en o en pausa. Los valores posibles son "Activado" o "En pausa"|
|onPremisesLastSyncDateTime|DateTimeOffset|Indica la última vez en que el objeto se ha sincronizado con el directorio local. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura. Es compatible con $filter.|
|onPremisesProvisioningErrors|colección de [onPremisesProvisioningError](onpremisesprovisioningerror.md)| Errores al usar el producto de sincronización de Microsoft durante el aprovisionamiento. |
|onPremisesSecurityIdentifier|Cadena|Contiene el identificador de seguridad local (SID) del grupo que se sincroniza desde un recurso local a la nube. Solo lectura. |
|onPremisesSyncEnabled|Booleano|**true** si este objeto está sincronizado desde un directorio local; **false** si este objeto se ha sincronizado originalmente desde un directorio local, pero ya no está sincronizado; **null** si este objeto no se ha sincronizado nunca desde un directorio local (valor predeterminado). Solo lectura. Es compatible con $filter.|
|preferredDataLocation|Cadena|La ubicación de datos preferido para el grupo. Para obtener más información, vea [OneDrive en línea Multi-ubican](https://docs.microsoft.com/sharepoint/dev/solution-guidance/multigeo-introduction).|
|preferredLanguage|Cadena|El idioma preferido para un grupo de Office 365. Debe seguir el código ISO 639-1; Por ejemplo, "en-US".|
|proxyAddresses|Colección string| Por ejemplo: `["SMTP: bob@contoso.com", "smtp: bob@sales.contoso.com"]` el operador **any** es necesario para las expresiones de filtro en las propiedades multivalor. Solo lectura. No admite valores NULL. Es compatible con $filter. |
|renewedDateTime|DateTimeOffset| Marca de tiempo de la última vez que se renovó el grupo. Esto no se puede modificar directamente y solo se actualiza a través de la [acción de servicio de renovación](../api/grouplifecyclepolicy-renewgroup.md). El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.|
|securityEnabled|Boolean|Especifica si el grupo es un grupo de seguridad. Si la propiedad **mailEnabled** también es true, el grupo es un grupo de seguridad habilitado para correo electrónico; de lo contrario, es un grupo de seguridad. Debe ser **false** para grupos de Office 365. Es compatible con $filter.|
|tema|Cadena|Especifica el tema de color de un grupo de Office 365. Los valores posibles son `Teal`, `Purple`, `Green`, `Blue`, `Pink`, `Orange` o `Red`.|
|unseenConversationsCount|Int32|Recuento de las conversaciones que se han entregado una o varias entradas de nuevo desde la última visita al grupo del usuario que ha iniciado sesión. Esta propiedad es el mismo que **unseenCount**.|
|unseenCount|Int32|Recuento de las conversaciones que se han entregado una o varias entradas de nuevo desde la última visita al grupo del usuario que ha iniciado sesión. Esta propiedad es el mismo que **unseenConversationsCount**.|
|unseenMessagesCount|Int32|Recuento de publicaciones nuevas que se han entregado a las conversaciones del grupo desde la última visita al grupo del usuario que ha iniciado sesión.|
|visibility|Cadena| Especifica la visibilidad de un grupo de Office 365. Los valores posibles son: `private`, `public`, o `hiddenmembership`; los valores en blanco se tratan como público.  Para obtener más información, vea [Opciones de visibilidad del grupo](#group-visibility-options) .<br>Se puede establecer la visibilidad solo cuando se crea un grupo; no es editable.<br>Visibilidad sólo se admite para grupos unificados; no se admite para grupos de seguridad.|

### <a name="group-visibility-options"></a>Opciones de visibilidad de grupo

Aquí es lo que significa cada valor de la propiedad de **visibilidad** :
 
|Valor|Description|
|:----|-----------|
| `public` | Cualquier usuario puede unirse al grupo sin necesidad de permiso de propietario.<br>Cualquier usuario puede ver el contenido del grupo.|
| `private` | Se necesita el permiso de propietario para unirse al grupo.<br>Que no sean miembros no pueden ver el contenido del grupo.|
| `hiddenmembership` | Se necesita el permiso de propietario para unirse al grupo.<br>Que no sean miembros no pueden ver el contenido del grupo.<br>Que no sean miembros no pueden ver a los miembros del grupo.<br>Los administradores (global, compañía, usuario y departamento de soporte técnico) pueden ver la pertenencia del grupo.<br>El grupo aparece en la libreta de direcciones global (GAL).|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|acceptedSenders|Colección [directoryObject](directoryobject.md)|La lista de usuarios o grupos que tienen permiso para crear publicaciones o eventos de calendario en este grupo. Si esta lista no está vacía, solo pueden publicar los usuarios o grupos enumerados en ella.|
|calendario|[calendario](calendar.md)|El calendario del grupo. Solo lectura.|
|calendarView|Colección [event](event.md)|La vista Calendario del calendario. Solo lectura.|
|conversations|Colección [conversation](conversation.md)|Las conversaciones del grupo.|
|createdOnBehalfOf|[directoryObject](directoryobject.md)| El usuario (o la aplicación) que creó el grupo. NOTA: No se establece si el usuario es un administrador. Solo lectura.|
|Unidad|[drive](drive.md)|Unidad de predeterminado del grupo. Solo lectura.|
|drives|Colección [drive](drive.md)|Unidades del grupo. Solo lectura.|
|extremos|Colección de [extremo](endpoint.md)| Extremos para el grupo. Solo lectura. Admite valores NULL.|
|events|Colección [event](event.md)|Eventos del grupo.|
|extensions|Colección [Extension](extension.md)|La colección de extensiones abiertas definidas para el grupo. Solo lectura. Admite valores NULL.|
|groupLifecyclePolicies|Colección de [groupLifecyclePolicy](grouplifecyclepolicy.md)|La colección de las directivas de ciclo de vida para este grupo. Solo lectura. Admite valores NULL.|
|memberOf|Colección [directoryObject](directoryobject.md)|Grupos y unidades administrativas que este grupo es un miembro de. Métodos HTTP: Obtener (versión admitida para todos los grupos). Solo lectura. Admite valores NULL.|
|members|Colección [directoryObject](directoryobject.md)| Los usuarios, contactos y grupos que son miembros de este grupo. Métodos HTTP: Obtener (versión admitida para todos los grupos), registrar (compatible con grupos de seguridad y grupos de seguridad habilitados para correo), eliminar (sólo admitida grupos de seguridad) de sólo lectura. Admite valores NULL.|
|membersWithLicenseErrors|Colección de [usuario](user.md)|Una lista de miembros del grupo con errores de la licencia de esta asignación de licencias basadas en grupos. Solo lectura.|
|onenote|[OneNote](onenote.md)| Solo lectura.|
|owners|Colección [directoryObject](directoryobject.md)|Los propietarios del grupo. Los propietarios son un conjunto de usuarios sin permisos de administrador que tienen permiso para modificar este objeto. Métodos HTTP: Obtener (versión admitida para todos los grupos), registrar (compatible con grupos de seguridad y grupos de seguridad habilitados para correo), eliminar (sólo admitida grupos de seguridad) de sólo lectura. Admite valores NULL.|
|photo|[profilePhoto](profilephoto.md)| Fotografías del perfil del grupo. |
|photos|Colección [profilePhoto](profilephoto.md)| Las fotos de perfil que pertenecen al grupo. Solo lectura. Admite valores NULL.|
|planner|[plannerGroup](plannergroup.md)| Servicios de organizador selectivos disponibles para el grupo. Solo lectura. Admite valores NULL. |
|rejectedSenders|Colección [directoryObject](directoryobject.md)|La lista de usuarios o grupos que no tienen permiso para crear publicaciones o eventos de calendario en este grupo. Admite valores NULL|
|configuración|colección de [establecer](directorysetting.md)| Configuración que puede controlar el comportamiento de este grupo, al igual que si los miembros pueden invitar a los usuarios invitados al grupo. Admite valores NULL.|
|sites|Colección [site](site.md)|La lista de sitios de SharePoint de este grupo. Acceda al sitio predeterminado con /sites/root.|
|threads|Colección [conversationThread](conversationthread.md)| Los hilos de conversación del grupo. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON
La siguiente es una representación de JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "acceptedSenders",
    "appRoleAssignments",
    "calendar",
    "calendarView",
    "conversations",
    "createdOnBehalfOf",
    "drive",
    "events",
    "extensions",
    "memberOf",
    "members",
    "onenote",
    "owners",
    "photo",
    "photos",    
    "rejectedSenders",
    "threads"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.group"
}-->

```json
{
  "accessType": "string",
  "assignedLicenses": [{"@odata.type": "microsoft.graph.assignedLicense"}],
  "allowExternalSenders": false,
  "autoSubscribeNewMembers": true,
  "createdDateTime": "String (timestamp)",
  "deletedDateTime": "String (timestamp)",
  "description": "string",
  "displayName": "string",
  "groupTypes": ["string"],
  "id": "string (identifier)",
  "isFavorite": true,  
  "isSubscribedByMail": true,
  "licenseProcessingState": "string",
  "mail": "string",
  "mailEnabled": true,
  "mailNickname": "string",
  "onPremisesLastSyncDateTime": "String (timestamp)",
  "onPremisesProvisioningErrors": [{"@odata.type": "microsoft.graph.onPremisesProvisioningError"}],
  "onPremisesSecurityIdentifier": "string",
  "onPremisesSyncEnabled": true,
  "preferredDataLocation": ["string"],
  "proxyAddresses": ["string"],
  "renewedDateTime": "String (timestamp)",
  "securityEnabled": true,
  "unseenConversationsCount": 1024,
  "unseenCount": 1024,
  "unseenMessagesCount": 1024,
  "visibility": "string",
  "acceptedSenders": [ { "@odata.type": "microsoft.graph.directoryObject"} ],
  "calendar": { "@odata.type": "microsoft.graph.calendar" },
  "calendarView": [{ "@odata.type": "microsoft.graph.event" }],
  "conversations": [ { "@odata.type": "microsoft.graph.conversation" }],
  "createdOnBehalfOf": { "@odata.type": "microsoft.graph.directoryObject" },
  "drive": { "@odata.type": "microsoft.graph.drive" },
  "events": [ { "@odata.type": "microsoft.graph.event" }],
  "memberOf": [ { "@odata.type": "microsoft.graph.directoryObject" } ],
  "members": [ { "@odata.type": "microsoft.graph.directoryObject" } ],
  "membersWithLicenseErrors": [{"@odata.type": "microsoft.graph.user"}],
  "owners": [ { "@odata.type": "microsoft.graph.directoryObject" } ],
  "photo": { "@odata.type": "microsoft.graph.profilePhoto" },
  "rejectedSenders": [ { "@odata.type": "microsoft.graph.directoryObject" } ],
  "sites": [ { "@odata.type": "microsoft.graph.site" } ],
  "threads": [ { "@odata.type": "microsoft.graph.conversationThread" }]
}

```

## <a name="see-also"></a>Vea también

- [Agregar datos personalizados a los recursos mediante extensiones](/graph/extensibility-overview)
- [Agregar datos personalizados a los usuarios mediante extensiones abiertas](/graph/extensibility-open-users)
- [Agregar datos personalizados a los grupos mediante extensiones de esquema](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
