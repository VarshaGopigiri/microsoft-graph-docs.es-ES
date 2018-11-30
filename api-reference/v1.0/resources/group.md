---
title: Tipo de recurso group
description: Representa un grupo de Azure Active Directory (AD Azure), que puede ser un grupo de Office 365, un grupo dinámico o un grupo de seguridad.
ms.openlocfilehash: e9e6d652bba485a28a36a5efa8d670d9f4a6053f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030216"
---
# <a name="group-resource-type"></a>Tipo de recurso group

Representa un grupo de Azure Active Directory (Azure AD) que puede ser un grupo de Office 365, un grupo dinámico o un grupo de seguridad. Se hereda de [DirectoryObject](directoryobject.md).

Este recurso admite:

- Adición de sus propios datos a las propiedades personalizadas como [extensiones](/graph/extensibility-overview).
- Suscribirse a [las notificaciones de cambios](/graph/webhooks).
- que use una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/user-delta.md).


## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|**Administración de grupos**| | |
|[Crear grupo](../api/group-post-groups.md) | [grupo](group.md) |Crea un grupo. Puede ser un grupo, un grupo dinámico o un grupo de seguridad de Office 365.|
|[Obtener grupo](../api/group-get.md) | [grupo](group.md) |Lee las propiedades de un objeto de grupo.|
|[Enumerar grupos](../api/group-list.md) |Colección [group](group.md) |Enumera los objetos de grupo y sus propiedades.|
|[Grupo de actualización](../api/group-update.md) | Ninguno |Actualiza las propiedades de un objeto de grupo. |
|[Eliminar grupo](../api/group-delete.md) | Ninguno |Elimina el objeto de grupo. |
|[delta](../api/group-delta.md)|Colección group| Obtiene los cambios incrementales de grupos. |
|[Mostrar groupLifecyclePolicies](../api/group-list-grouplifecyclepolicies.md) |Colección de [groupLifecyclePolicy](grouplifecyclepolicy.md)| Muestra las directivas de ciclo de vida del grupo. |
|[Renovar](../api/group-renew.md)|Booleano|Renueva la expiración de un grupo. Cuando se renueva un grupo, la expiración del grupo se amplía por el número de días definidos en la directiva.|
|[Agregar propietario](../api/group-post-owners.md) |Ninguno| Agrega un nuevo propietario al grupo al publicarlo en la propiedad de navegación **owners** (se admite solo para grupos de seguridad y grupos de seguridad habilitados para correo).|
|[Enumerar propietarios](../api/group-list-owners.md) |Colección [directoryObject](directoryobject.md)| Obtiene los propietarios del grupo desde la propiedad de navegación **owners**.|
|[Eliminar propietario](../api/group-delete-owners.md) | Ninguno |Elimina a un propietario de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **owners**.|
|[Agregar miembro](../api/group-post-members.md) |Ninguno| Agrega un usuario o grupo a este grupo publicándolo en la propiedad de navegación **members** (compatible solo con grupos de seguridad y grupos de seguridad habilitados para correo).|
|[Enumerar miembros](../api/group-list-members.md) |Colección [directoryObject](directoryobject.md)| Obtiene los usuarios y grupos que son miembros directos de este grupo desde la propiedad de navegación **members**.|
|[Eliminar miembro](../api/group-delete-members.md) | Ninguno |Elimina a un miembro de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **members**. Puede eliminar usuarios u otros grupos. |
|[checkMemberGroups](../api/group-checkmembergroups.md)|Colección string|Comprueba la pertenencia de este grupo a una lista de grupos. La función es transitiva.|
|[getMemberGroups](../api/group-getmembergroups.md)|Colección string|Devuelve todos los grupos de los que el grupo es miembro. La función es transitiva.|
|[getMemberObjects](../api/group-getmemberobjects.md)|Colección string|Devuelve todos los grupos de los que el grupo es miembro. La función es transitiva. |
|[Create setting](../api/groupsetting-post-groupsettings.md) | [groupSetting](groupsetting.md) |Crea un objeto de configuración según una plantilla de groupSettingTemplate. La solicitud POST debe proporcionar settingValues para toda la configuración establecida en la plantilla. Solo se pueden usar plantillas específicas de grupos para esta operación.|
|[Get setting](../api/groupsetting-get.md) | [groupSetting](groupsetting.md) | Lee las propiedades de un objeto de configuración específico. |
|[List settings](../api/groupsetting-list.md) | Colección de [groupSetting](groupsetting.md) | Enumera las propiedades de todos los objetos de configuración. |
|[Update setting](../api/groupsetting-update.md) | [groupSetting](groupsetting.md) | Actualiza el objeto de configuración. |
|[Delete setting](../api/groupsetting-delete.md) | Ninguno | Elimina un objeto de configuración. |
|**Calendario**| | |
|[Crear evento](../api/group-post-events.md) |[evento](event.md)| Crea un evento al publicarlo en la colección de eventos.|
|[Obtener evento](../api/group-get-event.md) |[evento](event.md)|Lee las propiedades de un objeto de evento.|
|[Lista de eventos](../api/group-list-events.md) |Colección [event](event.md)| Obtiene una colección de objetos de evento.|
|[Actualizar evento](../api/group-update-event.md) |Ninguno|Actualiza las propiedades del objeto de evento.|
|[Eliminar evento](../api/group-delete-event.md) |Ninguno|Elimina el objeto de evento.|
|[Lista de calendarView](../api/group-list-calendarview.md) |Colección de [eventos](event.md)| Obtiene una colección de eventos en un intervalo de tiempo especificado.|
|**Conversaciones**| | |
|[Crear conversación](../api/group-post-conversations.md) |[conversación](conversation.md)| Crea una conversación al publicarla en la colección de conversaciones.|
|[Obtener conversación](../api/group-get-conversation.md) |[conversación](conversation.md)| Lee las propiedades de un objeto de conversación.|
|[Lista de conversaciones](../api/group-list-conversations.md) |Colección de [conversaciones](conversation.md)| Obtiene una colección de objetos de conversación.|
|[Eliminar conversación](../api/group-delete-conversation.md) |Ninguno|Elimina un objeto de conversación.|
|[Obtener conversación](../api/group-get-thread.md) |[conversationThread](conversationthread.md)| Lee las propiedades de un objeto de conversación.|
|[Lista de conversaciones](../api/group-list-threads.md) |Colección [conversationThread](conversationthread.md)| Obtiene todas las conversaciones de un grupo.|
|[Actualizar conversación](../api/group-update-thread.md) |Ninguno| Actualiza las propiedades de un objeto de conversación.|
|[Eliminar conversación](../api/group-delete-thread.md) |Ninguno| Elimina un objeto de conversación.|
|[Lista de acceptedSenders](../api/group-list-acceptedsenders.md) |Colección [directoryObject](directoryobject.md)| Obtiene una lista de usuarios o grupos que se encuentran en la lista de acceptedSenders de este grupo.|
|[Agregar acceptedSenders](../api/group-post-acceptedsenders.md) |[directoryObject](directoryobject.md)| Agrega un usuario o grupo a la colección acceptSenders.|
|[Eliminar acceptedSender](../api/group-delete-acceptedsenders.md) |[directoryObject](directoryobject.md)| Elimina a un usuario o grupo de la colección acceptedSenders.|
|[Enumerar rejectedSenders](../api/group-list-rejectedsenders.md) |Colección [directoryObject](directoryobject.md)| Obtiene una lista de usuarios o grupos que se encuentran en la lista de rejectedSenders de este grupo.|
|[Agregar rejectedSender](../api/group-post-rejectedsenders.md) |[directoryObject](directoryobject.md)| Agrega un nuevo usuario o grupo a la colección rejectedSenders.|
|[Eliminar rejectedSender](../api/group-delete-rejectedsenders.md) |[directoryObject](directoryobject.md)| Elimina un nuevo usuario o grupo de la colección rejectedSenders.|
|[Create setting](../api/groupsetting-post-groupsettings.md) | [groupSetting](groupsetting.md) |Crea un objeto de configuración según una plantilla de groupSettingTemplate. La solicitud POST debe proporcionar settingValues para toda la configuración establecida en la plantilla. Solo se pueden usar plantillas específicas de grupos para esta operación.|
|[Get setting](../api/groupsetting-get.md) | [groupSetting](groupsetting.md) | Lee las propiedades de un objeto de configuración específico. |
|[List settings](../api/groupsetting-list.md) | Colección de [groupSetting](groupsetting.md) | Enumera las propiedades de todos los objetos de configuración. |
|[Configuración de actualización](../api/groupsetting-update.md) | Ninguno | Actualiza el objeto de configuración. |
|[Delete setting](../api/groupsetting-delete.md) | Ninguno | Elimina un objeto de configuración. |
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
|[removeFavorite](../api/group-removefavorite.md)|Ninguno|Quita el grupo de la lista de grupos favoritos del usuario actual. Compatible solo con grupos de Office 365.|
|[Enumerar memberOf](../api/group-list-memberof.md) |Colección [directoryObject](directoryobject.md)| Obtiene los grupos y las unidades administrativas de los que el usuario es miembro directo desde la propiedad de navegación **memberOf**.|
|[subscribeByMail](../api/group-subscribebymail.md)|Ninguno|Establece la propiedad isSubscribedByMail como **true**. Permite que el usuario actual pueda recibir conversaciones de correo electrónico. Compatible solo con grupos de Office 365.|
|[unsubscribeByMail](../api/group-unsubscribebymail.md)|Ninguno|Establece la propiedad isSubscribedByMail como **false**. Impide que el usuario actual pueda recibir conversaciones de correo electrónico. Compatible solo con grupos de Office 365.|
|[resetUnseenCount](../api/group-resetunseencount.md)|Ninguno|Restablece a 0 la unseenCount de todas las publicaciones que el usuario actual no ha visto desde su última visita. Compatible solo con grupos de Office 365.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|allowExternalSenders|Booleano|El valor predeterminado es **false**. Indica si los usuarios externos a la organización pueden enviar mensajes al grupo.|
|autoSubscribeNewMembers|Booleano|El valor predeterminado es **false**. Indica si los miembros agregados al grupo se suscribirán de forma automática para recibir notificaciones por correo electrónico. Puede establecer esta propiedad en una solicitud PATCH del grupo; no la establezca en la solicitud POST inicial que crea el grupo.|
|classification|String|Describe una clasificación para el grupo (como impacto en el negocio bajo, medio o alto). Los valores válidos para esta propiedad se definen mediante la creación de un valor [setting](groupsetting.md) ClassificationList, basado en la [definición de plantilla](groupsettingtemplate.md).|
|createdDateTime|DateTimeOffset| Marca de tiempo de cuando se creó el grupo. El valor no puede modificarse y se rellena automáticamente al crear el grupo. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura. |
|description|String|Una descripción opcional del grupo. |
|displayName|String|El nombre para mostrar del grupo. Esta propiedad es necesaria cuando se crea un grupo y no se puede borrar durante las actualizaciones. Es compatible con $filter y $orderby.|
|groupTypes|Colección String| Especifica el tipo de grupo para crear. Los valores posibles son `Unified` para crear un grupo de Office 365, o `DynamicMembership` para grupos dinámicos.  Para otro grupo de todos los tipos, como los grupos de seguridad y grupos de seguridad habilitados para correo electrónico, no establezca esta propiedad. Es compatible con $filter.|
|id|String|El identificador único del grupo. Heredado de [directoryObject](directoryobject.md). Clave. No admite valores NULL. Solo lectura.|
|isSubscribedByMail|Booleano|El valor predeterminado es **true**. Indica si el usuario actual está suscrito para recibir conversaciones de correo electrónico.|
|mail|String|La dirección SMTP del grupo, por ejemplo: "serviceadmins@contoso.onmicrosoft.com". Solo lectura. Es compatible con $filter.|
|mailEnabled|Boolean|Especifica si el grupo está habilitado para correo. Si la propiedad **securityEnabled** también es **true**, el grupo es un grupo de seguridad habilitado para correo electrónico; en caso contrario, el grupo es un grupo de distribución de Microsoft Exchange.|
|mailNickname|String|Alias de correo del grupo, único en la organización. Esta propiedad debe especificarse al crear un grupo. Admite $filter.|
|onPremisesLastSyncDateTime|DateTimeOffset|Indica la última vez que el grupo se ha sincronizado con el directorio local. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura. Es compatible con $filter.|
|onPremisesProvisioningErrors|colección de [onPremisesProvisioningError](onpremisesprovisioningerror.md)| Errores al usar el producto de sincronización de Microsoft durante el aprovisionamiento. |
|onPremisesSecurityIdentifier|String|Contiene el identificador de seguridad local (SID) del grupo que se sincroniza desde un recurso local a la nube. Solo lectura. |
|onPremisesSyncEnabled|Boolean|**true** si este grupo está sincronizado desde un directorio local; **false** si este grupo se ha sincronizado originalmente desde un directorio local, pero ya no está sincronizado; **null** si este grupo no se ha sincronizado nunca desde un directorio local (valor predeterminado). Solo lectura. Es compatible con $filter.|
|preferredDataLocation|String|La ubicación de datos preferido para el grupo. Para obtener más información, vea [OneDrive en línea Multi-ubican](https://docs.microsoft.com/sharepoint/dev/solution-guidance/multigeo-introduction).|
|proxyAddresses|Colección string| El operador **any** es necesario para las expresiones de filtro en las propiedades de varios valores. Solo lectura. No admite valores NULL. Es compatible con $filter. |
|renewedDateTime|DateTimeOffset| Marca de tiempo de la última vez que se renovó el grupo. Esto no se puede modificar directamente y solo se actualiza a través de la [acción de servicio de renovación](../api/group-renew.md). El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.|
|securityEnabled|Boolean|Especifica si el grupo es un grupo de seguridad. Si la propiedad **mailEnabled** también es true, el grupo es un grupo de seguridad habilitado para correo electrónico; de lo contrario, es un grupo de seguridad. Debe ser **false** para grupos de Office 365. Es compatible con $filter.|
|unseenCount|Int32|Recuento de las conversaciones que se han entregado una o varias entradas de nuevo desde la última visita al grupo del usuario que ha iniciado sesión.|
|visibility|String| Especifica la visibilidad de un grupo de Office 365. Los valores posibles son: `private`, `public`, o `hiddenmembership`; los valores en blanco se tratan como público.  Para obtener más información, vea [Opciones de visibilidad del grupo](#group-visibility-options) .<br>Se puede establecer la visibilidad solo cuando se crea un grupo; no es editable.<br>Visibilidad sólo se admite para grupos unificados; no se admite para grupos de seguridad.|

### <a name="group-visibility-options"></a>Opciones de visibilidad de grupo

Aquí es lo que significa cada valor de la propiedad de **visibilidad** :
 
|Valor|Descripción|
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
|events|Colección [event](event.md)|Los eventos de calendario del grupo.|
|extensions|Colección [Extension](extension.md)|La colección de extensiones abiertas definidas para el grupo. Solo lectura. Admite valores NULL.|
|groupLifecyclePolicies|Colección de [groupLifecyclePolicy](grouplifecyclepolicy.md)|La colección de las directivas de ciclo de vida para este grupo. Solo lectura. Admite valores NULL.|
|memberOf|Colección [directoryObject](directoryobject.md)|Grupos a los que pertenece este grupo. Métodos HTTP: GET (compatible con todos los grupos). Solo lectura. Admite valores NULL.|
|members|Colección [directoryObject](directoryobject.md)| Los usuarios y los grupos que son miembros de este grupo. Métodos HTTP: GET (compatible con todos los grupos), POST (compatible con grupos de Office 365, grupos de seguridad y los grupos de seguridad habilitados para correo), DELETE (compatible con grupos de Office 365 y grupos de seguridad). Admite valores NULL.|
|onenote|[OneNote](onenote.md)| Solo lectura.|
|owners|Colección [directoryObject](directoryobject.md)|Los propietarios del grupo. Los propietarios son un conjunto de usuarios no administradores que tienen permiso para modificar este objeto. Limitado a 10 propietarios. Métodos HTTP: GET (compatible con todos los grupos), POST (compatible con grupos de Office 365, grupos de seguridad y los grupos de seguridad habilitados para correo), DELETE (compatible con grupos de Office 365 y grupos de seguridad). Admite valores NULL.|
|photo|[profilePhoto](profilephoto.md)| La foto de perfil del grupo. |
|photos|Colección [profilePhoto](profilephoto.md)| Las fotos de perfil que pertenecen al grupo. Solo lectura. Admite valores NULL.|
|planner|[plannerGroup](plannergroup.md)| Punto de entrada al recurso de Planner que puede existir para un grupo unificado.|
|rejectedSenders|Colección [directoryObject](directoryobject.md)|La lista de usuarios o grupos que no tienen permiso para crear publicaciones o eventos de calendario en este grupo. Admite valores NULL|
|configuración|Colección de [groupSetting](groupsetting.md)| Solo lectura. Admite valores NULL.|
|sites|Colección [site](site.md)|La lista de sitios de SharePoint de este grupo. Acceda al sitio predeterminado con /sites/root.|
|threads|Colección [conversationThread](conversationthread.md)| Los hilos de conversación del grupo. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Esta es una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.directoryObject",
  "openType": true,
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
    "rejectedSenders",
    "threads"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.group",
  "@odata.annotations": [
    {
      "capabilities": {
        "changeTracking": true
      }
    },
    {
      "property": "acceptedSenders",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "searchable": false,
        "updatable": false
      }
    },
    {
      "property": "calendar",
      "capabilities": {
        "changeTracking": false,
        "deletable": false,
        "expandable": false,
        "insertable": false,
        "searchable": false,
        "updatable": false
      }
    },
    {
      "property": "calendarView",
      "capabilities": {
        "changeTracking": true,
        "deletable": false,
        "expandable": false,
        "insertable": false,
        "searchable": false,
        "updatable": false
      }
    },
    {
      "property": "conversations",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "updatable": false
      }
    },
    {
      "property": "events",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "searchable": false
      }
    },
    {
      "property": "photo",
      "capabilities": {
        "changeTracking": false,
        "deletable": false,
        "expandable": false,
        "insertable": false,
        "searchable": false
      }
    },
    {
      "property": "photos",
      "capabilities": {
        "changeTracking": false,
        "deletable": false,
        "expandable": false,
        "insertable": false,
        "searchable": false,
        "updatable": false
      }
    },
    {
      "property": "rejectedSenders",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "searchable": false,
        "updatable": false
      }
    },
    {
      "property": "threads",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "searchable": false,
        "updatable": false
      }
    }
  ]
}-->

```json
{
  "allowExternalSenders": false,
  "autoSubscribeNewMembers": true,
  "classification": "string",
  "createdDateTime": "String (timestamp)",
  "description": "string",
  "displayName": "string",
  "groupTypes": ["string"],
  "id": "string (identifier)",
  "isSubscribedByMail": true,
  "mail": "string",
  "mailEnabled": true,
  "mailNickname": "string",
  "onPremisesLastSyncDateTime": "String (timestamp)",
  "onPremisesProvisioningErrors": [{"@odata.type": "microsoft.graph.onPremisesProvisioningError"}],
  "onPremisesSecurityIdentifier": "string",
  "onPremisesSyncEnabled": true,
  "preferredDataLocation": "string",
  "proxyAddresses": ["string"],
  "renewedDateTime": "String (timestamp)",
  "securityEnabled": true,
  "unseenCount": 1024,
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
