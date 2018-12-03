---
title: tipo de recurso del usuario
description: Representa una cuenta de usuario de Azure AD. Se hereda de directoryObject.
ms.openlocfilehash: 893a5bef5fd3a2fce730c5f971ceca523e260be3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032131"
---
# <a name="user-resource-type"></a>tipo de recurso del usuario

Representa una cuenta de usuario de Azure AD. Se hereda de [directoryObject](directoryobject.md).

Este recurso admite:

- Adición de sus propios datos a las propiedades personalizadas como [extensiones](/graph/extensibility-overview).
- Suscribirse a [las notificaciones de cambios](/graph/webhooks).
- que use una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/user-delta.md).

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Enumerar usuarios](../api/user-list.md) |Colección [user](user.md)| Obtiene una lista de objetos de usuario.|
|[Crear usuario](../api/user-post-users.md) |[user](user.md)| Crea un objeto de usuario nuevo.|
|[Obtener usuario](../api/user-get.md) | [usuario](user.md) |Lee las propiedades y las relaciones del objeto de usuario.|
|[Actualizar usuario](../api/user-update.md) | [usuario](user.md) |Actualiza el objeto de usuario. |
|[Eliminar usuario](../api/user-delete.md) | Ninguno |Elimina el objeto de usuario. |
|[Enumerar mensajes](../api/user-list-messages.md) |Colección [message](message.md)| Obtiene todos los mensajes del buzón del usuario que inició sesión.|
|[Crear mensaje](../api/user-post-messages.md) |[Mensaje](message.md)| Crea un nuevo mensaje publicándolo en la colección de mensajes.|
|[Enumerar mailFolders](../api/user-list-mailfolders.md) |Colección [mailFolder](mailfolder.md)| Obtiene la colección de carpetas de correo en la carpeta raíz del usuario que inició sesión. |
|[Crear mailFolder](../api/user-post-mailfolders.md) |[MailFolder](mailfolder.md)| Crea un nuevo mailFolder publicándolo en la colección mailFolders.|
|[sendMail](../api/user-sendmail.md)|Ninguno|Envía el mensaje especificado en el cuerpo de la solicitud.|
|[Enumerar eventos](../api/user-list-events.md) |Colección [event](event.md)| Obtiene una lista de los objetos de evento del buzón del usuario. La lista contiene patrones de serie y reuniones de instancia única.|
|[Crear evento](../api/user-post-events.md) |[Evento](event.md)| Crea un nuevo evento publicándolo en la colección de eventos.|
|[Enumerar calendarios](../api/user-list-calendars.md) |Colección [calendar](calendar.md)| Obtiene una colección de objetos de calendario.|
|[Crear calendario](../api/user-post-calendars.md) |[Calendario](calendar.md)| Crea un nuevo calendario publicándolo en la colección de calendarios.|
|[Enumerar calendarGroups](../api/user-list-calendargroups.md) |Colección [calendarGroup](calendargroup.md)| Obtiene una colección de objetos calendarGroup.|
|[Crear calendarGroup](../api/user-post-calendargroups.md) |[CalendarGroup](calendargroup.md)| Crea un nuevo calendarGroup publicándolo en la colección calendarGroups.|
|[Enumerar calendarView](../api/user-list-calendarview.md) |Colección [event](event.md)| Obtiene una colección de objetos de evento.|
|[Enumerar contactos](../api/user-list-contacts.md) |Colección [contacts](contact.md)| Obtiene una colección de contactos de la carpeta de contactos predeterminada del usuario que inició sesión.|
|[Crear contacto](../api/user-post-contacts.md) |[Contacto](contact.md)| Crea un nuevo contacto publicándolo en la colección de contactos.|
|[Enumerar contactFolders](../api/user-list-contactfolders.md) |Colección [contactFolder](contactfolder.md)| Obtiene la colección de carpetas de contactos de la carpeta de contactos predeterminada del usuario que inició sesión.|
|[Crear ContactFolder](../api/user-post-contactfolders.md) |[ContactFolder](contactfolder.md)| Crea un nuevo contactFolder publicándolo en la colección contactFolders.|
|[Enumerar directReports](../api/user-list-directreports.md) |Colección [directoryObject](directoryobject.md)| Obtiene los usuarios y contactos que informan al usuario desde la propiedad de navegación directReports.|
|[Enumerar administrador](../api/user-list-manager.md) |[directoryObject](directoryobject.md) | Obtiene el usuario o el contacto que es administrador de este usuario desde la propiedad de navegación manager.|
|[Enumerar memberOf](../api/user-list-memberof.md) |Colección [directoryObject](directoryobject.md)| Obtiene los grupos y los roles de directorio de los que el usuario es miembro directo desde la propiedad de navegación memberOf.|
|[Enumerar ownedDevices](../api/user-list-owneddevices.md) |Colección [directoryObject](directoryobject.md)| Obtiene los dispositivos que son propiedad del usuario desde la propiedad de navegación ownedDevices.|
|[Enumerar ownedObjects](../api/user-list-ownedobjects.md) |Colección [directoryObject](directoryobject.md)| Obtiene los objetos de directorio que son propiedad del usuario desde la propiedad de navegación ownedObjects.|
|[Enumerar registeredDevices](../api/user-list-registereddevices.md) |Colección [directoryObject](directoryobject.md)| Obtiene los dispositivos registrados del usuario desde la propiedad de navegación registeredDevices.|
|[Enumerar createdObjects](../api/user-list-createdobjects.md) |Colección [directoryObject](directoryobject.md)| Obtiene los objetos de directorio creados por el usuario desde la propiedad de navegación createdObjects.|
|[assignLicense](../api/user-assignlicense.md)|[user](user.md)|Agrega o quita suscripciones del usuario. También puede habilitar y deshabilitar los planes específicos asociados a una suscripción.|
|[Enumerar licenseDetails](../api/user-list-licensedetails.md) |Colección [licenseDetails](licensedetails.md)| Obtenga una colección de objetos licenseDetails.|
|[checkMemberGroups](../api/user-checkmembergroups.md)|Colección string|Comprueba la pertenencia a una lista de grupos. La comprobación es transitiva.|
|[getMemberGroups](../api/user-getmembergroups.md)|Colección string|Devuelve todos los grupos de los que el usuario es miembro. La comprobación es transitiva.|
|[getMemberObjects](../api/user-getmemberobjects.md)|Colección string| Devuelve todos los grupos y los roles de directorio de los que el usuario es miembro. La comprobación es transitiva. |
|[reminderView](../api/user-reminderview.md)|Colección [reminder](reminder.md)|Devuelve una lista de los avisos de calendario entre las horas de inicio y finalización especificadas.|
|[delta](../api/user-delta.md)|Colección user| Obtener los cambios incrementales de usuarios. |
|**Extensiones abiertas**| | |
|[Crear extensión abierta](../api/opentypeextension-post-opentypeextension.md) |[openTypeExtension](opentypeextension.md)| Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o un recurso existente.|
|[Obtener extensión abierta](../api/opentypeextension-get.md) |Colección [openTypeExtension](opentypeextension.md)| Obtiene una extensión abierta identificada por el nombre de extensión.|
|**Extensiones de esquema**| | |
|[Agregar valores de extensión de esquema](/graph/extensibility-schema-groups) || Cree una definición de extensión de esquema y, después, úsela para agregar datos escritos personalizados a un recurso.|

