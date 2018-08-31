# <a name="group-resource-type"></a>Tipo de recurso group

Representa un grupo de Azure Active Directory (Azure AD) que puede ser un grupo de Office 365, un grupo dinámico o un grupo de seguridad. Se hereda de [DirectoryObject](directoryobject.md).

Este recurso admite:

- que agregue sus propios datos a las propiedades personalizadas mediante [extensiones](../../../concepts/extensibility_overview.md);
- que use una [consulta delta](../../../concepts/delta_query_overview.md) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/user_delta.md).


## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|**Administración de grupos**| | |
|[Crear grupo](../api/group_post_groups.md) | [group](group.md) |Crea un grupo. Puede ser un grupo, un grupo dinámico o un grupo de seguridad de Office 365.|
|[Obtener grupo](../api/group_get.md) | [group](group.md) |Lee las propiedades de un objeto de grupo.|
|[Enumerar grupos](../api/group_list.md) |Colección [group](group.md) |Enumera los objetos de grupo y sus propiedades.|
|[Grupo de actualización](../api/group_update.md) | Ninguno |Actualiza las propiedades de un objeto de grupo. |
|[Eliminar grupo](../api/group_delete.md) | Ninguno |Elimina el objeto de grupo. |
|[delta](../api/group_delta.md)|Colección group| Obtiene los cambios incrementales de grupos. |
|[Mostrar groupLifecyclePolicies](../api/group_list_grouplifecyclepolicies.md) |Colección de [groupLifecyclePolicy](grouplifecyclepolicy.md)| Muestra las directivas de ciclo de vida del grupo. |
|[Renovar](../api/group_renew.md)|Booleano|Renueva la expiración de un grupo. Cuando se renueva un grupo, la expiración del grupo se amplía por el número de días definidos en la directiva.|
|[Agregar propietario](../api/group_post_owners.md) |Ninguno| Agrega un nuevo propietario al grupo al publicarlo en la propiedad de navegación **owners** (se admite solo para grupos de seguridad y grupos de seguridad habilitados para correo).|
|[Enumerar propietarios](../api/group_list_owners.md) |Colección [directoryObject](directoryobject.md)| Obtiene los propietarios del grupo desde la propiedad de navegación **owners**.|
|[Eliminar propietario](../api/group_delete_owners.md) | Ninguno |Elimina a un propietario de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **owners**.|
|[Agregar miembro](../api/group_post_members.md) |Ninguno| Agrega un usuario o grupo a este grupo publicándolo en la propiedad de navegación **members** (compatible solo con grupos de seguridad y grupos de seguridad habilitados para correo).|
|[Enumerar miembros](../api/group_list_members.md) |Colección [directoryObject](directoryobject.md)| Obtiene los usuarios y grupos que son miembros directos de este grupo desde la propiedad de navegación **members**.|
|[Eliminar miembro](../api/group_delete_members.md) | Ninguno |Elimina a un miembro de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **members**. Puede eliminar usuarios u otros grupos. |
|[checkMemberGroups](../api/group_checkmembergroups.md)|Colección string|Comprueba la pertenencia de este grupo a una lista de grupos. La función es transitiva.|
|[getMemberGroups](../api/group_getmembergroups.md)|Colección string|Devuelve todos los grupos de los que el grupo es miembro. La función es transitiva.|
|[getMemberObjects](../api/group_getmemberobjects.md)|Colección string|Devuelve todos los grupos de los que el grupo es miembro. La función es transitiva. |
|[Create setting](../api/groupsetting_post_groupsettings.md) | [groupSetting](groupsetting.md) |Crea un objeto de configuración según una plantilla de groupSettingTemplate. La solicitud POST debe proporcionar settingValues para toda la configuración establecida en la plantilla. Solo se pueden usar plantillas específicas de grupos para esta operación.|
|[Get setting](../api/groupsetting_get.md) | [groupSetting](groupsetting.md) | Lee las propiedades de un objeto de configuración específico. |
|[List settings](../api/groupsetting_list.md) | Colección de [groupSetting](groupsetting.md) | Enumera las propiedades de todos los objetos de configuración. |
|[Update setting](../api/groupsetting_update.md) | [groupSetting](groupsetting.md) | Actualiza el objeto de configuración. |
|[Delete setting](../api/groupsetting_delete.md) | Ninguno | Elimina un objeto de configuración. |
|**Calendario**| | |
|[Crear evento](../api/group_post_events.md) |[evento](event.md)| Crea un evento al publicarlo en la colección de eventos.|
|[Obtener evento](../api/group_get_event.md) |[evento](event.md)|Lee las propiedades de un objeto de evento.|
|[Lista de eventos](../api/group_list_events.md) |Colección [event](event.md)| Obtiene una colección de objetos de evento.|
|[Actualizar evento](../api/group_update_event.md) |Ninguno|Actualiza las propiedades del objeto de evento.|
|[Eliminar evento](../api/group_delete_event.md) |Ninguno|Elimina el objeto de evento.|
|[Lista de calendarView](../api/group_list_calendarview.md) |Colección de [eventos](event.md)| Obtiene una colección de eventos en un intervalo de tiempo especificado.|
|**Conversaciones**| | |
|[Create conversation](../api/group_post_conversations.md) |[conversación](conversation.md)| Crea una conversación al publicarla en la colección de conversaciones.|
|[Obtener conversación](../api/group_get_conversation.md) |[conversación](conversation.md)| Lee las propiedades de un objeto de conversación.|
|[Lista de conversaciones](../api/group_list_conversations.md) |Colección de [conversaciones](conversation.md)| Obtiene una colección de objetos de conversación.|
|[Eliminar conversación](../api/group_delete_conversation.md) |Ninguno|Elimina un objeto de conversación.|
|[Obtener conversación](../api/group_get_thread.md) |[conversationThread](conversationthread.md)| Lee las propiedades de un objeto de conversación.|
|[Lista de conversaciones](../api/group_list_threads.md) |Colección [conversationThread](conversationthread.md)| Obtiene todas las conversaciones de un grupo.|
|[Actualizar conversación](../api/group_update_thread.md) |Ninguno| Actualiza las propiedades de un objeto de conversación.|
|[Eliminar conversación](../api/group_delete_thread.md) |Ninguno| Elimina un objeto de conversación.|
|[Lista de acceptedSenders](../api/group_list_acceptedsenders.md) |Colección [directoryObject](directoryobject.md)| Obtiene una lista de usuarios o grupos que se encuentran en la lista de acceptedSenders de este grupo.|
|[Agregar acceptedSenders](../api/group_post_acceptedsenders.md) |[directoryObject](directoryobject.md)| Agrega un usuario o grupo a la colección acceptSenders.|
|[Eliminar acceptedSender](../api/group_delete_acceptedsenders.md) |[directoryObject](directoryobject.md)| Elimina a un usuario o grupo de la colección acceptedSenders.|
|[Enumerar rejectedSenders](../api/group_list_rejectedsenders.md) |Colección [directoryObject](directoryobject.md)| Obtiene una lista de usuarios o grupos que se encuentran en la lista de rejectedSenders de este grupo.|
|[Agregar rejectedSender](../api/group_post_rejectedsenders.md) |[directoryObject](directoryobject.md)| Agrega un nuevo usuario o grupo a la colección rejectedSenders.|
|[Eliminar rejectedSender](../api/group_delete_rejectedsenders.md) |[directoryObject](directoryobject.md)| Elimina un nuevo usuario o grupo de la colección rejectedSenders.|
|[Create setting](../api/groupsetting_post_groupsettings.md) | [groupSetting](groupsetting.md) |Crea un objeto de configuración según una plantilla de groupSettingTemplate. La solicitud POST debe proporcionar settingValues para toda la configuración establecida en la plantilla. Solo se pueden usar plantillas específicas de grupos para esta operación.|
|[Get setting](../api/groupsetting_get.md) | [groupSetting](groupsetting.md) | Lee las propiedades de un objeto de configuración específico. |
|[List settings](../api/groupsetting_list.md) | Colección de [groupSetting](groupsetting.md) | Enumera las propiedades de todos los objetos de configuración. |
|[Configuración de actualización](../api/groupsetting_update.md) | Ninguno | Actualiza el objeto de configuración. |
|[Delete setting](../api/groupsetting_delete.md) | Ninguno | Elimina un objeto de configuración. |
|**Extensiones abiertas**| | |
|[Crear extensión abierta](../api/opentypeextension_post_opentypeextension.md) |[openTypeExtension](opentypeextension.md)| Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o un recurso existente.|
|[Obtener extensión abierta](../api/opentypeextension_get.md) |Colección [openTypeExtension](opentypeextension.md)| Obtiene una extensión abierta identificada por el nombre de extensión.|
|**Extensiones de esquema**| | |
|[Agregar valores de extensión de esquema](../../../concepts/extensibility_schema_groups.md) || Crea una definición de extensión de esquema y, después, la usa para agregar datos escritos personalizados a un recurso.|
|**Otros recursos de grupo**| | |
|[Enumerar fotos](../api/group_list_photos.md) |Colección [profilePhoto](photo.md)| Obtiene una colección de fotos de perfil para el grupo.|
|[Enumerar plannerPlans](../api/plannergroup_list_plans.md) |Colección [plannerPlan](plannerPlan.md)| Obtiene planes de Planner que pertenecen al grupo.|
|**Configuración de usuario**| | |
|[addFavorite](../api/group_addfavorite.md)|Ninguno|Agrega el grupo a la lista de grupos favoritos del usuario actual. Compatible solo con grupos de Office 365.|
|[removeFavorite](../api/group_removefavorite.md)|Ninguno|Quita el grupo de la lista de grupos favoritos del usuario actual. Compatible solo con grupos de Office 365.|
|[Enumerar memberOf](../api/group_list_memberof.md) |Colección [directoryObject](directoryobject.md)| Obtiene los grupos y las unidades administrativas de los que el usuario es miembro directo desde la propiedad de navegación **memberOf**.|
|[subscribeByMail](../api/group_subscribebymail.md)|Ninguno|Establece la propiedad isSubscribedByMail como **true**. Permite que el usuario actual pueda recibir conversaciones de correo electrónico. Compatible solo con grupos de Office 365.|
|[unsubscribeByMail](../api/group_unsubscribebymail.md)|Ninguno|Establece la propiedad isSubscribedByMail como **false**. Impide que el usuario actual pueda recibir conversaciones de correo electrónico. Compatible solo con grupos de Office 365.|
|[resetUnseenCount](../api/group_resetunseencount.md)|Ninguno|Restablece a 0 la unseenCount de todas las publicaciones que el usuario actual no ha visto desde su última visita. Compatible solo con grupos de Office 365.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|allowExternalSenders|Booleano|El valor predeterminado es **false**. Indica si los usuarios externos a la organización pueden enviar mensajes al grupo.|
|autoSubscribeNewMembers|Booleano|El valor predeterminado es **false**. Indica si los miembros agregados al grupo se suscribirán de forma automática para recibir notificaciones por correo electrónico. Puede establecer esta propiedad en una solicitud PATCH del grupo; no la establezca en la solicitud POST inicial que crea el grupo.|
|classification|Cadena|Describe una clasificación para el grupo (como impacto en el negocio bajo, medio o alto). Los valores válidos para esta propiedad se definen mediante la creación de un valor [setting](groupsetting.md) ClassificationList, basado en la [definición de plantilla](groupsettingtemplate.md).|
|createdDateTime|DateTimeOffset| Marca de tiempo de cuando se creó el grupo. El valor no puede modificarse y se rellena automáticamente al crear el grupo. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura. |
|description|Cadena|Una descripción opcional del grupo. |
|displayName|Cadena|El nombre para mostrar del grupo. Esta propiedad es necesaria cuando se crea un grupo y no se puede borrar durante las actualizaciones. Es compatible con $filter y $orderby.|
|groupTypes|Colección string| Especifica el tipo de grupo que se va a crear. Los valores posibles son **Unified** para crear un grupo de Office 365 o **DynamicMembership** para grupos dinámicos.  Para los demás tipos de grupos, como los grupos con seguridad habilitada y los grupos de seguridad habilitados para correo electrónico, no establezca esta propiedad. Es compatible con $filter.|
|id|Cadena|El identificador único del grupo. Heredado de [directoryObject](directoryobject.md). Clave. No admite valores NULL. Solo lectura.|
|isSubscribedByMail|Booleano|El valor predeterminado es **true**. Indica si el usuario actual está suscrito para recibir conversaciones de correo electrónico.|
|mail|Cadena|La dirección SMTP del grupo, por ejemplo: "serviceadmins@contoso.onmicrosoft.com". Solo lectura. Es compatible con $filter.|
|mailEnabled|Booleano|Especifica si el grupo está habilitado para correo. Si la propiedad **securityEnabled** también es **true**, el grupo es un grupo de seguridad habilitado para correo electrónico; en caso contrario, el grupo es un grupo de distribución de Microsoft Exchange.|
|mailNickname|Cadena|Alias de correo del grupo, único en la organización. Esta propiedad debe especificarse al crear un grupo. Admite $filter.|
|onPremisesLastSyncDateTime|DateTimeOffset|Indica la última vez que el grupo se ha sincronizado con el directorio local. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura. Es compatible con $filter.|
|onPremisesSecurityIdentifier|Cadena|Contiene el identificador de seguridad local (SID) del grupo que se sincroniza desde un recurso local a la nube. Solo lectura. |
|onPremisesSyncEnabled|Booleano|**true** si este grupo está sincronizado desde un directorio local; **false** si este grupo se ha sincronizado originalmente desde un directorio local, pero ya no está sincronizado; **null** si este grupo no se ha sincronizado nunca desde un directorio local (valor predeterminado). Solo lectura. Es compatible con $filter.|
|proxyAddresses|Colección string| El operador **any** es necesario para las expresiones de filtro en las propiedades de varios valores. Solo lectura. No admite valores NULL. Es compatible con $filter. |
|renewedDateTime|DateTimeOffset| Marca de tiempo de la última vez que se renovó el grupo. Esto no se puede modificar directamente y solo se actualiza a través de la [acción de servicio de renovación](../api/group_renew.md). El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.|
|securityEnabled|Booleano|Especifica si el grupo es un grupo de seguridad. Si la propiedad **mailEnabled** también es true, el grupo es un grupo de seguridad habilitado para correo electrónico; de lo contrario, es un grupo de seguridad. Debe ser **false** para grupos de Office 365. Es compatible con $filter.|
|unseenCount|Int32|Número de mensajes que el usuario actual no ha visto desde su última visita.|
|visibility|Cadena| Especifica la visibilidad de un grupo de Office 365. Los valores posibles son: **Private**, **Public**, **HiddenMembership** o vacío (que se interpreta como **Public**).|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|acceptedSenders|Colección [directoryObject](directoryobject.md)|La lista de usuarios o grupos que tienen permiso para crear publicaciones o eventos de calendario en este grupo. Si esta lista no está vacía, solo pueden publicar los usuarios o grupos enumerados en ella.|
|calendario|[calendario](calendar.md)|El calendario del grupo. Solo lectura.|
|calendarView|Colección [event](event.md)|La vista Calendario del calendario. Solo lectura.|
|conversations|Colección [conversation](conversation.md)|Las conversaciones del grupo.|
|createdOnBehalfOf|[directoryObject](directoryobject.md)| El usuario (o la aplicación) que creó el grupo. NOTA: No se establece si el usuario es un administrador. Solo lectura.|
|Unidad|[drive](drive.md)|La unidad predeterminada del grupo. Solo lectura.|
|drives|Colección [drive](drive.md)|Las unidades del grupo. Solo lectura.|
|events|Colección [event](event.md)|Los eventos de calendario del grupo.|
|extensions|Colección [Extension](extension.md)|La colección de extensiones abiertas definidas para el grupo. Solo lectura. Admite valores NULL.|
|groupLifecyclePolicies|Colección de [groupLifecyclePolicy](groupLifecyclePolicy.md)|La colección de las directivas de ciclo de vida para este grupo. Solo lectura. Admite valores NULL.|
|memberOf|Colección [directoryObject](directoryobject.md)|Grupos a los que pertenece este grupo. Métodos HTTP: GET (compatible con todos los grupos). Solo lectura. Admite valores NULL.|
|members|Colección [directoryObject](directoryobject.md)| Los usuarios y los grupos que son miembros de este grupo. Métodos HTTP: GET (compatible con todos los grupos), POST (compatible con grupos de Office 365, grupos de seguridad y los grupos de seguridad habilitados para correo), DELETE (compatible con grupos de Office 365 y grupos de seguridad). Admite valores NULL.|
|onenote|[Onenote](onenote.md)| Solo lectura.|
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
  "onPremisesSecurityIdentifier": "string",
  "onPremisesSyncEnabled": true,
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

- [Agregar datos personalizados a los recursos mediante extensiones](../../../concepts/extensibility_overview.md)
- [Agregar datos personalizados a los usuarios mediante extensiones abiertas](../../../concepts/extensibility_open_users.md)
- [Agregar datos personalizados a los grupos mediante extensiones de esquema](../../../concepts/extensibility_schema_groups.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
