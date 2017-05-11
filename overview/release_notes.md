# <a name="known-issues-with-microsoft-graph"></a>Problemas conocidos de Microsoft Graph

En este artículo, se describen los problemas conocidos de Microsoft Graph. Para obtener información acerca de las actualizaciones más recientes, consulte el [Registro de cambios de Microsoft Graph](http://graph.microsoft.io/en-us/changelog).

## <a name="graph-quick-start"></a>Inicio rápido de Graph
30 de abril de 2017: hay un error en el inicio rápido. Los flujos tienen un error en el que la URL de redireccionamiento no está configurada correctamente para Asp.Net MVC, Node.js, Angular, PHP, Python y Ruby. Estamos trabajando para obtener la corrección implementada en producción. Para resolver este problema, consulte nuestros [Tutoriales de introducción](https://developer.microsoft.com/en-us/graph/docs/get-started/get-started).   Esto se ha resuelto el 3 de mayo.

## <a name="graph-explorer"></a>Probador de Graph
Hemos desactivado los inicios de sesión de la cuenta Microsoft en el Explorador de Graph debido a un problema de servicio. Estamos trabajando activamente en una corrección y actualizaremos este texto cuando esté lista.  Actualización del 3 de mayo: ya se ha resuelto.

Los inicios de sesión con Internet Explorer y Microsoft Edge no funcionaban. Este problema está resuelto desde el 2 de febrero de 2017.

## <a name="users"></a>Usuarios
#### <a name="no-instant-access-after-creation"></a>No hay acceso instantáneo después de la creación
Los usuarios pueden crearse inmediatamente a través de un POST en la entidad del usuario. Una licencia de Office 365 primero se debe asignar a un usuario, con el fin de obtener acceso a los servicios de Office 365. Incluso entonces, debido a la naturaleza distribuida del servicio, puede llevar 15 minutos que los archivos, mensajes y entidades de eventos estén disponibles para su uso para este usuario, a través de la API de Microsoft Graph. Durante este tiempo, las aplicaciones recibirán una respuesta de error HTTP 404. 

#### <a name="photo-restrictions"></a>Restricciones de la foto
Leer y actualizar la foto de perfil de un usuario solo es posible si el usuario tiene un buzón. Además, cualquier foto que *pueda* haberse almacenado previamente mediante la propiedad **thumbnailPhoto** (usando la versión preliminar de la API unificada de Office 365 o Azure AD Graph, o bien mediante la sincronización de AD Connect) ya no será accesible mediante la propiedad de foto del usuario de Microsoft Graph. En este caso, no poder leer o actualizar una foto provocaría el error siguiente:

```javascript
    {
      "error": {
        "code": "ErrorNonExistentMailbox",
        "message": "The SMTP address has no mailbox associated with it."
      }
    }
```

 > **Nota**:  Poco después de GA, se habilitará el almacenamiento y la recuperación de las fotos de perfil del usuario, incluso cuando el usuario no tenga un buzón, y este error debería desaparecer.


#### <a name="adding-and-accessing-ics-based-calendars-in-users-mailbox"></a>Agregar y acceder a calendarios basados en archivos ICS en el buzón del usuario
Actualmente, existe una compatibilidad parcial con un calendario basado en una suscripción a calendarios de Internet (ICS):

* Puede agregar un calendario basado en ICS a un buzón de usuario mediante la interfaz de usuario, pero no mediante la API de Microsoft Graph. 
* [Enumerar los calendarios del usuario](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/user_list_calendars) le permite obtener las propiedades **name**, **color** e **id** de cada [calendario](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/calendar) en el grupo de calendarios predeterminado del usuario, o en un grupo de calendarios especificado, incluidos los calendarios basados en ICS. No puede almacenar ni acceder a la dirección URL de una ICS en el recurso del calendario.
* También puede [enumerar los eventos](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/calendar_list_events) de un calendario basado en ICS.

#### <a name="using-delta-query"></a>Usar la consulta de delta
Para ver los problemas conocidos al usar la consulta de delta, consulte la [sección Consulta de delta](#delta-query) de este artículo.

## <a name="groups"></a>Grupos
#### <a name="policy"></a>Directiva
Usar Microsoft Graph para crear y nombrar un grupo de Office 365 omite cualquier directiva de grupo de Office 365 que esté configurada a través de Outlook Web App. 

#### <a name="group-permission-scopes"></a>Ámbitos de permiso de grupo
Microsoft Graph expone dos ámbitos de permisos (*Group.Read.All* y *Group.ReadWrite.All*) para obtener acceso a las API de grupos.  
Estos ámbitos de permisos deben ser aceptados por un administrador (lo que supone un cambio respecto a la versión preliminar).  En el futuro, planeamos agregar nuevos ámbitos para grupos que pueden ser aceptados por los usuarios.

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


#### <a name="adding-and-getting-attachments-of-group-posts"></a>Agregar y obtener los datos adjuntos de las publicaciones de grupo
Actualmente, al [agregar](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/post_post_attachments) datos adjuntos a las publicaciones de grupo, así como al [enumerar](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/post_list_attachments) y obtener los datos adjuntos de las publicaciones de grupo, se devuelve el mensaje de error "La solicitud de OData no es compatible". Se ha desarrollado una corrección tanto para la versión `/v1.0` como para la `/beta` y se espera que esté disponible a finales de enero de 2016.


#### <a name="setting-the-allowexternalsenders-property"></a>Establecer la propiedad allowExternalSenders
Existe en la actualidad un problema que evita el establecimiento de la propiedad **allowExternalSenders** de un grupo en operaciones POST o PATCH, en `/v1.0` y `/beta`.

#### <a name="using-delta-query"></a>Usar la consulta de delta
Para ver los problemas conocidos al usar la consulta de delta, consulte la [sección Consulta de delta](#delta-query) de este artículo.

## <a name="contacts"></a>Contactos

#### <a name="organization-contacts-available-in-only-beta"></a>Contactos de organización disponibles solo en beta
Solo los contactos personales son compatibles actualmente. Actualmente no se admiten contactos de la organización en `/v1.0`, pero pueden encontrarse en `/beta`.

#### <a name="default-contacts-folder"></a>Carpeta de contactos predeterminada

En la versión `/v1.0`, `GET /me/contactFolders` no incluye la carpeta de contactos predeterminada del usuario. 

Estará disponible una corrección. Mientras tanto, puede usar la siguiente consulta [enumerar contactos](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/user_list_contacts) y la propiedad **parentFolderId** como una solución alternativa para obtener el identificador de la carpeta de contactos predeterminada:

```
GET https://graph.microsoft.com/v1.0/me/contacts?$top=1&$select=parentFolderId
```
En la consulta anterior:
1. `/me/contacts?$top=1` obtiene las propiedades de un elemento [contact](http://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/contact) de la carpeta de contactos predeterminada.
2. Al anexar `&$select=parentFolderId` se devuelve solo la propiedad **parentFolderId** del contacto, que es el identificador de la carpeta de contactos predeterminada.


#### <a name="accessing-contacts-via-a-contact-folder-in-beta"></a>Acceder a contactos a través de una carpeta de contactos en la versión beta
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
#### <a name="the-comment-parameter-for-creating-a-draft"></a>El parámetro de comentario para crear un borrador
El parámetro **comentario** para crear una respuesta o enviar un borrador ([createReply](../api-reference/v1.0/api/message_createreply.md), [createReplyAll](../api-reference/v1.0/api/message_createreplyall.md), [createForward](../api-reference/v1.0/api/message_createforward.md)) no se convierte en parte del cuerpo del borrador del mensaje resultante.  


## <a name="drives-files-and-content-streaming"></a>Unidades, archivos y streaming de contenido
* La primera vez que accede a una unidad personal del usuario a través de Microsoft Graph antes de que el usuario acceda a su sitio personal a través del explorador, se produce una respuesta 401.

## <a name="functionality-available-only-in-office-365-rest-apis"></a>Esta funcionalidad solo está disponible en las API de REST de Office 365

Algunas funciones todavía no están disponibles en Microsoft Graph. Si no ve la funcionalidad que busca, puede usar las [API de REST de Office 365](https://msdn.microsoft.com/en-us/office/office365/api/api-catalog) específicas del punto de conexión.


#### <a name="batching"></a>Procesamiento por lotes
El procesamiento por lotes no se admite en Microsoft Graph. Sin embargo, puede usar el punto de conexión en versión beta de Outlook y [las llamadas REST por lotes de Outlook](https://msdn.microsoft.com/en-us/office/office365/api/batch-outlook-rest-requests). 

#### <a name="availability-in-china"></a>Disponibilidad en China
El servicio de Microsoft Graph está operado por 21Vianet (y ahora disponible en China). Consulte [Implementaciones de nube soberana de Microsoft Graph](http://developer.microsoft.com/en-us/graph/docs/overview/deployments) para obtener más información, incluidas las restricciones.

#### <a name="service-actions-and-functions"></a>Funciones y acciones del servicio
`isMemberOf` y `getObjectsById` no están disponibles en Microsoft Graph

## <a name="microsoft-graph-permissions"></a>Permisos de Microsoft Graph
Consulte [Ámbitos de permiso](http://developer.microsoft.com/en-us/graph/docs/authorization/permission_scopes) para obtener la información más reciente acerca de los permisos delegados y de aplicación que admite Microsoft Graph. Además, se aplican a `v1.0` las siguientes limitaciones:

|Permiso |    Tipo de permiso | Limitación |    Alternativa |
|-----------|-----------------|------------|--------------|
|_User.ReadWrite_| Delegado    | No se puede actualizar el número de teléfono móvil|    Seleccionar también `Directory.AccessAsUser.All`| 
|_User.ReadWrite.All_|    Delegado|    No se puede realizar ninguna operación CRUD en `User` que no sea la actualización de la foto HD del usuario y las propiedades de perfil extendidas|    Seleccione también `Directory.ReadWrite.All` o `Directory.AccessAsUser.All` si se requiere la eliminación del usuario.|
|_User.Read.All_|    Aplicación    |No se puede realizar ninguna operación de lectura en otros usuarios|    Seleccionar también `Directory.Read.All`|
| _User.ReadWrite.All_ |    Aplicación |    No se puede realizar ninguna operación CRUD en `User` que no sea la actualización de la foto HD del usuario y las propiedades de perfil extendidas |    Seleccionar también`Directory.ReadWrite.All`. **NOTA**: La eliminación del usuario no será posible.|
|_Group.Read.All_    | Aplicación |    No se pueden enumerar los grupos ni las pertenencias a estos.  Todavía se puede leer el contenido del grupo para los grupos de Office    | Seleccionar también `Directory.Read.All` |
|_Group.ReadWrite.All_    | Aplicación    | No se pueden enumerar grupos ni pertenencias a grupos, crear grupos, actualizar pertenencias a grupos ni eliminar grupos.  Todavía se puede leer y actualizar el contenido del grupo para los grupos de Office.    | Seleccionar también `Directory.ReadWrite.All`. **NOTA**:  La eliminación del grupo no será posible.|

Además, existen las siguientes `/beta` limitaciones:

|Permiso |    Tipo de permiso | Limitación |    Alternativa |
|-----------|-----------------|------------|--------------|
| _Group.ReadWrite.All_    | Delegado    | No se puede leer ni actualizar las tareas del planificador de los grupos de Office    | Seleccionar también `Tasks.ReadWrite`|
|_Tasks.ReadWrite_    | Delegado    | No se puede leer ni actualizar las tareas del usuario que inició sesión| Seleccionar también `Group.ReadWrite.All`|

## <a name="odata-related-limitations"></a>Limitaciones relacionadas con OData
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

  >  Su opinión es importante para nosotros. Póngase en contacto con nosotros en [Stack Overflow](http://stackoverflow.com/questions/tagged/office365). Etiquete sus preguntas con {MicrosoftGraph} y {office365}.

## <a name="delta-query"></a>Consulta de delta

Solo se admite el seguimiento de cambios en las relaciones de usuarios y grupos dentro de la clase de recurso específica en la que se están siguiendo los cambios. Por ejemplo, si un cliente sigue los cambios en *grupos* y ha seleccionado la relación *miembros*, solo recibirá actualizaciones de pertenencia en la respuesta de consulta de delta si esos miembros son también *grupos*. Es decir, aún no es posible realizar el seguimiento de miembros para usuarios. El equipo de Microsoft Graph comprende que se trata de un escenario de alta prioridad y hay prevista una actualización pronto.
