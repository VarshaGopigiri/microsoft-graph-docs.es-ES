# <a name="user-resource-type"></a>tipo de recurso del usuario

Representa una cuenta de usuario de Azure AD. Se hereda de [directoryObject](directoryobject.md).


## <a name="methods"></a>Métodos
| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Obtener usuario](../api/user_get.md) | [usuario](user.md) |Lee las propiedades y las relaciones del objeto de usuario.|
|[Actualizar usuario](../api/user_update.md) | [usuario](user.md) |Actualiza el objeto de usuario. |
|[Eliminar usuario](../api/user_delete.md) | Ninguno |Elimina el objeto de usuario. |
|[Enumerar mensajes](../api/user_list_messages.md) |Colección [message](message.md)| Obtiene todos los mensajes del buzón del usuario que inició sesión.|
|[Crear mensaje](../api/user_post_messages.md) |[Mensaje](message.md)| Crea un nuevo mensaje publicándolo en la colección de mensajes.|
|[Enumerar mailFolders](../api/user_list_mailfolders.md) |Colección [mailFolder](mailfolder.md)| Obtiene la colección de carpetas de correo en la carpeta raíz del usuario que inició sesión. |
|[Crear mailFolder](../api/user_post_mailfolders.md) |[MailFolder](mailfolder.md)| Crea un nuevo mailFolder publicándolo en la colección mailFolders.|
|[sendMail](../api/user_sendmail.md)|Ninguno|Envía el mensaje especificado en el cuerpo de la solicitud.|
|[Enumerar eventos](../api/user_list_events.md) |Colección [event](event.md)| Obtiene una lista de los objetos de evento del buzón del usuario. La lista contiene patrones de serie y reuniones de instancia única.|
|[Crear evento](../api/user_post_events.md) |[Evento](event.md)| Crea un nuevo evento publicándolo en la colección de eventos.|
|[Enumerar calendarios](../api/user_list_calendars.md) |Colección [calendar](calendar.md)| Obtiene una colección de objetos de calendario.|
|[Crear calendario](../api/user_post_calendars.md) |[Calendario](calendar.md)| Crea un nuevo calendario publicándolo en la colección de calendarios.|
|[Enumerar calendarGroups](../api/user_list_calendargroups.md) |Colección [calendarGroup](calendargroup.md)| Obtiene una colección de objetos calendarGroup.|
|[Crear calendarGroup](../api/user_post_calendargroups.md) |[CalendarGroup](calendargroup.md)| Crea un nuevo calendarGroup publicándolo en la colección calendarGroups.|
|[Enumerar calendarView](../api/user_list_calendarview.md) |Colección [event](event.md)| Obtiene una colección de objetos de evento.|
|[Enumerar contactos](../api/user_list_contacts.md) |Colección [contacts](contact.md)| Obtiene una colección de contactos de la carpeta de contactos predeterminada del usuario que inició sesión.|
|[Crear contacto](../api/user_post_contacts.md) |[Contacto](contact.md)| Crea un nuevo contacto publicándolo en la colección de contactos.|
|[Enumerar contactFolders](../api/user_list_contactfolders.md) |Colección [contactFolder](contactfolder.md)| Obtiene la colección de carpetas de contactos de la carpeta de contactos predeterminada del usuario que inició sesión.|
|[Crear ContactFolder](../api/user_post_contactfolders.md) |[ContactFolder](contactfolder.md)| Crea un nuevo contactFolder publicándolo en la colección contactFolders.|
|[Enumerar directReports](../api/user_list_directreports.md) |Colección [directoryObject](directoryobject.md)| Obtiene los usuarios y contactos que informan al usuario desde la propiedad de navegación directReports.|
|[Enumerar administrador](../api/user_list_manager.md) |[directoryObject](directoryobject.md) | Obtiene el usuario o el contacto que es administrador de este usuario desde la propiedad de navegación manager.|
|[Enumerar memberOf](../api/user_list_memberof.md) |Colección [directoryObject](directoryobject.md)| Obtiene los grupos y los roles de directorio de los que el usuario es miembro directo desde la propiedad de navegación memberOf.|
|[Enumerar ownedDevices](../api/user_list_owneddevices.md) |Colección [directoryObject](directoryobject.md)| Obtiene los dispositivos que son propiedad del usuario desde la propiedad de navegación ownedDevices.|
|[Enumerar ownedObjects](../api/user_list_ownedobjects.md) |Colección [directoryObject](directoryobject.md)| Obtiene los objetos de directorio que son propiedad del usuario desde la propiedad de navegación ownedObjects.|
|[Enumerar registeredDevices](../api/user_list_registereddevices.md) |Colección [directoryObject](directoryobject.md)| Obtiene los dispositivos registrados del usuario desde la propiedad de navegación registeredDevices.|
|[Enumerar createdObjects](../api/user_list_createdobjects.md) |Colección [directoryObject](directoryobject.md)| Obtiene los objetos de directorio creados por el usuario desde la propiedad de navegación createdObjects.|
|[assignLicense](../api/user_assignlicense.md)|[user](user.md)|Agrega o quita suscripciones del usuario. También puede habilitar y deshabilitar los planes específicos asociados a una suscripción.|
|[checkMemberGroups](../api/user_checkmembergroups.md)|Colección string|Comprueba la pertenencia a una lista de grupos. La comprobación es transitiva.|
|[getMemberGroups](../api/user_getmembergroups.md)|Colección string|Devuelve todos los grupos de los que el usuario es miembro. La comprobación es transitiva.|
|[getMemberObjects](../api/user_getmemberobjects.md)|Colección string| Devuelve todos los grupos y los roles de directorio de los que el usuario es miembro. La comprobación es transitiva. |
|[reminderView](../api/user_reminderview.md)|Colección [reminder](reminder.md)|Devuelve una lista de los avisos de calendario entre de las horas de inicio y finalización especificadas.|



## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|aboutMe|Cadena|Un campo de entrada de texto de forma libre para que el usuario se describa a sí mismo.|
|accountEnabled|Booleano| **true** si la cuenta está habilitada; en caso contrario, **false**. Esta propiedad es necesaria cuando se crea un usuario. Es compatible con $filter.    |
|assignedLicenses|Colección [assignedLicense](assignedlicense.md)|Las licencias asignadas al usuario. No admite valores NULL.            |
|assignedPlans|Colección [assignedPlan](assignedplan.md)|Los planes asignados al usuario. Solo lectura. No admite valores NULL. |
|birthday|DateTimeOffset|El cumpleaños del usuario. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|city|String|La ciudad en la que se encuentra el usuario. Es compatible con $filter.|
|country|String|El país o la región en la que se encuentra el usuario. Por ejemplo: "US" o "UK". Es compatible con $filter.|
|department|String|El nombre del departamento en el que trabaja el usuario. Es compatible con $filter.|
|displayName|String|El nombre del usuario que aparece en la libreta de direcciones. Suele ser la combinación del nombre del usuario, la inicial del segundo nombre y el apellido. Esta propiedad es necesaria cuando se crea un usuario y no se puede borrar durante las actualizaciones. Es compatible con $filter y $orderby.|
|givenName|String|El nombre (nombre de pila) del usuario. Es compatible con $filter.|
|hireDate|DateTimeOffset|La fecha de contratación del usuario. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|id|String|El identificador único del usuario. Heredado de [directoryObject](directoryobject.md). Clave. No admite valores NULL. Solo lectura.|
|interests|Colección string|Una lista para que el usuario describa sus intereses.|
|jobTitle|String|El puesto del usuario. Es compatible con $filter.|
|mail|String|La dirección SMTP del usuario, por ejemplo: "jeff@contoso.onmicrosoft.com". Solo lectura. Es compatible con $filter.|
|mailboxSettings|[mailboxSettings](mailboxsettings.md)|Configuración del buzón principal del usuario que ha iniciado sesión. Puede [obtener](../api/user_get_mailboxsettings.md) o [actualizar](../api/user_update_mailboxsettings.md) las opciones para enviar respuestas automáticas a mensajes entrantes, de configuración regional y de zona horaria.|
|mailNickname|String|El alias de correo del usuario. Esta propiedad debe especificarse al crear un usuario. Es compatible con $filter.|
|mobilePhone|Cadena|El número de teléfono móvil principal del usuario.|
|mySite|Cadena|La dirección URL del sitio personal del usuario.|
|officeLocation|Cadena|La ubicación de la oficina del lugar de trabajo del usuario.|
|onPremisesImmutableId|String|Esta propiedad se utiliza para asociar una cuenta local de usuario de Active Directory a su objeto de usuario de Azure AD. Esta propiedad debe especificarse al crear una nueva cuenta de usuario en Graph si utiliza un dominio federado para la propiedad **userPrincipalName** (UPN) del usuario. **Importante**: Los caracteres **$** y **_** no se pueden utilizar a la hora de especificar esta propiedad. Es compatible con $filter.                            |
|onPremisesLastSyncDateTime|DateTimeOffset|Indica la última vez que se ha sincronizado el objeto con el directorio local. Por ejemplo: "2013-02-16T03:04:54Z". El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.|
|onPremisesSecurityIdentifier|String|Contiene el identificador de seguridad local (SID) del usuario que se sincroniza desde un recurso local a la nube. Solo lectura.|
|onPremisesSyncEnabled|Booleano| **true** si este objeto está sincronizado desde un directorio local; **false** si este objeto se ha sincronizado originalmente desde un directorio local, pero ya no está sincronizado; **null** si este objeto no se ha sincronizado nunca desde un directorio local (valor predeterminado). Solo lectura |
|passwordPolicies|String|Especifica las directivas de contraseña del usuario. Este valor es una enumeración con un valor posible de "DisableStrongPassword" y permite especificar contraseñas menos seguras que la directiva predeterminada. También se puede especificar "DisablePasswordExpiration". Los dos se pueden especificar a la vez. Por ejemplo: "DisablePasswordExpiration, DisableStrongPassword".|
|passwordProfile|[PasswordProfile](passwordprofile.md)|Especifica el perfil de contraseña del usuario. El perfil contiene la contraseña del usuario. Esta propiedad es necesaria cuando se crea un usuario. La contraseña del perfil debe cumplir los requisitos mínimos especificados por la propiedad **passwordPolicies**. De manera predeterminada, se requiere una contraseña segura.|
|pastProjects|Colección string|Una lista para que el usuario enumere sus últimos proyectos.|
|postalCode|String|El código postal de la dirección del usuario. El código postal es específico del país o de la región del usuario. En Estados Unidos, este atributo contiene el código postal.|
|preferredLanguage|String|El idioma preferido del usuario. Debe seguir el código ISO 639-1. Por ejemplo, "en-US".|
|preferredName|Cadena|El nombre preferido del usuario.|
|provisionedPlans|Colección [ProvisionedPlan](provisionedplan.md)|Los planes que se ha aprovisionado para el usuario. Solo lectura. No admite valores NULL. |
|proxyAddresses|Colección string|Por ejemplo: `["SMTP: bob@contoso.com", "smtp: bob@sales.contoso.com"]` El operador **any** es necesario para las expresiones de filtro en las propiedades de varios valores. Solo lectura, no admite valores NULL. Es compatible con $filter.          |
|responsibilities|Colección string|Una lista para que el usuario enumere sus responsabilidades.|
|schools|Colección string|Una lista para que el usuario enumere las escuelas a las que ha ido.|
|skills|Colección string|Una lista para que el usuario enumere sus aptitudes.|
|state|String|El estado o la provincia de la dirección del usuario. Es compatible con $filter.|
|streetAddress|Cadena|La dirección postal del lugar de trabajo del usuario.|
|surname|String|El apellido (o apellidos) del usuario. Es compatible con $filter.|
|usageLocation|String|Un código de país de dos letras (norma ISO 3166). Es necesario para los usuarios a los que se asignarán licencias debido a un requisito legal para comprobar la disponibilidad de los servicios en los países.  Algunos ejemplos son: "US", "JP" y "GB". No admite valores NULL. Es compatible con $filter.|
|userPrincipalName|String|El nombre principal del usuario (UPN) del usuario. El UPN es un nombre de inicio de sesión de Internet del usuario basado en la norma RFC 822. Por convención, se debe asignar al nombre de correo electrónico del usuario. El formato general es alias@dominio, donde el dominio debe estar presente en la colección de dominios verificados del inquilino. Esta propiedad es necesaria cuando se crea un usuario. Se puede acceder a los dominios verificados del inquilino desde la propiedad **verifiedDomains** en [organización](organization.md). Es compatible con $filter y $orderby.
|userType|String|Un valor de cadena que puede utilizarse para clasificar los tipos de usuario en el directorio. Por ejemplo: "Miembro" e "Invitado". Es compatible con $filter.          |

