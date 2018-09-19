# <a name="user-resource-type"></a>tipo de recurso del usuario

Representa una cuenta de usuario de Azure AD. Se hereda de [directoryObject](directoryobject.md).

Este recurso admite:

- Agregar sus propios datos a las propiedades personalizadas como [extensiones](../../../concepts/extensibility_overview.md).
- Suscribirse a [las notificaciones de cambios](../../../concepts/webhooks.md).
- Usar una [consulta delta](../../../concepts/delta_query_overview.md) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/user_delta.md).

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Enumerar usuarios](../api/user_list.md) |Colección [user](user.md)| Obtiene una lista de objetos de usuario.|
|[Crear usuario](../api/user_post_users.md) |[user](user.md)| Crea un objeto de usuario nuevo.|
|[Obtener usuario](../api/user_get.md) | [user](user.md) |Lee las propiedades y las relaciones del objeto de usuario.|
|[Actualizar usuario](../api/user_update.md) | [user](user.md) |Actualiza el objeto de usuario. |
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
|[Enumerar licenseDetails](../api/user_list_licensedetails.md) |Colección [licenseDetails](licensedetails.md)| Obtenga una colección de objetos licenseDetails.|
|[checkMemberGroups](../api/user_checkmembergroups.md)|Colección string|Comprueba la pertenencia a una lista de grupos. La comprobación es transitiva.|
|[getMemberGroups](../api/user_getmembergroups.md)|Colección string|Devuelve todos los grupos de los que el usuario es miembro. La comprobación es transitiva.|
|[getMemberObjects](../api/user_getmemberobjects.md)|Colección string| Devuelve todos los grupos y los roles de directorio de los que el usuario es miembro. La comprobación es transitiva. |
|[reminderView](../api/user_reminderview.md)|Colección [reminder](reminder.md)|Devuelve una lista de los avisos de calendario entre las horas de inicio y finalización especificadas.|
|[delta](../api/user_delta.md)|Colección user| Obtener los cambios incrementales de usuarios. |
|**Extensiones abiertas**| | |
|[Crear extensión abierta](../api/opentypeextension_post_opentypeextension.md) |[openTypeExtension](opentypeextension.md)| Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o un recurso existente.|
|[Obtener extensión abierta](../api/opentypeextension_get.md) |Colección [openTypeExtension](opentypeextension.md)| Obtiene una extensión abierta identificada por el nombre de extensión.|
|**Extensiones de esquema**| | |
|[Agregar valores de extensión de esquema](../../../concepts/extensibility_schema_groups.md) || Cree una definición de extensión de esquema y, después, úsela para agregar datos escritos personalizados a un recurso.|

## <a name="properties"></a>Propiedades

| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|aboutMe|Cadena|Un campo de entrada de texto de forma libre para que el usuario se describa a sí mismo.|
|accountEnabled|Booleano| **true** si la cuenta está habilitada; en caso contrario, **false**. Esta propiedad es necesaria cuando se crea un usuario. Es compatible con $filter.    |
|ageGroup|Cadena|Establece el grupo de edad del usuario. Valores permitidos: `null`, `minor`, `notAdult` y `adult`. Consulte las [definiciones de propiedades de grupo de edad legal](#legal-age-group-property-definitions) para obtener más información. |
|assignedLicenses|Colección [assignedLicense](assignedlicense.md)|Las licencias asignadas al usuario. No admite valores NULL.            |
|assignedPlans|Colección [assignedPlan](assignedplan.md)|Los planes asignados al usuario. Solo lectura. No admite valores NULL. |
|birthday|DateTimeOffset|El cumpleaños del usuario. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|businessPhones|Colección string|Los números de teléfono del usuario. NOTA: Aunque se trata de una colección de cadenas, solo se puede establecer un número para esta propiedad.|
|city|Cadena|La ciudad en la que se encuentra el usuario. Es compatible con $filter.|
|companyName | Cadena | El nombre de la compañía a la que está asociado el usuario. Solo lectura. |
|consentProvidedForMinor|Cadena|Establece si se ha obtenido el consentimiento para menores. Valores permitidos: `null`, `granted`, `denied` y `notRequired`. Consulte las [definiciones de propiedades de grupo de edad legal](#legal-age-group-property-definitions) para obtener más información.|
|country|Cadena|El país o la región en la que se encuentra el usuario. Por ejemplo: "US" o "UK". Es compatible con $filter.|
|createdDateTime | DateTimeOffset |La fecha de creación del objeto de usuario. |
|department|Cadena|El nombre del departamento en el que trabaja el usuario. Es compatible con $filter.|
|displayName|Cadena|El nombre del usuario que aparece en la libreta de direcciones. Suele ser la combinación del nombre del usuario, la inicial del segundo nombre y el apellido. Esta propiedad es necesaria cuando se crea un usuario y no se puede borrar durante las actualizaciones. Es compatible con $filter y $orderby.|
|givenName|Cadena|El nombre (nombre de pila) del usuario. Es compatible con $filter.|
|hireDate|DateTimeOffset|La fecha de contratación del usuario. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|id|Cadena|El identificador único del usuario. Heredado de [directoryObject](directoryobject.md). Clave. No admite valores NULL. Solo lectura.|
|imAddresses|Colección string|Direcciones del protocolo de inicio de sesión (SIP) de voz sobre IP (VOIP) del servicio de mensajería instantánea correspondientes al usuario. Solo lectura.|
|interests|Colección string|Una lista para que el usuario describa sus intereses.|
|jobTitle|Cadena|El puesto del usuario. Es compatible con $filter.|
|legalAgeGroupClassification|Cadena| Se usa en las aplicaciones empresariales para determinar el grupo de edad legal del usuario. Esta propiedad es de sólo lectura y calculadas en función de `ageGroup` y `consentProvidedForMinor` propiedades. Valores permitidos: `null`, `minorWithOutParentalConsent`, `minorWithParentalConsent`, `minorNoParentalConsentRequired`, `notAdult` y `adult`. Consulte las [definiciones de propiedades de grupo de edad legal](#legal-age-group-property-definitions) para obtener más información.|
|mail|Cadena|La dirección SMTP del usuario, por ejemplo: "jeff@contoso.onmicrosoft.com". Solo lectura. Es compatible con $filter.|
|mailboxSettings|[mailboxSettings](mailboxsettings.md)|Configuración del buzón principal del usuario que ha iniciado sesión. Puede [obtener](../api/user_get_mailboxsettings.md) o [actualizar](../api/user_update_mailboxsettings.md) las opciones para enviar respuestas automáticas a mensajes entrantes, de configuración regional y de zona horaria.|
|mailNickname|Cadena|El alias de correo del usuario. Esta propiedad debe especificarse al crear un usuario. Es compatible con $filter.|
|mobilePhone|Cadena|El número de teléfono móvil principal del usuario.|
|mySite|Cadena|La dirección URL del sitio personal del usuario.|
|officeLocation|Cadena|La ubicación de la oficina del lugar de trabajo del usuario.|
|onPremisesDomainName|Cadena| Contiene los locales `domainFQDN`, también se conoce como dnsDomainName sincronizado desde el directorio local. La propiedad solo se rellena para los clientes que sincronizan su directorio local a Azure Active Directory a través de Azure AD Connect. Solo lectura. |
|onPremisesExtensionAttributes|[OnPremisesExtensionAttributes](onpremisesextensionattributes.md)|Contiene extensionAttributes 1-15 para el usuario. Tenga en cuenta que los atributos de extensión individuales no se pueden seleccionar ni filtrar. Para un usuario `onPremisesSyncEnabled`, este conjunto de propiedades se controla localmente y es de solo lectura. Para un usuario solo en la nube (donde `onPremisesSyncEnabled` es false), estas propiedades se pueden establecer durante la creación o la actualización. |
|onPremisesImmutableId|Cadena|Esta propiedad se utiliza para asociar una cuenta local de usuario de Active Directory a su objeto de usuario de Azure AD. Esta propiedad debe especificarse al crear una nueva cuenta de usuario en Graph si utiliza un dominio federado para la propiedad **userPrincipalName** (UPN) del usuario. **Importante**: Los caracteres **$** y **_** no se pueden utilizar a la hora de especificar esta propiedad. Es compatible con $filter.                            |
|onPremisesLastSyncDateTime|DateTimeOffset|Indica la última vez que se ha sincronizado el objeto con el directorio local. Por ejemplo: "2013-02-16T03:04:54Z". El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.|
|onPremisesProvisioningErrors|Colección [onPremisesProvisioningError](onpremisesprovisioningerror.md)| Errores al usar el producto de sincronización de Microsoft durante el aprovisionamiento. |
|onPremisesSamAccountName|Cadena| Contiene los locales `samAccountName` sincronizados desde el directorio local. La propiedad solo se rellena para los clientes que sincronizan su directorio local a Azure Active Directory a través de Azure AD Connect. Solo lectura. |
|onPremisesSecurityIdentifier|Cadena|Contiene el identificador de seguridad local (SID) del usuario que se sincroniza desde un recurso local a la nube. Solo lectura.|
|onPremisesSyncEnabled|Booleano| **true** si este objeto está sincronizado desde un directorio local; **false** si este objeto se ha sincronizado originalmente desde un directorio local, pero ya no está sincronizado; **null** si este objeto no se ha sincronizado nunca desde un directorio local (valor predeterminado). Solo lectura |
|onPremisesUserPrincipalName|Cadena| Contiene los locales `userPrincipalName` sincronizados desde el directorio local. La propiedad solo se rellena para los clientes que sincronizan su directorio local a Azure Active Directory a través de Azure AD Connect. Solo lectura. |
|passwordPolicies|Cadena|Especifica las directivas de contraseña del usuario. Este valor es una enumeración con un valor posible de "DisableStrongPassword" y permite especificar contraseñas menos seguras que la directiva predeterminada. También se puede especificar "DisablePasswordExpiration". Los dos se pueden especificar a la vez. Por ejemplo: "DisablePasswordExpiration, DisableStrongPassword".|
|passwordProfile|[PasswordProfile](passwordprofile.md)|Especifica el perfil de contraseña del usuario. El perfil contiene la contraseña del usuario. Esta propiedad es necesaria cuando se crea un usuario. La contraseña del perfil debe cumplir los requisitos mínimos especificados por la propiedad **passwordPolicies**. De manera predeterminada, se requiere una contraseña segura.|
|pastProjects|Colección string|Una lista para que el usuario enumere sus últimos proyectos.|
|postalCode|Cadena|El código postal de la dirección del usuario. El código postal es específico del país o de la región del usuario. En Estados Unidos, este atributo contiene el código postal.|
|preferredLanguage|Cadena|El idioma preferido del usuario. Debe seguir el código ISO 639-1. Por ejemplo, "en-US".|
|preferredName|Cadena|El nombre preferido del usuario.|
|provisionedPlans|Colección [ProvisionedPlan](provisionedplan.md)|Los planes que se ha aprovisionado para el usuario. Solo lectura. No admite valores NULL. |
|proxyAddresses|Colección string|Por ejemplo: `["SMTP: bob@contoso.com", "smtp: bob@sales.contoso.com"]` El operador **any** es necesario para las expresiones de filtro en las propiedades de varios valores. Solo lectura, no admite valores NULL. Es compatible con $filter.          |
|responsibilities|Colección string|Una lista para que el usuario enumere sus responsabilidades.|
|schools|Colección string|Una lista para que el usuario enumere las escuelas a las que ha ido.|
|skills|Colección string|Una lista para que el usuario enumere sus aptitudes.|
|state|Cadena|El estado o la provincia de la dirección del usuario. Es compatible con $filter.|
|streetAddress|Cadena|La dirección postal del lugar de trabajo del usuario.|
|surname|Cadena|El apellido (o apellidos) del usuario. Es compatible con $filter.|
|usageLocation|Cadena|Un código de país de dos letras (norma ISO 3166). Es necesario para los usuarios a los que se asignarán licencias debido a un requisito legal para comprobar la disponibilidad de los servicios en los países.  Algunos ejemplos son: "US", "JP" y "GB". No admite valores NULL. Es compatible con $filter.|
|userPrincipalName|Cadena|El nombre principal del usuario (UPN) del usuario. El UPN es un nombre de inicio de sesión de Internet del usuario basado en la norma RFC 822. Por convención, se debe asignar al nombre de correo electrónico del usuario. El formato general es alias@dominio, donde el dominio debe estar presente en la colección de dominios verificados del inquilino. Esta propiedad es necesaria cuando se crea un usuario. Se puede acceder a los dominios verificados del inquilino desde la propiedad **verifiedDomains** en [organización](organization.md). Es compatible con $filter y $orderby.
|userType|Cadena|Un valor de cadena que puede utilizarse para clasificar los tipos de usuario en el directorio. Por ejemplo: "Miembro" e "Invitado". Es compatible con $filter.          |

### <a name="legal-age-group-property-definitions"></a>Definiciones de propiedades de grupo de edad legal

En esta sección se explica cómo las tres propiedades del grupo de edad (`legalAgeGroupClassification`, `ageGroup` y `consentProvidedForMinor`) se usan por los administradores de Azure AD y los desarrolladores de aplicaciones de empresa para cumplir las reglamentaciones relacionadas con la edad.

Por ejemplo: Cameron es administrador de un directorio para una escuela de primaria en Holyport en el Reino Unido. Al principio del año escolar utiliza la documentación de admisión para obtener consentimiento de los padres del menor de edad según las reglamentaciones relacionadas con la edad del Reino Unido. El consentimiento obtenido del padre permite que la cuenta del menor de edad se use en la escuela Holyport y con Microsoft Apps. A continuación, Cameron crea todas las cuentas y establece ageGroup a "menor de edad" y consentProvidedForMinor a "concedido". Las aplicaciones utilizadas por sus estudiantes son entonces capaces de suprimir las características que no son adecuadas para menores.

#### <a name="legal-age-group-classification"></a>Clasificación de grupo de edad legal

Esta propiedad de solo lectura se usa en los desarrolladores de aplicaciones de empresa para garantizar el control correcto de un usuario en función de su grupo de edad legal. Se calcula en función de las propiedades de usuario `ageGroup` y `consentProvidedForMinor`.

| Valor    | #  |Descripción|
|:---------------|:--------|:----------|
|null|0|Valor predeterminado, ningún `ageGroup` se ha establecido para el usuario.|
|minorWithoutParentalConsent |1|(Reservado para uso futuro)|
|minorWithParentalConsent|2| El usuario se considera un menor de edad según las reglamentaciones relacionadas con la edad de su país o región y el administrador de la cuenta ha obtenido apropiado consentimiento de un padre o tutor.|
|adult|3|El usuario considera un contenido para adultos según las reglamentaciones relacionadas con la edad de su país o región.|
|notAdult|4|El usuario es de un país o región que tiene regulaciones adicionales relacionados con la edad (por ejemplo, Estados Unidos, Reino Unido, Unión Europea o Corea del sur) y la edad del usuario se encuentra entre la de un menor y la de un adulto (como está estipulado en función del país o región). Por lo general, esto significa que los adolescentes se consideran `notAdult` en países regulados.|
|minorNoParentalConsentRequired|5|El usuario es un menor de edad, pero es de un país o región que no tiene reglamentaciones relacionadas con la edad.|

#### <a name="age-group-and-minor-consent"></a>Grupo de edad y consentimiento del menor

Las propiedades de consentimiento del menor y grupo de edad son propiedades opcionales usadas por los administradores de Azure AD para ayudar a garantizar que el uso de una cuenta se controla correctamente según las reglas de las normativas relacionadas con la edad que rigen en el país o región del usuario.

#### <a name="agegroup-property"></a>Propiedad ageGroup

| Valor    | #  |Descripción|
|:---------------|:--------|:----------|
|null|0|Valor predeterminado, ningún `ageGroup` se ha establecido para el usuario.|
|minor|1|El usuario se considere un menor de edad.|
|notAdult|2|El usuario es de un país que tiene regulaciones estatutarias (Estados Unidos, Reino Unido, Unión Europea o Corea del Sur) y la edad del usuario es mayor que el límite superior de la edad del niño (según el país) y menor que el límite inferior de la edad del adulto (según lo estipulado en base al país o región). Básicamente, los adolescentes se consideran `notAdult` en los países regulados.|
|adult|3|El usuario debe ser tratado como un adulto.|

#### <a name="consentprovidedforminor-property"></a>Propiedad consentProvidedForMinor

| Valor    | #  |Descripción|
|:---------------|:--------|:----------|
|null|0|Valor predeterminado, ningún `consentProvidedForMinor` se ha establecido para el usuario.|
|granted|1|Se ha obtenido el consentimiento para que el usuario tenga una cuenta.|
|denied|2|No se ha obtenido el consentimiento para que el usuario tenga una cuenta.|
|notRequired|3|El usuario es de una ubicación que no requiere su consentimiento.|
 
## <a name="relationships"></a>Relaciones

| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|activities|Colección [userActivity](projectrome_activity.md)|Las actividades del usuario a través de dispositivos. Solo lectura. Admite valores NULL.|
|calendar|[Calendario](calendar.md)|El calendario principal del usuario. Solo lectura.|
|calendarGroups|Colección [calendarGroup](calendargroup.md)|Los grupos de calendario del usuario. Solo lectura. Admite valores NULL.|
|calendarView|Colección [event](event.md)|La vista Calendario del calendario. Solo lectura. Admite valores NULL.|
|calendars|Colección [calendar](calendar.md)|Los calendarios del usuario. Solo lectura. Admite valores NULL.|
|contactFolders|Colección [contactFolder](contactfolder.md)|Las carpetas de contactos del usuario. Solo lectura. Admite valores NULL.|
|contactos|Colección [contacts](contact.md)|Los contactos del usuario. Solo lectura. Admite valores NULL.|
|createdObjects|Colección [directoryObject](directoryobject.md)|Objetos de directorio creados por el usuario. Solo lectura. Admite valores NULL.|
|directReports|Colección [directoryObject](directoryobject.md)|Los usuarios y contactos que informan al usuario (los usuarios y contactos cuya propiedad manager está establecida para este usuario). Solo lectura. Admite valores NULL. |
|drive|[drive](drive.md)|OneDrive del usuario. Solo lectura.|
|drives|Colección [drive](drive.md)| Una colección de unidades disponibles para este usuario. Solo lectura. |
|events|Colección [event](event.md)|Los eventos del usuario. La opción predeterminada muestra eventos en el calendario predeterminado. Solo lectura. Admite valores NULL.|
|extensions|Colección [Extension](extension.md)|La colección de extensiones abiertas definidas para el usuario. Solo lectura. Admite valores NULL.|
|inferenceClassification | [inferenceClassification](inferenceClassification.md) | Clasificación de relevancia de los mensajes del usuario según las designaciones explícitas que invalidan una relevancia o importancia inferida. |
|licenseDetails|Colección [licenseDetails](licensedetails.md)|Una colección de detalles de la licencia de este usuario. Admite valores NULL.|
|mailFolders|Colección [MailFolder](mailfolder.md)| Las carpetas de correo del usuario. Solo lectura. Admite valores NULL.|
|manager|[directoryObject](directoryobject.md)|El usuario o el contacto que es administrador de este usuario. Solo lectura. (métodos HTTP: GET, PUT y DELETE).|
|memberOf|Colección [directoryObject](directoryobject.md)|Los grupos y los roles de directorio de los que el usuario es miembro. Solo lectura. Admite valores NULL.|
|messages|Colección [message](message.md)|Los mensajes en un buzón o una carpeta. Solo lectura. Admite valores NULL.|
|onenote|[Onenote](onenote.md)| Solo lectura.|
|outlook|[OutlookUser](outlookuser.md)| Solo lectura.|
|ownedDevices|Colección [directoryObject](directoryobject.md)|Dispositivos que son propiedad del usuario. Solo lectura. Admite valores NULL.|
|ownedObjects|Colección [directoryObject](directoryobject.md)|Objetos de directorio que son propiedad del usuario. Solo lectura. Admite valores NULL.|
|people|Colección [person](person.md)| Personas que son relevantes para el usuario. Solo lectura. Admite valores NULL.
|photo|[profilePhoto](profilephoto.md)| La foto de perfil del usuario. Solo lectura.|
|planner|[plannerUser](planneruser.md)| Punto de entrada para el recurso de Planner que un usuario puede tener. Solo lectura.|
|registeredDevices|Colección [directoryObject](directoryobject.md)|Dispositivos del usuario que están registrados. Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.directoryObject",
  "openType": true,
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
    "extensions",
    "joinedGroups",
    "mailFolders",
    "manager",
    "memberOf",
    "messages",
    "oauth2PermissionGrants",
    "onenote",
    "ownedDevices",
    "ownedObjects",
    "photo",
    "registeredDevices"
  ],
  "@odata.type": "microsoft.graph.user",
  "@odata.annotations": [
    {
      "capabilities": {
        "changeTracking": true
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
      "property": "calendarGroups",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "searchable": false
      }
    },
    {
      "property": "calendars",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "searchable": false
      }
    },
    {
      "property": "calendarView",
      "capabilities": {
        "changeTracking": true,
        "deletable": false,
        "expandable": true,
        "insertable": false,
        "navigability": "single",
        "searchable": false,
        "updatable": false
      }
    },
    {
      "property": "contactFolders",
      "capabilities": {
        "changeTracking": true,
        "expandable": false,
        "searchable": false
      }
    },
    {
      "property": "contacts",
      "capabilities": {
        "changeTracking": true,
        "expandable": false
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
      "property": "inferenceClassification",
      "capabilities": {
        "changeTracking": false,
        "deletable": false,
        "expandable": false,
        "insertable": false,
        "searchable": false
      }
    },
    {
      "property": "mailFolders",
      "capabilities": {
        "changeTracking": true,
        "expandable": false,
        "searchable": false
      }
    },
    {
      "property": "messages",
      "capabilities": {
        "changeTracking": false,
        "expandable": false
      }
    },
    {
      "property": "people",
      "capabilities": {
        "changeTracking": false,
        "deletable": false,
        "expandable": false,
        "insertable": false,
        "updatable": false
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
    }
  ]
}-->

```json
{
  "aboutMe": "string",
  "accountEnabled": true,
  "ageGroup": "string",
  "assignedLicenses": [{"@odata.type": "microsoft.graph.assignedLicense"}],
  "assignedPlans": [{"@odata.type": "microsoft.graph.assignedPlan"}],
  "birthday": "String (timestamp)",
  "businessPhones": ["string"],
  "city": "string",
  "companyName": "string",
  "consentProvidedForMinor": "string",
  "country": "string",
  "department": "string",
  "displayName": "string",
  "givenName": "string",
  "hireDate": "String (timestamp)",
  "id": "string (identifier)",
  "imAddresses": ["string"],
  "interests": ["string"],
  "jobTitle": "string",
  "legalAgeGroupClassification": "string",
  "mail": "string",
  "mailboxSettings": {"@odata.type": "microsoft.graph.mailboxSettings"},
  "mailNickname": "string",
  "mobilePhone": "string",
  "mySite": "string",
  "officeLocation": "string",
  "onPremisesDomainName": "string",
  "onPremisesExtensionAttributes": {"@odata.type": "microsoft.graph.onPremisesExtensionAttributes"},
  "onPremisesImmutableId": "string",
  "onPremisesLastSyncDateTime": "String (timestamp)",
  "onPremisesProvisioningErrors": [{"@odata.type": "microsoft.graph.onPremisesProvisioningError"}],
  "onPremisesSamAccountName": "string",
  "onPremisesSecurityIdentifier": "string",
  "onPremisesSyncEnabled": true,
  "onPremisesUserPrincipalName": "string",
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
  "drives": [ { "@odata.type": "microsoft.graph.drive" } ],
  "events": [ { "@odata.type": "microsoft.graph.event" } ],
  "inferenceClassification": { "@odata.type": "microsoft.graph.inferenceClassification" },
  "mailFolders": [ { "@odata.type": "microsoft.graph.mailFolder" } ],
  "manager": { "@odata.type": "microsoft.graph.directoryObject" },
  "memberOf": [ { "@odata.type": "microsoft.graph.directoryObject" } ],
  "messages": [ { "@odata.type": "microsoft.graph.message" } ],
  "outlook": { "@odata.type": "microsoft.graph.outlookUser" },
  "ownedDevices": [ { "@odata.type": "microsoft.graph.directoryObject" } ],
  "ownedObjects": [ { "@odata.type": "microsoft.graph.directoryObject" } ],
  "photo": { "@odata.type": "microsoft.graph.profilePhoto" },
  "registeredDevices": [ { "@odata.type": "microsoft.graph.directoryObject" } ]
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
  "description": "user resource",
  "keywords": "",
  "suppressions" : [
     "Warning: /api-reference/v1.0/resources/user.md/microsoft.graph.user:
      Property 'createdDateTime' found in markdown table but not in resource definition."
  ],
  "section": "documentation",
  "tocPath": ""
}-->
