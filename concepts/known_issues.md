# <a name="known-issues-with-microsoft-graph"></a>Problemas conocidos de Microsoft Graph

En este artículo, se describen los problemas conocidos de Microsoft Graph. Para obtener información acerca de las actualizaciones más recientes, consulte el [Registro de cambios de Microsoft Graph](changelog.md).

## <a name="users"></a>Usuarios

### <a name="no-instant-access-after-creation"></a>No hay acceso instantáneo después de la creación

Los usuarios pueden crearse inmediatamente a través de un POST en la entidad del usuario. Una licencia de Office 365 primero se debe asignar a un usuario, con el fin de obtener acceso a los servicios de Office 365. Incluso entonces, debido a la naturaleza distribuida del servicio, puede llevar 15 minutos que los archivos, mensajes y entidades de eventos estén disponibles para su uso para este usuario, a través de la API de Microsoft Graph. Durante este tiempo, las aplicaciones recibirán una respuesta de error HTTP 404.

### <a name="photo-restrictions"></a>Restricciones de la foto

Leer y actualizar la foto de perfil de un usuario solo es posible si el usuario tiene un buzón. Además, cualquier foto que *pueda* haberse almacenado previamente mediante la propiedad **thumbnailPhoto** (usando la vista previa de la API unificada de Office 365 o Azure AD Graph, o bien mediante la sincronización de AD Connect) ya no será accesible mediante la propiedad de **foto** del recurso de [usuario](../api-reference/v1.0/resources/user.md). En este caso, no poder leer o actualizar una foto provocaría el error siguiente:

```javascript
    {
      "error": {
        "code": "ErrorNonExistentMailbox",
        "message": "The SMTP address has no mailbox associated with it."
      }
    }
```

### <a name="adding-and-accessing-ics-based-calendars-in-users-mailbox"></a>Agregar y acceder a calendarios basados en archivos ICS en el buzón del usuario

Actualmente, existe una compatibilidad parcial con un calendario basado en una suscripción a calendarios de Internet (ICS):

* Puede agregar un calendario basado en ICS a un buzón de usuario mediante la interfaz de usuario, pero no mediante la API de Microsoft Graph.
* [Enumerar los calendarios del usuario](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/user_list_calendars) le permite obtener las propiedades **name**, **color** e **id.** de cada [calendario](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/calendar) en el grupo de calendarios predeterminado del usuario, o en un grupo de calendarios especificado, incluidos los calendarios basados en ICS. No puede almacenar ni acceder a la dirección URL de una ICS en el recurso del calendario.
* También puede [enumerar los eventos](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/calendar_list_events) de un calendario basado en ICS.

### <a name="using-delta-query"></a>Usar la consulta de delta