## <a name="properties"></a>Propiedades

| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|aboutMe|String|Un campo de entrada de texto de forma libre para que el usuario se describa a sí mismo.|
|accountEnabled|Booleano| **true** si la cuenta está habilitada; en caso contrario, **false**. Esta propiedad es necesaria cuando se crea un usuario. Es compatible con $filter.    |
|ageGroup|String|Establece el grupo de edad del usuario. Valores permitidos: `null`, `minor`, `notAdult` y `adult`. Hacer referencia a las [definiciones de propiedades de grupo de edad legal](#legal-age-group-property-definitions) para obtener más información. |
|assignedLicenses|Colección [assignedLicense](assignedlicense.md)|Las licencias asignadas al usuario. No admite valores NULL.            |
|assignedPlans|Colección [assignedPlan](assignedplan.md)|Los planes asignados al usuario. Solo lectura. No admite valores NULL. |
|birthday|DateTimeOffset|El cumpleaños del usuario. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|businessPhones|Colección string|Los números de teléfono del usuario. NOTA: Aunque se trata de una colección de cadenas, solo se puede establecer un número para esta propiedad.|
|city|String|La ciudad en la que se encuentra el usuario. Es compatible con $filter.|
|companyName | String | El nombre de la compañía a la que está asociado el usuario. Solo lectura. |
|consentProvidedForMinor|String|Establece si se ha obtenido el consentimiento para menores. Valores permitidos: `null`, `granted`, `denied` y `notRequired`. Hacer referencia a las [definiciones de propiedades de grupo de edad legal](#legal-age-group-property-definitions) para obtener más información.|
|country|String|El país o la región en la que se encuentra el usuario. Por ejemplo: "US" o "UK". Es compatible con $filter.|
|createdDateTime | DateTimeOffset |La fecha de creación del objeto de usuario. |
|department|String|El nombre del departamento en el que trabaja el usuario. Es compatible con $filter.|
|displayName|String|El nombre del usuario que aparece en la libreta de direcciones. Suele ser la combinación del nombre del usuario, la inicial del segundo nombre y el apellido. Esta propiedad es necesaria cuando se crea un usuario y no se puede borrar durante las actualizaciones. Es compatible con $filter y $orderby.|
|givenName|String|El nombre (nombre de pila) del usuario. Es compatible con $filter.|
|hireDate|DateTimeOffset|La fecha de contratación del usuario. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|id|String|El identificador único del usuario. Heredado de [directoryObject](directoryobject.md). Clave. No admite valores NULL. Solo lectura.|
|imAddresses|Colección string|Direcciones del protocolo de inicio de sesión (SIP) de voz sobre IP (VOIP) del servicio de mensajería instantánea correspondientes al usuario. Solo lectura.|
|interests|Colección string|Una lista para que el usuario describa sus intereses.|
|jobTitle|String|El puesto del usuario. Es compatible con $filter.|
|legalAgeGroupClassification|String| Se usa en las aplicaciones empresariales para determinar el grupo de edad legal del usuario. Esta propiedad es de sólo lectura y calculadas en función de `ageGroup` y `consentProvidedForMinor` propiedades. Valores permitidos: `null`, `minorWithOutParentalConsent`, `minorWithParentalConsent`, `minorNoParentalConsentRequired`, `notAdult` y `adult`. Hacer referencia a las [definiciones de propiedades de grupo de edad legal](#legal-age-group-property-definitions) para obtener más información.)|
|mail|String|La dirección SMTP del usuario, por ejemplo: "jeff@contoso.onmicrosoft.com". Solo lectura. Es compatible con $filter.|
|mailboxSettings|[mailboxSettings](mailboxsettings.md)|Configuración del buzón principal del usuario que ha iniciado sesión. Puede [obtener](../api/user-get-mailboxsettings.md) o [actualizar](../api/user-update-mailboxsettings.md) las opciones para enviar respuestas automáticas a mensajes entrantes, de configuración regional y de zona horaria.|
|mailNickname|String|El alias de correo del usuario. Esta propiedad debe especificarse al crear un usuario. Es compatible con $filter.|
|mobilePhone|String|El número de teléfono móvil principal del usuario.|
|mySite|String|La dirección URL del sitio personal del usuario.|
|officeLocation|String|La ubicación de la oficina del lugar de trabajo del usuario.|
|onPremisesDomainName|String| Contiene el local `domainFQDN`, también se denomina NombreDominioDns sincronizado desde el directorio local. La propiedad sólo se rellena para los clientes que se sincronizan su directorio local para Azure Active Directory a través de Azure Connect de AD. Solo lectura. |
|onPremisesExtensionAttributes|[OnPremisesExtensionAttributes](onpremisesextensionattributes.md)|Contiene extensionAttributes 1-15 para el usuario. Tenga en cuenta que los atributos de extensión individuales son ni seleccionable ni que se pueden filtrar. Para un `onPremisesSyncEnabled` usuario, este conjunto de propiedades es mastered local y es de sólo lectura. Para un usuario solo en la nube (donde `onPremisesSyncEnabled` es false), estas propiedades se pueden establecer durante la creación o actualizar. |
|onPremisesImmutableId|String|Esta propiedad se usa para asociar una cuenta de usuario de Active Directory local a su objeto de usuario de Azure AD. Esta propiedad se debe especificar al crear una nueva cuenta de usuario en el gráfico si utiliza un dominio federado para la propiedad de **userPrincipalName** (UPN) del usuario. **Importante:** El **$** y **\_** caracteres no se puede usar cuando se especifica esta propiedad. Es compatible con $filter.                            |
|onPremisesLastSyncDateTime|DateTimeOffset|Indica la última vez que se ha sincronizado el objeto con el directorio local. Por ejemplo: "2013-02-16T03:04:54Z". El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.|
|onPremisesProvisioningErrors|colección de [onPremisesProvisioningError](onpremisesprovisioningerror.md)| Errores al usar el producto de sincronización de Microsoft durante el aprovisionamiento. |
|onPremisesSamAccountName|String| Contiene el local `samAccountName` sincronizado desde el directorio local. La propiedad sólo se rellena para los clientes que se sincronizan su directorio local para Azure Active Directory a través de Azure Connect de AD. Solo lectura. |
|onPremisesSecurityIdentifier|String|Contiene el identificador de seguridad local (SID) del usuario que se sincroniza desde un recurso local a la nube. Solo lectura.|
|onPremisesSyncEnabled|Booleano| **true** si este objeto está sincronizado desde un directorio local; **false** si este objeto se ha sincronizado originalmente desde un directorio local, pero ya no está sincronizado; **null** si este objeto no se ha sincronizado nunca desde un directorio local (valor predeterminado). Solo lectura |
|onPremisesUserPrincipalName|String| Contiene el local `userPrincipalName` sincronizado desde el directorio local. La propiedad sólo se rellena para los clientes que se sincronizan su directorio local para Azure Active Directory a través de Azure Connect de AD. Solo lectura. |
|passwordPolicies|String|Especifica las directivas de contraseña del usuario. Este valor es una enumeración con un valor posible de "DisableStrongPassword" y permite especificar contraseñas menos seguras que la directiva predeterminada. También se puede especificar "DisablePasswordExpiration". Los dos se pueden especificar a la vez. Por ejemplo: "DisablePasswordExpiration, DisableStrongPassword".|
|passwordProfile|[PasswordProfile](passwordprofile.md)|Especifica el perfil de contraseña del usuario. El perfil contiene la contraseña del usuario. Esta propiedad es necesaria cuando se crea un usuario. La contraseña del perfil debe cumplir los requisitos mínimos especificados por la propiedad **passwordPolicies**. De manera predeterminada, se requiere una contraseña segura.|
|pastProjects|Colección string|Una lista para que el usuario enumere sus últimos proyectos.|
|postalCode|String|El código postal de la dirección del usuario. El código postal es específico del país o de la región del usuario. En Estados Unidos, este atributo contiene el código postal.|
|preferredDataLocation|String|La ubicación de datos preferido para el usuario. Para obtener más información, vea [OneDrive en línea Multi-ubican](https://docs.microsoft.com/sharepoint/dev/solution-guidance/multigeo-introduction).|
|preferredLanguage|String|El idioma preferido del usuario. Debe seguir el código ISO 639-1. Por ejemplo, "en-US".|
|preferredName|String|El nombre preferido del usuario.|
|provisionedPlans|Colección [ProvisionedPlan](provisionedplan.md)|Los planes que se ha aprovisionado para el usuario. Solo lectura. No admite valores NULL. |
|proxyAddresses|Colección string|Por ejemplo: `["SMTP: bob@contoso.com", "smtp: bob@sales.contoso.com"]` El operador **any** es necesario para las expresiones de filtro en las propiedades de varios valores. Solo lectura, no admite valores NULL. Es compatible con $filter.          |
|responsibilities|Colección string|Una lista para que el usuario enumere sus responsabilidades.|
|schools|Colección string|Una lista para que el usuario enumere las escuelas a las que ha ido.|
|skills|Colección string|Una lista para que el usuario enumere sus aptitudes.|
|state|String|El estado o la provincia de la dirección del usuario. Es compatible con $filter.|
|streetAddress|String|La dirección postal del lugar de trabajo del usuario.|
|surname|String|El apellido (o apellidos) del usuario. Es compatible con $filter.|
|usageLocation|String|Un código de país de dos letras (norma ISO 3166). Es necesario para los usuarios a los que se asignarán licencias debido a un requisito legal para comprobar la disponibilidad de los servicios en los países.  Algunos ejemplos son: "US", "JP" y "GB". No admite valores NULL. Es compatible con $filter.|
|userPrincipalName|String|El nombre principal del usuario (UPN) del usuario. El UPN es un nombre de inicio de sesión de Internet del usuario basado en la norma RFC 822. Por convención, se debe asignar al nombre de correo electrónico del usuario. El formato general es alias@dominio, donde el dominio debe estar presente en la colección de dominios verificados del inquilino. Esta propiedad es necesaria cuando se crea un usuario. Se puede acceder a los dominios verificados del inquilino desde la propiedad **verifiedDomains** en [organización](organization.md). Es compatible con $filter y $orderby.
|userType|String|Un valor de cadena que puede utilizarse para clasificar los tipos de usuario en el directorio. Por ejemplo: "Miembro" e "Invitado". Es compatible con $filter.          |

### <a name="legal-age-group-property-definitions"></a>Definiciones de propiedades de grupo de edad legal

En esta sección se explica cómo las tres propiedades del grupo de edad (`legalAgeGroupClassification`, `ageGroup` y `consentProvidedForMinor`) usadas por los administradores de Azure AD y los desarrolladores de aplicaciones de empresa para cumplir las reglamentaciones relacionadas con la edad.

Por ejemplo: Cameron es administrador de un directorio para una escuela de primaria en Holyport en el Reino Unido. Al principio del año escolar utiliza la documentación de admisión para obtener consentimiento de los padres del menor según las reglamentaciones relacionadas con la antigüedad del Reino Unido. El consentimiento obtenido en el elemento primario permite que la cuenta del menor que va a usar Holyport school y aplicaciones de Microsoft. A continuación, Cameron crea todas las cuentas y establece ageGroup a "secundarias" y consentProvidedForMinor a "concedido". Aplicaciones utilizadas por sus estudiantes, a continuación, son capaces de suprimir las características que no son adecuadas para menores.

#### <a name="legal-age-group-classification"></a>Clasificación de grupo de edad legal

Esta propiedad de solo lectura se usa en los desarrolladores de aplicaciones de empresa para garantizar el control correcto de un usuario en función de su grupo de edad legal. Se calcula en función del usuario `ageGroup` y `consentProvidedForMinor` propiedades.

| Valor    | #  |Descripción|
|:---------------|:--------|:----------|
|nulo|0|Valor predeterminado que no `ageGroup` se ha establecido para el usuario.|
|minorWithoutParentalConsent |1|(Reservado para uso futuro)|
|minorWithParentalConsent|2| El usuario se considera a un secundarias según las reglamentaciones relacionadas con la edad de su país o región y el Administrador de la cuenta ha obtenido apropiado consentimiento de un elemento primario o guardián.|
|contenido para adultos|3|El usuario considera un contenido para adultos según las reglamentaciones relacionadas con la edad de su país o región.|
|notAdult|4|El usuario es de un país o región que tiene regulaciones adicionales relacionados con la edad (por ejemplo, Estados Unidos, Reino Unido, Unión Europea o Corea del sur) y la edad del usuario se encuentra entre una secundaria y una vigencia para adultos (como país en función de estipulado o región). Por lo general, esto significa que se consideran adolescentes como `notAdult` en países regulados.|
|minorNoParentalConsentRequired|5|El usuario es un menor, pero es de un país o región que no tiene ningún reglamentaciones relacionadas con la edad.|

#### <a name="age-group-and-minor-consent"></a>Grupo de edad y consentimiento secundaria

Las propiedades de consentimiento del menor y grupo de edad son propiedades opcionales usadas por los administradores de Azure AD para ayudar a garantizar que el uso de una cuenta se controla correctamente según las reglas de las normativas relacionadas con la edad que rigen el usuario país o región.

#### <a name="agegroup-property"></a>ageGroup (propiedad)

| Valor    | #  |Descripción|
|:---------------|:--------|:----------|
|nulo|0|Valor predeterminado que no `ageGroup` se ha establecido para el usuario.|
|secundaria|1|El usuario se considere un secundarias.|
|notAdult|2|El usuario es de un país que tiene observancia normativas de Estados Unidos, Reino Unido, Unión Europea o Corea del sur) y edad del usuario es mucho más que el límite superior de edad kid (según país) y límite inferior menor de edad para adultos (como país en función de estipulado o región) . Básicamente, se consideran adolescentes como `notAdult` en países regulados.|
|contenido para adultos|3|El usuario debe ser tratados como un contenido para adultos.|

#### <a name="consentprovidedforminor-property"></a>consentProvidedForMinor (propiedad)

| Valor    | #  |Descripción|
|:---------------|:--------|:----------|
|nulo|0|Valor predeterminado que no `consentProvidedForMinor` se ha establecido para el usuario.|
|concedido|1|Se ha obtenido el consentimiento para que el usuario tenga una cuenta.|
|denegado|2|No se ha obtenido el consentimiento para que el usuario tenga una cuenta.|
|notRequired|3|El usuario es desde una ubicación que no requiera su consentimiento.|
 
## <a name="relationships"></a>Relaciones

| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|activities|colección de [userActivity](projectrome-activity.md)|Las actividades del usuario a través de dispositivos. Solo lectura. Admite valores NULL.|
|calendar|[Calendar](calendar.md)|El calendario principal del usuario. Solo lectura.|
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
|inferenceClassification | [inferenceClassification](inferenceclassification.md) | Clasificación de relevancia de los mensajes del usuario según las designaciones explícitas que invalidan una relevancia o importancia inferida. |
|licenseDetails|Colección de [LicenseDetails](licensedetails.md)|Una colección de detalles de la licencia de este usuario. Admite valores NULL.|
|mailFolders|Colección [MailFolder](mailfolder.md)| Las carpetas de correo del usuario. Solo lectura. Admite valores NULL.|
|manager|[directoryObject](directoryobject.md)|El usuario o el contacto que es administrador de este usuario. Solo lectura. (métodos HTTP: GET, PUT y DELETE).|
|memberOf|Colección [directoryObject](directoryobject.md)|Los grupos y los roles de directorio de los que el usuario es miembro. Solo lectura. Admite valores NULL.|
|messages|Colección [message](message.md)|Los mensajes en un buzón o una carpeta. Solo lectura. Admite valores NULL.|
|onenote|[OneNote](onenote.md)| Solo lectura.|
|Outlook|[OutlookUser](outlookuser.md)| Solo lectura.|
|ownedDevices|Colección [directoryObject](directoryobject.md)|Dispositivos que son propiedad del usuario. Solo lectura. Admite valores NULL.|
|ownedObjects|Colección [directoryObject](directoryobject.md)|Objetos de directorio que son propiedad del usuario. Solo lectura. Admite valores NULL.|
|personas|colección de [persona](person.md)| Personas que son relevantes para el usuario. Solo lectura. Admite valores NULL.
|photo|[profilePhoto](profilephoto.md)| La foto de perfil del usuario. Solo lectura.|
|planner|[plannerUser](planneruser.md)| Punto de entrada para el recurso de organizador que pudiera existir para un usuario. Solo lectura.|
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
  "preferredDataLocation": "string",
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

- [Agregar datos personalizados a los recursos mediante extensiones](/graph/extensibility-overview)
- [Agregar datos personalizados a los usuarios mediante extensiones abiertas](/graph/extensibility-open-users)
- [Agregar datos personalizados a los grupos mediante extensiones de esquema](/graph/extensibility-schema-groups)

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