## <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|calendar|[Calendar](calendar.md)|El calendario principal del usuario. Solo lectura.|
|calendarGroups|Colección [calendarGroup](calendargroup.md)|Los grupos de calendario del usuario. Solo lectura. Admite valores NULL.|
|calendarView|Colección [event](event.md)|La vista Calendario del calendario. Solo lectura. Admite valores NULL.|
|calendars|Colección [calendar](calendar.md)|Los calendarios del usuario. Solo lectura. Admite valores NULL.|
|contactFolders|Colección [contactFolder](contactfolder.md)|Las carpetas de contactos del usuario. Solo lectura. Admite valores NULL.|
|contactos|Colección [contacts](contact.md)|Los contactos del usuario. Solo lectura. Admite valores NULL.|
|createdObjects|Colección [directoryObject](directoryobject.md)|Objetos de directorio creados por el usuario. Solo lectura. Admite valores NULL.|
|directReports|Colección [directoryObject](directoryobject.md)|Los usuarios y contactos que informan al usuario (los usuarios y contactos cuya propiedad manager está establecida para este usuario). Solo lectura. Admite valores NULL. |
|drive|[drive](drive.md)|OneDrive del usuario. Solo lectura.|
|events|Colección [event](event.md)|Los eventos del usuario. La opción predeterminada muestra eventos en el calendario predeterminado. Solo lectura. Admite valores NULL.|
|inferenceClassification | [inferenceClassification](inferenceClassification.md) | Clasificación de relevancia de los mensajes del usuario según las designaciones explícitas que invalidan una relevancia o importancia inferida. |
|mailFolders|Colección [MailFolder](mailfolder.md)| Las carpetas de correo del usuario. Solo lectura. Admite valores NULL.|
|manager|[directoryObject](directoryobject.md)|El usuario o el contacto que es administrador de este usuario. Solo lectura. (métodos HTTP: GET, PUT y DELETE).|
|memberOf|Colección [directoryObject](directoryobject.md)|Los grupos y los roles de directorio de los que el usuario es miembro. Solo lectura. Admite valores NULL.|
|messages|Colección [message](message.md)|Los mensajes en un buzón o una carpeta. Solo lectura. Admite valores NULL.|
|ownedDevices|Colección [directoryObject](directoryobject.md)|Dispositivos que son propiedad del usuario. Solo lectura. Admite valores NULL.|
|ownedObjects|Colección [directoryObject](directoryobject.md)|Objetos de directorio que son propiedad del usuario. Solo lectura. Admite valores NULL.|
|Foto|[profilePhoto](profilephoto.md)| La foto de perfil del usuario. Solo lectura.|
|registeredDevices|Colección [directoryObject](directoryobject.md)|Dispositivos del usuario que están registrados. Solo lectura. Admite valores NULL.|


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "appRoleAssignments",
    "calendar",
    "calendarGroups",
    "calendarView",
    "calendars",
    "contactFolders",
    "contacts",
    "createdObjects",
    "directReports",
    "drive",
    "events",
    "joinedGroups",
    "mailFolders",
    "manager",
    "memberOf",
    "messages",
    "oauth2PermissionGrants",
    "ownedDevices",
    "ownedObjects",
    "photo",
    "registeredDevices"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.user"
}-->

