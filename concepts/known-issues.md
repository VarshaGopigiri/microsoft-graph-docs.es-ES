---
title: Problemas conocidos de Microsoft Graph
description: En este artículo, se describen los problemas conocidos de Microsoft Graph. Para obtener información sobre las actualizaciones más recientes, consulte el Registro de cambios de Microsoft Graph.
author: jthake-msft
localization_priority: Priority
ms.openlocfilehash: 65a38e8852c878811d609b56b0f7f0ad1d4e73ff
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820226"
---
# <a name="known-issues-with-microsoft-graph"></a>Problemas conocidos de Microsoft Graph

En este artículo, se describen los problemas conocidos de Microsoft Graph. Para obtener información sobre las actualizaciones más recientes, consulte el [Registro de cambios de Microsoft Graph](changelog.md).

## <a name="users"></a>Usuarios

### <a name="no-instant-access-after-creation"></a>No hay acceso instantáneo después de la creación

Los usuarios pueden crearse inmediatamente a través de un POST en la entidad del usuario. Una licencia de Office 365 primero se debe asignar a un usuario, con el fin de obtener acceso a los servicios de Office 365. Incluso entonces, debido a la naturaleza distribuida del servicio, puede llevar 15 minutos que los archivos, mensajes y entidades de eventos estén disponibles para su uso para este usuario, a través de la API de Microsoft Graph. Durante este tiempo, las aplicaciones recibirán una respuesta de error HTTP 404.

### <a name="photo-restrictions"></a>Restricciones de la foto

Leer y actualizar la foto de perfil de un usuario solo es posible si el usuario tiene un buzón. Además, cualquier foto que *pueda* haberse almacenado previamente mediante la propiedad **thumbnailPhoto** (usando la vista previa de la API unificada de Office 365 o Azure AD Graph, o bien mediante la sincronización de AD Connect) ya no será accesible mediante la propiedad **photo** del recurso [user](/graph/api/resources/user?view=graph-rest-1.0). En este caso, no poder leer o actualizar una foto provocaría el error siguiente:

```javascript
    {
      "error": {
        "code": "ErrorNonExistentMailbox",
        "message": "The SMTP address has no mailbox associated with it."
      }
    }
```

### <a name="using-delta-query"></a>Usar la consulta de delta