Para ver los problemas conocidos al usar la consulta delta, consulte la [sección Consulta delta](#delta-query) de este artículo.

## <a name="groups-and-microsoft-teams"></a>Grupos y Microsoft Teams

>**Nota** Teams Microsoft ahora está en estado de vista previa disponible en sólo el extremo de la versión beta de Microsoft Graph.

### <a name="policy"></a>Directiva

Usar Microsoft Graph para crear y nombrar un grupo de Office 365 omite cualquier directiva de grupo de Office 365 que esté configurada a través de Outlook Web App. 

### <a name="permissions-for-groups-and-microsoft-teams"></a>Permisos para grupos y Microsoft Teams

Microsoft Graph expone dos permisos (*Group.Read.All* and *Group.ReadWrite.All*) para obtener acceso a las API de grupos y Microsoft Teams. Un administrador debe aceptar estos permisos (lo que supone un cambio respecto a la vista previa).  En el futuro, plantearemos agregar nuevos permisos para los grupos y equipos que puedan admitir los usuarios.

Además, solo la API para la administración y gestión del grupo principal admite el acceso con permisos delegados o solo de aplicación. El resto de características de la API de grupo solo admiten permisos delegados.

Ejemplos de funciones de grupo que admiten permisos delegados y de aplicación:

* Crear y eliminar grupos
* Obtener y actualizar las propiedades de grupos relativas a la administración de grupos.
* Grupo [configuración del directorio](../api-reference/v1.0/resources/directoryobject.md), tipo y sincronización
* Propietarios de grupo y pertenencia


Ejemplos de funciones de grupo que admiten solo permisos delegados:

* Conversaciones, eventos y fotos de grupo
* Remitentes externos, remitentes aceptados o rechazados, suscripciones a grupos
* Favoritos del usuario y recuento no visto

### <a name="teams-in-microsoft-teams-preview"></a>Equipos de Microsoft Teams (vista previa)

Microsoft Teams se basa en grupos de Office 365.  Todas las API de grupo pueden utilizarse también con los equipos, con la excepción de que "Crear grupo" no le permite crear un equipo en este momento.  Las versiones futuras de API serán compatibles con esto.

### <a name="microsoft-teams-channels-preview"></a>Canales de Microsoft Teams (vista previa)

Actualmente, puede leer y crear canales, pero no puede actualizarlos o eliminarlos.  Las versiones futuras de API serán compatibles con esto.

### <a name="microsoft-teams-chat-threads-and-chat-messages-preview"></a>Mensajes de chat y conversaciones de chat de Microsoft Teams (vista previa)

Actualmente, se pueden crear conversaciones de chat en canales, pero no puede leer las conversaciones de chat existentes o agregar respuestas.  Del mismo modo, no se puede leer o escribir chats directos entre los usuarios que están fuera del ámbito de un grupo o un canal.  Las versiones futuras de API agregarán capacidades adicionales en esta área.


### <a name="adding-and-getting-attachments-of-group-posts"></a>Agregar y obtener los datos adjuntos de las publicaciones de grupo

Actualmente, al [agregar](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/post_post_attachments) datos adjuntos a las publicaciones de grupo, así como al [enumerar](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/post_list_attachments) y obtener los datos adjuntos de las publicaciones de grupo, se devuelve el mensaje de error "La solicitud de OData no es compatible". Se ha desarrollado una corrección tanto para la versión `/v1.0` como para la `/beta` y se espera que esté disponible a finales de enero de 2016.

### <a name="setting-the-allowexternalsenders-property"></a>Establecer la propiedad allowExternalSenders

Existe en la actualidad un problema que evita el establecimiento de la propiedad **allowExternalSenders** de un grupo en operaciones POST o PATCH, en `/v1.0` y `/beta`.

### <a name="using-delta-query"></a>Usar la consulta de delta

Para ver los problemas conocidos al usar la consulta de delta, consulte la [sección Consulta de delta](#delta-query) de este artículo.

## <a name="contacts"></a>Contactos

### <a name="organization-contacts-available-in-only-beta"></a>Contactos de organización disponibles solo en beta

Solo los contactos personales son compatibles actualmente. Actualmente no se admiten contactos de la organización en `/v1.0`, pero pueden encontrarse en `/beta`.

### <a name="default-contacts-folder"></a>Carpeta de contactos predeterminada

En la versión `/v1.0`, `GET /me/contactFolders` no incluye la carpeta de contactos predeterminada del usuario. 

Estará disponible una corrección. Mientras tanto, puede usar la siguiente consulta [enumerar contactos](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/user_list_contacts) y la propiedad **parentFolderId** como una solución alternativa para obtener el identificador de la carpeta de contactos predeterminada:

```http
GET https://graph.microsoft.com/v1.0/me/contacts?$top=1&$select=parentFolderId
```

En la consulta anterior:

1. `/me/contacts?$top=1` obtiene las propiedades de un elemento [contact](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/contact) de la carpeta de contactos predeterminada.
2. Al anexar `&$select=parentFolderId` se devuelve solo la propiedad **parentFolderId** del contacto, que es el identificador de la carpeta de contactos predeterminada.


### <a name="accessing-contacts-via-a-contact-folder-in-beta"></a>Acceder a contactos a través de una carpeta de contactos en la versión beta

En la versión `/beta`, existe un problema en la actualidad que impide acceder a un [contacto](../api-reference/beta/resources/contact.md) especificando su carpeta primaria en la dirección de solicitud REST, tal y como se muestra en los dos escenarios siguientes.

* Acceso a un contacto desde un [contactFolder](../api-reference/beta/resources/contactfolder.md) de nivel superior del usuario.

```http
GET /me/contactfolders/{id}/contacts/{id}
GET /users/{id | userPrincipalName}/contactfolders/{id}/contacts/{id}
```

* Acceso a un contacto contenido en una carpeta secundaria de una **contactFolder**.  En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.

```http
GET /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
GET /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```

Como alternativa, puede simplemente [obtener](../api-reference/beta/api/contact_get.md) el contacto especificando su identificador, tal como se muestra a continuación, ya que GET/contacts en la versión `/beta` se aplica a todos los contactos del buzón de correo del usuario:

```http
GET /me/contacts/{id}
GET /users/{id | userPrincipalName}/contacts/{id}
```

## <a name="messages"></a>Mensajes

### <a name="the-comment-parameter-for-creating-a-draft"></a>El parámetro de comentario para crear un borrador

El parámetro **comentario** para crear una respuesta o enviar un borrador ([createReply](../api-reference/v1.0/api/message_createreply.md), [createReplyAll](../api-reference/v1.0/api/message_createreplyall.md), [createForward](../api-reference/v1.0/api/message_createforward.md)) no se convierte en parte del cuerpo del borrador del mensaje resultante.  

## <a name="drives-files-and-content-streaming"></a>Unidades, archivos y streaming de contenido

* La primera vez que accede a una unidad personal del usuario a través de Microsoft Graph antes de que el usuario acceda a su sitio personal a través del explorador, se produce una respuesta 401.

## <a name="query-parameter-limitations"></a>Limitaciones del parámetro de consulta

* Limitaciones de **$expand**:
    * No se admite para `nextLink`
     * No se admite para más de un nivel de expansión
     * No se admite con parámetros adicionales (**$filter**, **$select**)
* No se admiten varios espacios de nombres
* Las solicitudes GET en `$ref` y la conversión no se admiten en usuarios, grupos, dispositivos, entidades de servicio y aplicaciones.
* `@odata.bind` no se admite.  Esto significa que los desarrolladores no podrán establecer correctamente `Accepted` o `RejectedSenders` en un grupo.
* `@odata.id` no está presente en las navegaciones de no contención (como los mensajes) cuando se usan metadatos mínimos
* No está disponible el filtrado o la búsqueda de carga de trabajo cruzada. 
* La búsqueda de texto completo (con **$search**) solo está disponible para algunas entidades, como los mensajes.

## <a name="delta-query"></a>Consulta delta

* El contexto OData a veces se devuelve de forma incorrecta cuando se realiza el seguimiento de cambios en las relaciones.
* Las extensiones de esquema (heredadas) no se devuelven con la instrucción $select, pero se devuelven sin $select.
* Los clientes no pueden controlar los cambios para abrir las extensiones o las extensiones de esquema registradas.

## <a name="extensions"></a>Extensiones

### <a name="change-tracking-is-not-supported"></a>No se admite el seguimiento de cambios

El seguimiento de cambios (consulta delta) aún no se admite para las propiedades de extensiones abiertas o de esquema.

### <a name="creating-a-resource-and-open-extension-at-the-same-time"></a>Crear un recurso y una extensión abierta al mismo tiempo

No se puede especificar una extensión abierta a la vez que se crea una instancia de **administrativeUnit**, **device**, **group**, **organization** o **user**. Debe crear primero la instancia y después especificar los datos de extensión abierta en una solicitud ``POST`` posterior en esa instancia.

### <a name="limit-of-100-schema-extension-property-values-allowed-per-resource-instance"></a>Límite de 100 valores de propiedad de extensión de esquema permitido por cada instancia del recurso

En la actualidad, los recursos de directorio, como **dispositivos**, **grupos** y **usuarios**, limitan a 100 el número total de valores de propiedad de extensión de esquema que pueden establecerse en un recurso.

## <a name="json-batching"></a>Procesamiento por lotes JSON

### <a name="no-nested-batch"></a>No hay ningún lote anidado

Las solicitudes por lotes JSON no deben contener ninguna solicitud de proceso por lotes anidados.

### <a name="all-individual-requests-must-be-synchronous"></a>Todas las solicitudes individuales deben ser sincrónicas

Todas las solicitudes de contenido en una solicitud por lotes se deben ejecutar de forma sincrónica. Si está presente, se omitirá la preferencia `respond-async`.

### <a name="no-transactions"></a>No hay transacciones

Microsoft Graph no admite actualmente el procesamiento transaccional de solicitudes individuales. Se omitirá la propiedad `atomicityGroup` en solicitudes individuales.

### <a name="uris-must-be-relative"></a>Los URI deben ser relativos

Especificar siempre los identificadores URI relativos en solicitudes por lotes. Microsoft Graph crea estas direcciones URL absolutas mediante el punto de conexión de la versión que está incluido en la URL por lotes.

### <a name="limit-on-batch-size"></a>Límite de tamaño por lotes

Las solicitudes por lotes JSON están limitadas actualmente a cinco solicitudes individuales. A medida se desarrolla el procesamiento por lotes JSON, se produce este límite.

### <a name="simplified-dependencies"></a>Dependencias simplificadas

Las solicitudes individuales pueden depender de otras solicitudes individuales. Actualmente, las solicitudes solo pueden depender de una sola solicitud y deben seguir uno de estos tres modelos:

1. En paralelo - Ninguna solicitud individual indica una dependencia de la propiedad `dependsOn`.
2. En serie - Todas las solicitudes individuales dependen de la anterior solicitud individual.
3. Mismo - Todas las solicitudes individuales que indican una dependencia de la propiedad `dependsOn`, indican la misma dependencia.

A medida que crece el procesamiento por lotes JSON, se eliminan estas limitaciones.

## <a name="cloud-solution-provider-apps-must-use-azure-ad-endpoint"></a>Las aplicaciones del Proveedor de soluciones en la nube deben utilizar el punto de conexión Azure AD

Las aplicaciones del Proveedor soluciones en la nube (CSP) deben adquirir tokens de los puntos de conexión de Azure AD (v1) para llamar correctamente a Microsoft Graph en sus clientes gestionados por el asociado. Actualmente, no se admite adquirir un token a través de los puntos de conexión de v2.0 de Azure AD más recientes.

## <a name="functionality-available-only-in-office-365-rest-or-azure-ad-graph-apis"></a>Esta funcionalidad solo está disponible en las API de REST de Office 365 o las API de Graph de Azure AD

Algunas funciones todavía no están disponibles en Microsoft Graph. Si no ve la funcionalidad que busca, puede usar las [API de REST de Office 365](https://msdn.microsoft.com/en-us/office/office365/api/api-catalog) específicas del punto de conexión. Para Azure Active Directory, consulte la publicación en el blog [Microsoft Graph o Azure AD Graph](https://dev.office.com/blogs/microsoft-graph-or-azure-ad-graph) que se encuentra en las características que solo están disponibles a través de la API de Azure AD Graph.

### <a name="feedback"></a>Comentarios

> Su opinión es importante para nosotros. Conecte con nosotros en [Desbordamiento de pila](http://stackoverflow.com/questions/tagged/microsoftgraph).