```json
{
  "aboutMe": "string",
  "accountEnabled": true,
  "assignedLicenses": [{"@odata.type": "microsoft.graph.assignedLicense"}],
  "assignedPlans": [{"@odata.type": "microsoft.graph.assignedPlan"}],
  "birthday": "String (timestamp)",
  "businessPhones": ["string"],
  "city": "string",
  "companyName": "string",
  "country": "string",
  "department": "string",
  "displayName": "string",
  "givenName": "string",
  "hireDate": "String (timestamp)",
  "id": "string (identifier)",
  "interests": ["string"],
  "jobTitle": "string",
  "mail": "string",
  "mailboxSettings": {"@odata.type": "microsoft.graph.mailboxSettings"},
  "mailNickname": "string",
  "mobilePhone": "string",
  "mySite": "string",
  "officeLocation": "string",
  "onPremisesImmutableId": "string",
  "onPremisesLastSyncDateTime": "String (timestamp)",
  "onPremisesSecurityIdentifier": "string",
  "onPremisesSyncEnabled": true,
  "passwordPolicies": "string",
  "passwordProfile": {"@odata.type": "microsoft.graph.passwordProfile"},
  "pastProjects": ["string"],
  "postalCode": "string",
  "preferredLanguage": "string",
  "preferredName": "string",
  "provisionedPlans": [{"@odata.type": "microsoft.graph.provisionedPlan"}],
  "proxyAddresses": ["string"],
  "responsibilities": ["string"],
  "schools": ["string"],
  "skills": ["string"],
  "state": "string",
  "streetAddress": "string",
  "surname": "string",
  "usageLocation": "string",
  "userPrincipalName": "string",
  "userType": "string",

  "calendar": { "@odata.type": "microsoft.graph.calendar" },
  "calendarGroups": [{ "@odata.type": "microsoft.graph.calendarGroup" }],
  "calendarView": [{ "@odata.type": "microsoft.graph.event" }],
  "calendars": [ {"@odata.type": "microsoft.graph.calendar"} ],
  "contacts": [ { "@odata.type": "microsoft.graph.contact" } ],
  "contactFolders": [ { "@odata.type": "microsoft.graph.contactFolder" } ],
  "createdObjects": [ { "@odata.type": "microsoft.graph.directoryObject" } ],
  "directReports": [ { "@odata.type": "microsoft.graph.directoryObject" } ],
  "drive": { "@odata.type": "microsoft.graph.drive" },
  "events": [ { "@odata.type": "microsoft.graph.event" } ],
  "inferenceClassification": { "@odata.type": "microsoft.graph.inferenceClassification" },
  "mailFolders": [ { "@odata.type": "microsoft.graph.mailFolder" } ],
  "manager": { "@odata.type": "microsoft.graph.directoryObject" },
  "memberOf": [ { "@odata.type": "microsoft.graph.directoryObject" } ],
  "messages": [ { "@odata.type": "microsoft.graph.message" } ],
  "ownedDevices": [ { "@odata.type": "microsoft.graph.directoryObject" } ],
  "photo": { "@odata.type": "microsoft.graph.profilePhoto" },
  "registeredDevices": [ { "@odata.type": "microsoft.graph.directoryObject" } ]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