Para ver los problemas conocidos al usar la consulta de delta, vea la [sección Consulta de delta](#delta-query) de este artículo.

## <a name="microsoft-teams"></a>Microsoft Teams

### <a name="create-chat-thread-api"></a>Crear una API de conversación de chat

La API actual para [crear una conversación de chat](/graph/api/channel-post-chatthreads?view=graph-rest-beta) se reemplazará con una API más compleja y coherente con el esquema de [lista de mensajes del canal](/graph/api/channel-list-messages?view=graph-rest-beta).

### <a name="graph-explorer-and-global-admins"></a>El Explorador de Graph y los administradores globales

Actualmente, el Probador de Graph permite que los administradores globales manipulen equipos de los que no son propietarios o miembros, pero con otras aplicaciones que intentan realizar las mismas llamadas API se producirán un error si el usuario actual no es un miembro o el propietario del equipo.

### <a name="get-teams-and-post-teams-are-not-supported"></a>GET /teams y POST /teams no son compatibles

Vea [lista de todos los equipos](teams-list-all-teams.md) y [lista de sus equipos](/graph/api/user-list-joinedteams?view=graph-rest-1.0) para obtener una lista de equipos.
Vea [crear equipo](/graph/api/team-put-teams?view=graph-rest-1.0) para crear equipos.

### <a name="missing-teams-in-list-all-teams"></a>Faltan equipos en la lista de todos los equipos

Algunos equipos que se crearon en el pasado pero que no se han usado recientemente por un usuario de Microsoft Teams no se encuentran en la [lista de todos los equipos](teams-list-all-teams.md). 
Se mostrarán los nuevos equipos.
Algunos equipos antiguos no tienen una propiedad **resourceProvisioningOptions** que contiene "Equipo", porque está configurada para equipos recién creados y equipos que se han visitado en Microsoft Teams.
En el futuro, configuraremos **resourceProvisioningOptions** para los equipos existentes que no se han abierto en Microsoft Teams.

## <a name="groups"></a>Grupos

### <a name="permissions-for-groups-and-microsoft-teams"></a>Permisos para grupos y Microsoft Teams

Microsoft Graph expone dos permisos ([*Group.Read.All*](permissions-reference.md#group-permissions) y [*Group.ReadWrite.All*](permissions-reference.md#group-permissions)) para obtener acceso a las API de grupos y Microsoft Teams.
Estos permisos deben ser admitidos por el administrador.
En el futuro, planeamos agregar nuevos permisos para grupos y equipos que puedan ser admitidos por los usuarios.

Además, solo la API para la administración y gestión del grupo principal admite el acceso con permisos delegados o solo de aplicación. El resto de características de la API de grupo solo admiten permisos delegados.

Ejemplos de funciones de grupo que admiten permisos delegados y de aplicación:

* Crear y eliminar grupos
* Obtener y actualizar las propiedades de grupos relativas a la administración de grupos.
* Grupo [configuración del directorio](/graph/api/resources/directoryobject?view=graph-rest-1.0), tipo y sincronización
* Propietarios de grupo y pertenencia

Ejemplos de funciones de grupo que admiten solo permisos delegados:

* Conversaciones, eventos y fotos de grupo
* Remitentes externos, remitentes aceptados o rechazados, suscripciones a grupos
* Favoritos del usuario y conteo no visto 

### <a name="policy"></a>Directiva

Usar Microsoft Graph para crear y nombrar un grupo de Office 365 omite cualquier directiva de grupo de Office 365 que esté configurada a través de Outlook Web App.

### <a name="adding-and-getting-attachments-of-group-posts"></a>Agregar y obtener datos adjuntos de las publicaciones de grupo

Actualmente, al [agregar](/graph/api/post-post-attachments?view=graph-rest-1.0) datos adjuntos a las publicaciones de grupo, así como al [enumerar](/graph/api/post-list-attachments?view=graph-rest-1.0) y obtener los datos adjuntos de las publicaciones de grupo, se devuelve el mensaje de error "La solicitud de OData no es compatible". Se ha desarrollado una corrección tanto para la versión `/v1.0` como para la `/beta` y se espera que esté disponible a finales de enero de 2016.

### <a name="setting-the-allowexternalsenders-property"></a>Establecer la propiedad allowExternalSenders

Existe en la actualidad un problema que evita el establecimiento de la propiedad **allowExternalSenders** de un grupo en operaciones POST o PATCH, en `/v1.0` y `/beta`.

### <a name="using-delta-query"></a>Usar la consulta de delta

Para ver los problemas conocidos al usar la consulta de delta, vea la [sección Consulta de delta](#delta-query) de este artículo.

## <a name="bookings"></a>Bookings

### <a name="errorexceededfindcountlimit-when-querying-bookingbusinesses"></a>ErrorExceededFindCountLimit al consultar bookingBusinesses

La obtención de la lista de `bookingBusinesses` genera el siguiente código de error si una organización tiene varias empresas de Bookings y la cuenta que realiza la solicitud no es de administrador:

```json
{
  "error": {
    "code": "ErrorExceededFindCountLimit",
    "message":
      "The GetBookingMailboxes request returned too many results. Please specify a query to limit the results.",
  }
}
```

Como solución alternativa, puede limitar el conjunto de empresas devuelto por la solicitud mediante la inclusión de un parámetro `query`, por ejemplo:

```
GET https://graph.microsoft.com/beta/bookingBusinesses?query=Fabrikam
```


## <a name="calendars"></a>Calendarios

### <a name="accessing-a-shared-calendar"></a>Acceso a calendarios compartidos

Al intentar tener acceso a los eventos de un calendario que se ha compartido por otro usuario mediante la siguiente operación:

```http
GET \users('{id}')\calendars('{id}')\events
```

Puede obtener HTTP 500 con el código de error `ErrorInternalServerTransientError`. El error se produce porque:

- Tradicionalmente existen dos maneras de implementar el uso compartido del calendario, que, con fines de diferenciación, se les hace referencia como el enfoque "antiguo" y el enfoque "nuevo".
- El enfoque nuevo está disponible en estos momentos para los calendarios de uso compartido con permisos de vista o edición, pero no con permisos delegados.
- Puede usar la API de REST de calendario para ver o editar los calendarios compartidos, solo si los calendarios se han compartido según el enfoque **nuevo**.
- No puede usar la API de REST de calendario para ver o editar dichos calendarios (o sus eventos) si los calendarios se han compartido según el enfoque **antiguo**.


Si un calendario se ha compartido con permisos de vista o edición pero con el enfoque antiguo, ahora puede trabajar en el error y actualizar manualmente el calendario de uso compartido para que use el enfoque nuevo.
Con el tiempo, Outlook actualizará automáticamente todos los calendarios compartidos para que usen el nuevo enfoque, incluidos los calendarios compartidos con permisos de delegado.

Para actualizar manualmente un calendario compartido para que use el enfoque nuevo, siga estos pasos:
1.  El destinatario quita el calendario que se ha compartido anteriormente con ellos.
2.  El propietario del calendario vuelve a compartirlo en Outlook en la web, Outlook en iOS o Outlook en Android.
3.  El destinatario vuelve a aceptar el calendario compartido con Outlook en la web. (Será posible usar otros clientes de Outlook pronto).
4.  El destinatario comprueba que el calendario se ha vuelto a compartir correctamente con el nuevo enfoque al ver el calendario compartido en Outlook en iOS o en Outlook en Android.

Un calendario compartido con usted mediante el nuevo enfoque aparece como cualquier otro calendario de su buzón. Puede usar la API de REST de calendario para ver o editar eventos en el calendario compartido, como si fuera su propio calendario. Por ejemplo:

```http
GET \me\calendars('{id}')\events
```

### <a name="adding-and-accessing-ics-based-calendars-in-users-mailbox"></a>Agregar y acceder a calendarios basados en archivos ICS en el buzón del usuario

Actualmente, existe una compatibilidad parcial con un calendario basado en una suscripción a calendarios de Internet (ICS):

* Puede agregar un calendario basado en ICS a un buzón de usuario mediante la interfaz de usuario, pero no mediante la API de Microsoft Graph.
* [Enumerar los calendarios del usuario](/graph/api/user-list-calendars?view=graph-rest-1.0) le permite obtener las propiedades **name**, **color** e **id** de cada [calendario](/graph/api/resources/calendar?view=graph-rest-1.0) en el grupo de calendarios predeterminado del usuario, o en un grupo de calendarios especificado, incluidos los calendarios basados en ICS. No puede almacenar ni acceder a la dirección URL de una ICS en el recurso del calendario.
* También puede [enumerar los eventos](/graph/api/calendar-list-events?view=graph-rest-1.0) de un calendario basado en ICS.

### <a name="onlinemeetingurl-property-support-for-microsoft-teams"></a>Compatibilidad con la propiedad onlineMeetingUrl de Microsoft Teams

Actualmente, la propiedad **onlineMeetingUrl** de un [evento](/graph/api/resources/event?view=graph-rest-1.0) de una reunión de Skype indicaría la dirección URL de la reunión en línea. Pero esa propiedad para un evento de reunión de Microsoft Teams se establece a null.

## <a name="calls-and-online-meetings"></a>Llamadas y reuniones en línea

> **Nota:** Actualmente, las llamadas y las reuniones en línea están en versión preliminar y solo se encuentran disponibles en el punto de conexión de la versión beta de Microsoft Graph.

- La ruta de navegación `/applications/{id}` no es compatible. No está permitido navegar mediante el nodo de aplicaciones globales a la aplicación, incluso la suya. Use solo la navegación `/app`.

## <a name="contacts"></a>Contactos

### <a name="organization-contacts-available-in-only-beta"></a>Contactos de organización disponibles solo en beta

Solo los contactos personales son compatibles actualmente. Actualmente no se admiten contactos de la organización en `/v1.0`, pero pueden encontrarse en `/beta`.

### <a name="default-contacts-folder"></a>Carpeta de contactos predeterminada

En la versión `/v1.0`, `GET /me/contactFolders` no incluye la carpeta de contactos predeterminada del usuario.

Estará disponible una corrección. Mientras tanto, puede usar la siguiente consulta [enumerar contactos](/graph/api/user-list-contacts?view=graph-rest-1.0) y la propiedad **parentFolderId** como una solución alternativa para obtener el identificador de la carpeta de contactos predeterminada:

```http
GET https://graph.microsoft.com/v1.0/me/contacts?$top=1&$select=parentFolderId
```

En la consulta anterior:

1. `/me/contacts?$top=1` obtiene las propiedades de un elemento [contact](/graph/api/resources/contact?view=graph-rest-1.0) de la carpeta de contactos predeterminada.
2. Al anexar `&$select=parentFolderId` se devuelve solo la propiedad **parentFolderId** del contacto, que es el identificador de la carpeta de contactos predeterminada.


### <a name="accessing-contacts-via-a-contact-folder-in-beta"></a>Acceder a contactos a través de una carpeta de contactos en la versión beta

En la versión `/beta`, existe un problema en la actualidad que impide acceder a un [contacto](/graph/api/resources/contact?view=graph-rest-beta) especificando su carpeta primaria en la dirección de solicitud REST, tal y como se muestra en los dos escenarios siguientes.

* Acceso a un contacto desde un [contactFolder](/graph/api/resources/contactfolder?view=graph-rest-beta) de nivel superior del usuario.

```http
GET /me/contactfolders/{id}/contacts/{id}
GET /users/{id | userPrincipalName}/contactfolders/{id}/contacts/{id}
```

* Acceso a un contacto contenido en una carpeta secundaria de una **contactFolder**.  En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.

```http
GET /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
GET /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```

Como alternativa, puede simplemente [obtener](/graph/api/contact-get?view=graph-rest-beta) el contacto especificando su identificador, tal como se muestra a continuación, ya que GET/contacts en la versión `/beta` se aplica a todos los contactos del buzón de correo del usuario:

```http
GET /me/contacts/{id}
GET /users/{id | userPrincipalName}/contacts/{id}
```

## <a name="messages"></a>Mensajes

### <a name="the-comment-parameter-for-creating-a-draft"></a>El parámetro de comentario para crear un borrador

El parámetro **comentario** para crear una respuesta o enviar un borrador ([createReply](/graph/api/message-createreply?view=graph-rest-1.0), [createReplyAll](/graph/api/message-createreplyall?view=graph-rest-1.0), [createForward](/graph/api/message-createforward?view=graph-rest-1.0)) no se convierte en parte del cuerpo del borrador del mensaje resultante.

### <a name="get-messages-returns-chats-in-microsoft-teams"></a>Los mensajes de GET devuelven chats en Microsoft Teams

En los extremos de la v1 y la beta, la respuesta de `GET /users/id/messages` incluye los chats de Microsoft Teams del usuario efectuados fuera del ámbito de un equipo o un canal. Estos mensajes de chat tienen "Mensajería instantánea" como el asunto.


## <a name="drives-files-and-content-streaming"></a>Unidades de disco, archivos y streaming de contenido

* La primera vez que accede a una unidad personal del usuario a través de Microsoft Graph antes de que el usuario acceda a su sitio personal a través del explorador, se produce una respuesta 401.

## <a name="query-parameter-limitations"></a>Limitaciones del parámetro de consulta

* No se admiten varios espacios de nombres.
* Las solicitudes GET en `$ref` y la conversión no se admiten en usuarios, grupos, dispositivos, entidades de seguridad y aplicaciones.
* No se admite `@odata.bind`. Esto significa que los desarrolladores no podrán establecer correctamente `Accepted` o `RejectedSenders` en un grupo.
* `@odata.id` no está presente en las navegaciones de no contención (como los mensajes) cuando se usan metadatos mínimos
* `$expand`:
  * No es compatible con `nextLink`
  * No es compatible con más de un nivel de expansión
  * No es compatible con parámetros adicionales (`$filter`, `$select`)
* `$filter`:
  * El punto de conexión `/attachments` no admite filtros. Si están presentes, se ignora el parámetro `$filter`.
  * No se admite el filtrado de cargas de trabajo cruzadas.
* `$search`:
  * La búsqueda de texto completo solo está disponible para un subconjunto de entidades tales como mensajes.
  * No se admite la búsqueda de cargas de trabajo cruzadas.

## <a name="delta-query"></a>Consulta delta

* El contexto OData a veces se devuelve de forma incorrecta cuando se realiza el seguimiento de cambios en las relaciones.
* Las extensiones de esquema (heredadas) no se devuelven con la instrucción $select, pero se devuelven sin $select.
* Los clientes no pueden controlar los cambios para abrir las extensiones o las extensiones de esquema registradas.

## <a name="application-and-serviceprincipal-api-changes"></a>Cambios en la API servicePrincipal y en aplicaciones

Existen cambios actuales en las entidades [application](/graph/api/resources/application?view=graph-rest-beta) y [servicePrincipal](/graph/api/resources/serviceprincipal?view=graph-rest-beta) en el desarrollo. A continuación se muestra un resumen de las limitaciones actuales y las características de la API en el desarrollo.

Limitaciones actuales:

* Algunas propiedades de aplicaciones (como appRoles y addIns) no estarán disponibles hasta que se completen todos los cambios.
* Solo pueden registrarse las aplicaciones multiinquilino.
* La actualización de aplicaciones está restringida a las aplicaciones que se han registrado después de la actualización de la versión beta inicial.
* Los usuarios de Azure Active Directory pueden registrar aplicaciones y agregar propietarios adicionales.
* Compatibilidad con los protocolos OpenID Connect y OAuth.
* Error en las asignaciones de directivas en una aplicación.
* Las operaciones de ownedObjects que necesiten appId producirán un error (Por ejemplo, users/{id|userPrincipalName}/ownedObjects/{id}/...).

En desarrollo:

* Capacidad de registrar aplicaciones de inquilino único.
* Actualizaciones de servicePrincipal.
* Migración de aplicaciones de Azure AD existentes en un modelo actualizado.
* Compatibilidad para appRoles, clientes autorizados previamente, notificaciones opcionales, notificaciones de pertenencia a grupos y personalización de marca.
* Los usuarios de cuentas de Microsoft (MSA) pueden registrar aplicaciones.
* Compatibilidad con los protocolos SAML y WsFed.

## <a name="extensions"></a>Extensiones

### <a name="change-tracking-is-not-supported"></a>No se admite el seguimiento de cambios

El seguimiento de cambios (consulta delta) aún no se admite para las propiedades de extensiones abiertas o de esquema.

### <a name="creating-a-resource-and-open-extension-at-the-same-time"></a>Crear un recurso y una extensión abierta al mismo tiempo

No se puede especificar una extensión abierta a la vez que se crea una instancia de **administrativeUnit**, **device**, **group**, **organization** o **user**. Debe crear primero la instancia y después especificar los datos de extensión abierta en una solicitud ``POST`` posterior en esa instancia.

### <a name="creating-a-resource-instance-and-adding-schema-extension-data-at-the-same-time"></a>Creación de una instancia de recurso y adición de datos de extensión de esquema al mismo tiempo

No se puede especificar una extensión de esquema en la misma operación de creación de una instancia de **contacto**, **evento**, **mensaje** o **publicación**.
Debe crear primero la instancia de recurso y, a continuación, aplicar una revisión `PATCH` a esa instancia para agregar una extensión de esquema y datos personalizados.

### <a name="limit-of-100-schema-extension-property-values-allowed-per-resource-instance"></a>Límite de 100 valores de propiedad de extensión de esquema permitido por cada instancia del recurso

En la actualidad, los recursos de directorio, como **dispositivos**, **grupos** y **usuarios**, limitan a 100 el número total de valores de propiedad de extensión de esquema que pueden establecerse en un recurso.

### <a name="filtering-on-schema-extension-properties-not-supported-on-all-entity-types"></a>No todos los tipos de entidad admiten el filtrado por propiedades de extensión de esquema

Los tipos de entidad de Outlook no admiten el filtrado por propiedades de extensión de esquema (con la expresión `$filter`): **contact**, **event**, **message**o **post**.

## <a name="json-batching"></a>Procesamiento por lotes JSON

### <a name="no-nested-batch"></a>No hay ningún lote anidado

Las solicitudes por lotes JSON no deben contener ninguna solicitud de proceso por lotes anidados.

### <a name="all-individual-requests-must-be-synchronous"></a>Todas las solicitudes individuales deben ser sincrónicas

Todas las solicitudes de contenido en una solicitud por lotes se deben ejecutar de forma sincrónica. Si está presente, se omitirá la preferencia `respond-async`.

### <a name="no-transactions"></a>No hay transacciones

Microsoft Graph no admite actualmente el procesamiento transaccional de solicitudes individuales. Se omitirá la propiedad `atomicityGroup` en solicitudes individuales.

### <a name="uris-must-be-relative"></a>Los URI deben ser relativos

Especifique siempre los identificadores URI relativos en solicitudes por lotes. Microsoft Graph crea estas direcciones URL absolutas mediante el punto de conexión de la versión que está incluido en la URL por lotes.

### <a name="limit-on-batch-size"></a>Límite de tamaño por lotes

Las solicitudes por lotes JSON están limitadas actualmente a veinte solicitudes individuales.

### <a name="simplified-dependencies"></a>Dependencias simplificadas

Las solicitudes individuales pueden depender de otras solicitudes individuales. Actualmente, las solicitudes solo pueden depender de una sola solicitud y deben seguir uno de estos tres modelos:

1. En paralelo: ninguna solicitud individual indica una dependencia de la propiedad `dependsOn`.
2. En serie: todas las solicitudes individuales dependen de la anterior solicitud individual.
3. Igual: todas las solicitudes individuales que indican una dependencia de la propiedad `dependsOn`, indican la misma dependencia.

A medida que madure el procesamiento por lotes JSON, se irán quitando estas limitaciones.

## <a name="cloud-solution-provider-apps"></a>Aplicaciones del Proveedor de soluciones en la nube

### <a name="csp-apps-must-use-azure-ad-endpoint"></a>Las aplicaciones de CSP deben usar el punto de conexión de Azure AD

Las aplicaciones del Proveedor soluciones en la nube (CSP) deben adquirir tokens de los puntos de conexión de Azure AD (v1) para llamar correctamente a Microsoft Graph en sus clientes gestionados por el asociado. Actualmente, no se admite adquirir un token a través del punto de conexión más reciente de Azure AD v2.0.

### <a name="pre-consent-for-csp-apps-doesnt-work-in-some-customer-tenants"></a>El consentimiento previo de las aplicaciones de CSP no funciona en algunos inquilinos de cliente

En determinadas circunstancias, el consentimiento previo de las aplicaciones de CSP puede que no funcione para algunos de los inquilinos de cliente.

- Para las aplicaciones que usan permisos delegados, al usar la aplicación por primera vez con un nuevo inquilino de cliente puede recibir este error después del inicio de sesión: `AADSTS50000: There was an error issuing a token`.
- Para las aplicaciones que usan permisos de aplicación, su aplicación puede adquirir un token, pero obtiene inesperadamente un mensaje de acceso denegado al llamar a Microsoft Graph.

Estamos trabajando en solucionar este problema tan pronto como sea posible para que el consentimiento previo funcione en todos los inquilinos de cliente.

Mientras tanto, para desbloquear el desarrollo y las pruebas, puede usar la siguiente solución alternativa.

>**NOTA:** Esta no es una solución permanente y solo está prevista para desbloquear el desarrollo.  Esta solución alternativa no será necesaria una vez que se solucione el problema mencionado anteriormente.  Esta solución alternativa no necesita deshacerse una vez que se implemente la corrección.

1. Abra una sesión de PowerShell de Azure AD v2 y conéctese al inquilino `customer`. Para ello, escriba sus credenciales de administrador en la ventana de inicio de sesión. Puede descargar e instalar PowerShell V2 para Azure AD desde [aquí](https://www.powershellgallery.com/packages/AzureAD).

    ```PowerShell
    Connect-AzureAd -TenantId {customerTenantIdOrDomainName}
    ```

2. Cree la entidad de servicio de Microsoft Graph.

    ```PowerShell
    New-AzureADServicePrincipal -AppId 00000003-0000-0000-c000-000000000000
    ```

## <a name="functionality-available-only-in-office-365-rest-or-azure-ad-graph-apis"></a>Esta función solo está disponible en las API de REST de Office 365 o las API de Graph de Azure AD

Algunas funciones todavía no están disponibles en Microsoft Graph. Si no ve la funcionalidad que busca, puede usar las [API de REST de Office 365](https://msdn.microsoft.com/office/office365/api/api-catalog) específicas del punto de conexión. Para Azure Active Directory, consulte la publicación del blog [Microsoft Graph o Azure AD Graph](https://dev.office.com/blogs/microsoft-graph-or-azure-ad-graph) sobre las características que solo están disponibles a través de la API de Azure AD Graph.

## <a name="feedback"></a>Comentarios

> Su opinión es importante para nosotros. Conecte con nosotros en [Desbordamiento de pila](https://stackoverflow.com/questions/tagged/microsoftgraph).
