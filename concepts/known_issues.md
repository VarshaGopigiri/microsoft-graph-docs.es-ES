# <a name="known-issues-with-microsoft-graph"></a><span data-ttu-id="26d34-101">Problemas conocidos de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="26d34-101">Known issues with Microsoft Graph</span></span>

<span data-ttu-id="26d34-p101">En este artículo, se describen los problemas conocidos de Microsoft Graph. Para obtener información sobre las actualizaciones más recientes, consulte el [Registro de cambios de Microsoft Graph](changelog.md).</span><span class="sxs-lookup"><span data-stu-id="26d34-p101">This article describes known issues with Microsoft Graph. For information about the latest updates, see the [Microsoft Graph changelog](changelog.md).</span></span>

## <a name="users"></a><span data-ttu-id="26d34-104">Usuarios</span><span class="sxs-lookup"><span data-stu-id="26d34-104">Users</span></span>

### <a name="no-instant-access-after-creation"></a><span data-ttu-id="26d34-105">No hay acceso instantáneo después de la creación</span><span class="sxs-lookup"><span data-stu-id="26d34-105">No instant access after creation</span></span>

<span data-ttu-id="26d34-p102">Los usuarios pueden crearse inmediatamente a través de un POST en la entidad del usuario. Una licencia de Office 365 primero se debe asignar a un usuario, con el fin de obtener acceso a los servicios de Office 365. Incluso entonces, debido a la naturaleza distribuida del servicio, puede llevar 15 minutos que los archivos, mensajes y entidades de eventos estén disponibles para su uso para este usuario, a través de la API de Microsoft Graph. Durante este tiempo, las aplicaciones recibirán una respuesta de error HTTP 404.</span><span class="sxs-lookup"><span data-stu-id="26d34-p102">Users can be created immediately through a POST on the user entity. An Office 365 license must first be assigned to a user, in order to get access to Office 365 services. Even then, due to the distributed nature of the service, it might take 15 minutes before files, messages and events entities are available for use for this user, through the Microsoft Graph API. During this time, apps will receive a 404 HTTP error response.</span></span>

### <a name="photo-restrictions"></a><span data-ttu-id="26d34-110">Restricciones de la foto</span><span class="sxs-lookup"><span data-stu-id="26d34-110">Photo restrictions</span></span>

<span data-ttu-id="26d34-p103">Leer y actualizar la foto de perfil de un usuario solo es posible si el usuario tiene un buzón. Además, cualquier foto que *pueda* haberse almacenado previamente mediante la propiedad **thumbnailPhoto** (usando la vista previa de la API unificada de Office 365 o Azure AD Graph, o bien mediante la sincronización de AD Connect) ya no será accesible mediante la propiedad **photo** del recurso [user](../api-reference/v1.0/resources/user.md). En este caso, no poder leer o actualizar una foto provocaría el error siguiente:</span><span class="sxs-lookup"><span data-stu-id="26d34-p103">Reading and updating a user's profile photo is only possible if the user has a mailbox. Additionally, any photos that *may* have been previously stored using the **thumbnailPhoto** property (using the Office 365 unified API preview, or the Azure AD Graph, or through AD Connect synchronization) are no longer accessible through the Microsoft Graph **photo** property of the [user](../api-reference/v1.0/resources/user.md) resource. Failure to read or update a photo, in this case, would result in the following error:</span></span>

```javascript
    {
      "error": {
        "code": "ErrorNonExistentMailbox",
        "message": "The SMTP address has no mailbox associated with it."
      }
    }
```


### <a name="using-delta-query"></a><span data-ttu-id="26d34-114">Usar la consulta de delta</span><span class="sxs-lookup"><span data-stu-id="26d34-114">Using delta query</span></span>

<span data-ttu-id="26d34-115">Para ver los problemas conocidos al usar la consulta delta, consulte la [sección Consulta delta](#delta-query) de este artículo.</span><span class="sxs-lookup"><span data-stu-id="26d34-115">For known issues using delta query, see the [delta query section](#delta-query) in this article.</span></span>

## <a name="groups-and-microsoft-teams"></a><span data-ttu-id="26d34-116">Grupos y Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="26d34-116">Groups and Microsoft Teams</span></span>

><span data-ttu-id="26d34-117">**Nota** Actualmente, Microsoft Teams está en versión preliminar y solo se encuentra disponible en el punto de conexión de la versión beta de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="26d34-117">**Note** Microsoft Teams is currently in preview and is available only in the Microsoft Graph beta endpoint.</span></span>

### <a name="policy"></a><span data-ttu-id="26d34-118">Directiva</span><span class="sxs-lookup"><span data-stu-id="26d34-118">Policy</span></span>

<span data-ttu-id="26d34-119">Usar Microsoft Graph para crear y nombrar un grupo de Office 365 omite cualquier directiva de grupo de Office 365 que esté configurada a través de Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="26d34-119">Using Microsoft Graph to create and name an Office 365 group bypasses any Office 365 group policies that are configured through Outlook Web App.</span></span>

### <a name="permissions-for-groups-and-microsoft-teams"></a><span data-ttu-id="26d34-120">Permisos para grupos y Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="26d34-120">Permissions for groups and Microsoft Teams</span></span>

<span data-ttu-id="26d34-p104">Microsoft Graph expone dos permisos (*Group.Read.All* y *Group.ReadWrite.All*) para obtener acceso a las API de grupos y Microsoft Teams. Un administrador debe aceptar estos permisos (lo que supone un cambio respecto a la versión preliminar).  En el futuro, plantearemos agregar nuevos permisos para los grupos y equipos que puedan admitir los usuarios.</span><span class="sxs-lookup"><span data-stu-id="26d34-p104">Microsoft Graph exposes two permissions (*Group.Read.All* and *Group.ReadWrite.All*) for access to the APIs for groups and Microsoft Teams. These permissions must be consented to by an administrator (which is a change from preview).  In the future, we plan to add new permissions for groups and teams that users can consent to.</span></span>

<span data-ttu-id="26d34-p105">Además, solo la API para la administración y gestión del grupo principal admite el acceso con permisos delegados o solo de aplicación. El resto de características de la API de grupo solo admiten permisos delegados.</span><span class="sxs-lookup"><span data-stu-id="26d34-p105">Also, only the API for core group administration and management supports access using delegated or app-only permissions. All other features of the group API support only delegated permissions.</span></span>

<span data-ttu-id="26d34-126">Ejemplos de funciones de grupo que admiten permisos delegados y de aplicación:</span><span class="sxs-lookup"><span data-stu-id="26d34-126">Examples of group features that support delegated and app-only permissions:</span></span>

* <span data-ttu-id="26d34-127">Crear y eliminar grupos</span><span class="sxs-lookup"><span data-stu-id="26d34-127">Creating and deleting groups</span></span>
* <span data-ttu-id="26d34-128">Obtener y actualizar las propiedades de grupos relativas a la administración de grupos.</span><span class="sxs-lookup"><span data-stu-id="26d34-128">Getting and updating group properties pertaining to group administration or management</span></span>
* <span data-ttu-id="26d34-129">Grupo [configuración del directorio](../api-reference/v1.0/resources/directoryobject.md), tipo y sincronización</span><span class="sxs-lookup"><span data-stu-id="26d34-129">Group [directory settings](../api-reference/v1.0/resources/directoryobject.md), type, and synchronization</span></span>
* <span data-ttu-id="26d34-130">Propietarios de grupo y pertenencia</span><span class="sxs-lookup"><span data-stu-id="26d34-130">Group owners and membership</span></span>

<span data-ttu-id="26d34-131">Ejemplos de funciones de grupo que admiten solo permisos delegados:</span><span class="sxs-lookup"><span data-stu-id="26d34-131">Examples of group features that support only delegated permissions:</span></span>

* <span data-ttu-id="26d34-132">Conversaciones, eventos y fotos de grupo</span><span class="sxs-lookup"><span data-stu-id="26d34-132">Group conversations, events, photo</span></span>
* <span data-ttu-id="26d34-133">Remitentes externos, remitentes aceptados o rechazados, suscripciones a grupos</span><span class="sxs-lookup"><span data-stu-id="26d34-133">External senders, accepted or rejected senders, group subscription</span></span>
* <span data-ttu-id="26d34-134">Favoritos del usuario y recuento no visto</span><span class="sxs-lookup"><span data-stu-id="26d34-134">User favorites and unseen count</span></span>
* <span data-ttu-id="26d34-135">Canales de Microsoft Teams y charlas</span><span class="sxs-lookup"><span data-stu-id="26d34-135">Microsoft Teams channels and chats</span></span>

### <a name="teams-in-microsoft-teams-preview"></a><span data-ttu-id="26d34-136">Equipos de Microsoft Teams (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="26d34-136">Teams in Microsoft Teams (preview)</span></span>

<span data-ttu-id="26d34-p106">Microsoft Teams y Grupos de Office 365 [comparten una funcionalidad similar](../api-reference/beta/resources/teams_api_overview.md). Todas las API de grupo se pueden usar con los equipos, salvo que en este momento la API de creación de grupo no le permite crear un equipo.  Las versiones futuras de la API admitirán esta posibilidad.</span><span class="sxs-lookup"><span data-stu-id="26d34-p106">Microsoft Teams and Office 365 groups [share similar functionality](../api-reference/beta/resources/teams_api_overview.md). All group APIs can be used with teams, with the exception that the Create group API does not currently allow you to create a team.  Future API releases will support this.</span></span>

### <a name="microsoft-teams-chat-threads-and-chat-messages-preview"></a><span data-ttu-id="26d34-140">Mensajes de chat y conversaciones de chat de Microsoft Teams (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="26d34-140">Microsoft Teams chat threads and chat messages (preview)</span></span>

<span data-ttu-id="26d34-p107">Actualmente, se pueden crear conversaciones de chat en canales, pero no es posible leer las conversaciones de chat existentes o agregar respuestas. Además, no se pueden leer ni escribir chats directos entre los usuarios que están fuera del ámbito de un grupo o canal.  Las versiones futuras de la API agregarán capacidades adicionales en esta área.</span><span class="sxs-lookup"><span data-stu-id="26d34-p107">Currently, you can create chat threads in channels, but you cannot read existing chat threads or add replies to them. Also, you cannot read or write direct chats between users that are outside the scope of a team or channel.  Future API releases will add additional capabilities in this area.</span></span>

### <a name="microsoft-teams-users-list-of-joined-teams-preview"></a><span data-ttu-id="26d34-144">Lista de equipos agrupados (versión preliminar) del usuario de Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="26d34-144">Microsoft Teams user's list of joined teams (preview)</span></span>

<span data-ttu-id="26d34-p108">Actualmente, [el listado de los equipos a los que un usuario se ha unido](../api-reference/beta/api/user_list_joinedteams.md) solo funciona con el usuario "yo" para el que el autor de la llamada tiene [permisos delegados](permissions_reference.md).  Las versiones futuras admitirán esta operación para cualquier identificador de usuario que se especifique.</span><span class="sxs-lookup"><span data-stu-id="26d34-p108">Currrently, [listing the teams a user has joined](../api-reference/beta/api/user_list_joinedteams.md) only works for the 'me' user for which the caller has [delegated permissions](permissions_reference.md).  Future releases will support this operation for any specified user ID.</span></span>

### <a name="adding-and-getting-attachments-of-group-posts"></a><span data-ttu-id="26d34-147">Agregar y obtener los datos adjuntos de las publicaciones de grupo</span><span class="sxs-lookup"><span data-stu-id="26d34-147">Adding and getting attachments of group posts</span></span>

<span data-ttu-id="26d34-p109">Actualmente, al [agregar](http://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/api/post_post_attachments) datos adjuntos a las publicaciones de grupo, así como al [enumerar](http://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/api/post_list_attachments) y obtener los datos adjuntos de las publicaciones de grupo, se devuelve el mensaje de error "La solicitud de OData no es compatible". Se ha desarrollado una corrección tanto para la versión `/v1.0` como para la `/beta` y se espera que esté disponible a finales de enero de 2016.</span><span class="sxs-lookup"><span data-stu-id="26d34-p109">[Adding](http://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/api/post_post_attachments) attachments to group posts, [listing](http://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/api/post_list_attachments) and getting attachments of group posts currently return the error message "The OData request is not supported." A fix has been rolled out for both the `/v1.0` and `/beta` versions, and is expected to be widely available by the end of January 2016.</span></span>

### <a name="setting-the-allowexternalsenders-property"></a><span data-ttu-id="26d34-150">Establecer la propiedad allowExternalSenders</span><span class="sxs-lookup"><span data-stu-id="26d34-150">Setting the allowExternalSenders property</span></span>

<span data-ttu-id="26d34-151">Existe en la actualidad un problema que evita el establecimiento de la propiedad **allowExternalSenders** de un grupo en operaciones POST o PATCH, en `/v1.0` y `/beta`.</span><span class="sxs-lookup"><span data-stu-id="26d34-151">There is currently an issue that prevents setting the **allowExternalSenders** property of a group in a POST or PATCH operation, in both `/v1.0` and `/beta`.</span></span>

### <a name="using-delta-query"></a><span data-ttu-id="26d34-152">Usar la consulta de delta</span><span class="sxs-lookup"><span data-stu-id="26d34-152">Using delta query</span></span>

<span data-ttu-id="26d34-153">Para ver los problemas conocidos al usar la consulta de delta, vea la [sección Consulta de delta](#delta-query) de este artículo.</span><span class="sxs-lookup"><span data-stu-id="26d34-153">For known issues using delta query, see the [delta query section](#delta-query) in this article.</span></span>


## <a name="bookings"></a><span data-ttu-id="26d34-154">Bookings</span><span class="sxs-lookup"><span data-stu-id="26d34-154">Bookings</span></span>

### <a name="errorexceededfindcountlimit-when-querying-bookingbusinesses"></a><span data-ttu-id="26d34-155">ErrorExceededFindCountLimit al consultar bookingBusinesses</span><span class="sxs-lookup"><span data-stu-id="26d34-155">ErrorExceededFindCountLimit when querying bookingBusinesses</span></span>

<span data-ttu-id="26d34-156">La obtención de la lista de `bookingBusinesses` genera el siguiente código de error si una organización tiene varias empresas de Bookings y la cuenta que realiza la solicitud no es de administrador:</span><span class="sxs-lookup"><span data-stu-id="26d34-156">Getting the list of `bookingBusinesses` fails with the following error code when an organization has several Bookings businesses and the account making the request is not an administrator:</span></span>

```json
{
  "error": {
    "code": "ErrorExceededFindCountLimit",
    "message":
      "The GetBookingMailboxes request returned too many results. Please specify a query to limit the results.",
  }
}
```

<span data-ttu-id="26d34-157">Como solución alternativa, puede limitar el conjunto de empresas devuelto por la solicitud mediante la inclusión de un parámetro `query`, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="26d34-157">As a workaround, you can limit the set of businesses returned by the request by including a `query` parameter, for example:</span></span>

```
GET https://graph.microsoft.com/beta/bookingBusinesses?query=Fabrikam
```


## <a name="calendars"></a><span data-ttu-id="26d34-158">Calendarios</span><span class="sxs-lookup"><span data-stu-id="26d34-158">Calendars</span></span>

### <a name="adding-and-accessing-ics-based-calendars-in-users-mailbox"></a><span data-ttu-id="26d34-159">Agregar y acceder a calendarios basados en archivos ICS en el buzón del usuario</span><span class="sxs-lookup"><span data-stu-id="26d34-159">Adding and accessing ICS-based calendars in user's mailbox</span></span>

<span data-ttu-id="26d34-160">Actualmente, existe una compatibilidad parcial con un calendario basado en una suscripción a calendarios de Internet (ICS):</span><span class="sxs-lookup"><span data-stu-id="26d34-160">Currently, there is partial support for a calendar based on an Internet Calendar Subscription (ICS):</span></span>

* <span data-ttu-id="26d34-161">Puede agregar un calendario basado en ICS a un buzón de usuario mediante la interfaz de usuario, pero no mediante la API de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="26d34-161">You can add an ICS-based calendar to a user mailbox through the user interface, but not through the Microsoft Graph API.</span></span>
* <span data-ttu-id="26d34-p110">[Enumerar los calendarios del usuario](http://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/api/user_list_calendars) le permite obtener las propiedades **name**, **color** e **id** de cada [calendario](http://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/resources/calendar) en el grupo de calendarios predeterminado del usuario, o en un grupo de calendarios especificado, incluidos los calendarios basados en ICS. No puede almacenar ni acceder a la dirección URL de una ICS en el recurso del calendario.</span><span class="sxs-lookup"><span data-stu-id="26d34-p110">[Listing the user's calendars](http://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/api/user_list_calendars) lets you get the **name**, **color** and **id** properties of each [calendar](http://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/resources/calendar) in the user's default calendar group, or a specified calendar group, including any ICS-based calendars. You cannot store or access the ICS URL in the calendar resource.</span></span>
* <span data-ttu-id="26d34-164">También puede [enumerar los eventos](http://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/api/calendar_list_events) de un calendario basado en ICS.</span><span class="sxs-lookup"><span data-stu-id="26d34-164">You can also [list the events](http://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/api/calendar_list_events) of an ICS-based calendar.</span></span>

### <a name="accessing-a-shared-calendar"></a><span data-ttu-id="26d34-165">Acceso a calendarios compartidos</span><span class="sxs-lookup"><span data-stu-id="26d34-165">Accessing a shared calendar</span></span>

<span data-ttu-id="26d34-166">Al intentar tener acceso a los eventos de un calendario que se ha compartido por otro usuario mediante la siguiente operación:</span><span class="sxs-lookup"><span data-stu-id="26d34-166">When attempting to access events in a calendar that has been shared by another user using the following operation:</span></span>

```http
GET \users('{id}')\calendars('{id}')\events
```

<span data-ttu-id="26d34-p111">Puede obtener HTTP 500 con el código de error `ErrorInternalServerTransientError`. El error se produce porque:</span><span class="sxs-lookup"><span data-stu-id="26d34-p111">You may get HTTP 500 with the error code `ErrorInternalServerTransientError`. The error occurs because:</span></span>

- <span data-ttu-id="26d34-169">Tradicionalmente existen dos maneras de implementar el uso compartido del calendario, que, con fines de diferenciación, se les hace referencia como el enfoque "antiguo" y el enfoque "nuevo".</span><span class="sxs-lookup"><span data-stu-id="26d34-169">Historically, there are two ways that calendar sharing has been implemented, which, for the purpose of differentiating them, are referred to as the "old" approach and "new" approach.</span></span>
- <span data-ttu-id="26d34-170">El enfoque nuevo está disponible en estos momentos para los calendarios de uso compartido con permisos de vista o edición, pero no con permisos delegados.</span><span class="sxs-lookup"><span data-stu-id="26d34-170">The new approach is currently available for sharing calendars with view or edit permissions, but not with delegate permissions.</span></span>
- <span data-ttu-id="26d34-171">Puede usar la API de REST de calendario para ver o editar los calendarios compartidos, solo si los calendarios se han compartido según el enfoque **nuevo**.</span><span class="sxs-lookup"><span data-stu-id="26d34-171">You can use the calendar REST API to view or edit shared calendars only if the calendars were shared using the **new** approach.</span></span>
- <span data-ttu-id="26d34-172">No puede usar la API de REST de calendario para ver o editar dichos calendarios (o sus eventos) si los calendarios se han compartido según el enfoque **antiguo**.</span><span class="sxs-lookup"><span data-stu-id="26d34-172">You cannot use the calendar REST API to view or edit such calendars (or their events) if the calendars were shared using the **old** approach.</span></span>


<span data-ttu-id="26d34-173">Si un calendario se ha compartido con permisos de vista o edición pero con el enfoque antiguo, ahora puede trabajar en el error y actualizar manualmente el calendario de uso compartido para que use el enfoque nuevo.</span><span class="sxs-lookup"><span data-stu-id="26d34-173">If a calendar was shared with view or edit permissions but using the old approach, you can now work around the error and manually upgrade the calendar sharing to use the new approach.</span></span>
<span data-ttu-id="26d34-174">Con el tiempo, Outlook actualizará automáticamente todos los calendarios compartidos para que usen el nuevo enfoque, incluidos los calendarios compartidos con permisos de delegado.</span><span class="sxs-lookup"><span data-stu-id="26d34-174">Over time, Outlook will automatically upgrade all shared calendars to use the new approach, including calendars shared with delegate permissions.</span></span>

<span data-ttu-id="26d34-175">Para actualizar manualmente un calendario compartido para que use el enfoque nuevo, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="26d34-175">To manually upgrade a shared calendar to use the new approach, follow these steps:</span></span>
1.  <span data-ttu-id="26d34-176">El destinatario quita el calendario que se ha compartido anteriormente con ellos.</span><span class="sxs-lookup"><span data-stu-id="26d34-176">The recipient removes the calendar that was previously shared to them.</span></span>
2.  <span data-ttu-id="26d34-177">El propietario del calendario vuelve a compartirlo en Outlook en la web, Outlook en iOS o Outlook en Android.</span><span class="sxs-lookup"><span data-stu-id="26d34-177">The calendar owner re-shares the calendar in Outlook on the web, Outlook on iOS, or Outlook on Android.</span></span>
3.  <span data-ttu-id="26d34-p113">El destinatario vuelve a aceptar el calendario compartido con Outlook en la web. (Será posible usar otros clientes de Outlook pronto).</span><span class="sxs-lookup"><span data-stu-id="26d34-p113">The recipient re-accepts the shared calendar using Outlook on the web. (It will be possible to use other Outlook clients soon.)</span></span>
4.  <span data-ttu-id="26d34-180">El destinatario comprueba que el calendario se ha vuelto a compartir correctamente con el nuevo enfoque al ver el calendario compartido en Outlook en iOS o en Outlook en Android.</span><span class="sxs-lookup"><span data-stu-id="26d34-180">The recipient verifies that the calendar has been re-shared successfully using the new approach by being able to view the shared calendar in Outlook on iOS or Outlook on Android.</span></span>

<span data-ttu-id="26d34-p114">Un calendario compartido con usted mediante el nuevo enfoque aparece como cualquier otro calendario de su buzón. Puede usar la API de REST de calendario para ver o editar eventos en el calendario compartido, como si fuera su propio calendario. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="26d34-p114">A calendar shared with you in the new approach appears as just another calendar in your mailbox. You can use the calendar REST API to view or edit events in the shared calendar, as if it's your own calendar. As an example:</span></span>

```http
GET \me\calendars('{id}')\events
```


## <a name="contacts"></a><span data-ttu-id="26d34-184">Contactos</span><span class="sxs-lookup"><span data-stu-id="26d34-184">Contacts</span></span>

### <a name="organization-contacts-available-in-only-beta"></a><span data-ttu-id="26d34-185">Contactos de organización disponibles solo en beta</span><span class="sxs-lookup"><span data-stu-id="26d34-185">Organization contacts available in only beta</span></span>

<span data-ttu-id="26d34-p115">Solo los contactos personales son compatibles actualmente. Actualmente no se admiten contactos de la organización en `/v1.0`, pero pueden encontrarse en `/beta`.</span><span class="sxs-lookup"><span data-stu-id="26d34-p115">Only personal contacts are currently supported. Organizational contacts are not currently supported in `/v1.0`, but can be found in `/beta`.</span></span>

### <a name="default-contacts-folder"></a><span data-ttu-id="26d34-188">Carpeta de contactos predeterminada</span><span class="sxs-lookup"><span data-stu-id="26d34-188">Default contacts folder</span></span>

<span data-ttu-id="26d34-189">En la versión `/v1.0`, `GET /me/contactFolders` no incluye la carpeta de contactos predeterminada del usuario.</span><span class="sxs-lookup"><span data-stu-id="26d34-189">In the `/v1.0` version, `GET /me/contactFolders` does not include the user's default contacts folder.</span></span>

<span data-ttu-id="26d34-p116">Estará disponible una corrección. Mientras tanto, puede usar la siguiente consulta [enumerar contactos](http://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/api/user_list_contacts) y la propiedad **parentFolderId** como una solución alternativa para obtener el identificador de la carpeta de contactos predeterminada:</span><span class="sxs-lookup"><span data-stu-id="26d34-p116">A fix will be made available. Meanwhile, you can use the following [list contacts](http://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/api/user_list_contacts) query and the **parentFolderId** property as a workaround to get the folder ID of the default contacts folder:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/contacts?$top=1&$select=parentFolderId
```

<span data-ttu-id="26d34-192">En la consulta anterior:</span><span class="sxs-lookup"><span data-stu-id="26d34-192">In the above query:</span></span>

1. <span data-ttu-id="26d34-193">`/me/contacts?$top=1` obtiene las propiedades de un elemento [contact](http://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/resources/contact) de la carpeta de contactos predeterminada.</span><span class="sxs-lookup"><span data-stu-id="26d34-193">`/me/contacts?$top=1` gets the properties of a [contact](http://developer.microsoft.com/es-ES/graph/docs/api-reference/v1.0/resources/contact) in the default contacts folder.</span></span>
2. <span data-ttu-id="26d34-194">Al anexar `&$select=parentFolderId` se devuelve solo la propiedad **parentFolderId** del contacto, que es el identificador de la carpeta de contactos predeterminada.</span><span class="sxs-lookup"><span data-stu-id="26d34-194">Appending `&$select=parentFolderId` returns only the contact's **parentFolderId** property, which is the ID of the default contacts folder.</span></span>


### <a name="accessing-contacts-via-a-contact-folder-in-beta"></a><span data-ttu-id="26d34-195">Acceder a contactos a través de una carpeta de contactos en la versión beta</span><span class="sxs-lookup"><span data-stu-id="26d34-195">Accessing contacts via a contact folder in beta</span></span>

<span data-ttu-id="26d34-196">En la versión `/beta`, existe un problema en la actualidad que impide acceder a un [contacto](../api-reference/beta/resources/contact.md) especificando su carpeta primaria en la dirección de solicitud REST, tal y como se muestra en los dos escenarios siguientes.</span><span class="sxs-lookup"><span data-stu-id="26d34-196">In the `/beta` version, there is currently an issue that prevents accessing a [contact](../api-reference/beta/resources/contact.md) by specifying its parent folder in the REST request URL, as shown in the 2 scenarios below.</span></span>

* <span data-ttu-id="26d34-197">Acceso a un contacto desde un [contactFolder](../api-reference/beta/resources/contactfolder.md) de nivel superior del usuario.</span><span class="sxs-lookup"><span data-stu-id="26d34-197">Accessing a contact from a top level [contactFolder](../api-reference/beta/resources/contactfolder.md) of the user's.</span></span>

```http
GET /me/contactfolders/{id}/contacts/{id}
GET /users/{id | userPrincipalName}/contactfolders/{id}/contacts/{id}
```

* <span data-ttu-id="26d34-p117">Acceso a un contacto contenido en una carpeta secundaria de una **contactFolder**.  En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="26d34-p117">Accessing a contact contained in a child folder of a **contactFolder**.  The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>

```http
GET /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
GET /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```

<span data-ttu-id="26d34-200">Como alternativa, puede simplemente [obtener](../api-reference/beta/api/contact_get.md) el contacto especificando su identificador, tal como se muestra a continuación, ya que GET/contacts en la versión `/beta` se aplica a todos los contactos del buzón de correo del usuario:</span><span class="sxs-lookup"><span data-stu-id="26d34-200">As an alternative, you can simply [get](../api-reference/beta/api/contact_get.md) the contact by specifying its ID as shown below, since GET /contacts in the `/beta` version applies to all the contacts in the user's mailbox:</span></span>

```http
GET /me/contacts/{id}
GET /users/{id | userPrincipalName}/contacts/{id}
```

## <a name="messages"></a><span data-ttu-id="26d34-201">Mensajes</span><span class="sxs-lookup"><span data-stu-id="26d34-201">Messages</span></span>

### <a name="the-comment-parameter-for-creating-a-draft"></a><span data-ttu-id="26d34-202">El parámetro de comentario para crear un borrador</span><span class="sxs-lookup"><span data-stu-id="26d34-202">The comment parameter for creating a draft</span></span>

<span data-ttu-id="26d34-203">El parámetro **comentario** para crear una respuesta o enviar un borrador ([createReply](../api-reference/v1.0/api/message_createreply.md), [createReplyAll](../api-reference/v1.0/api/message_createreplyall.md), [createForward](../api-reference/v1.0/api/message_createforward.md)) no se convierte en parte del cuerpo del borrador del mensaje resultante.</span><span class="sxs-lookup"><span data-stu-id="26d34-203">The **comment** parameter for creating a reply or forward draft ([createReply](../api-reference/v1.0/api/message_createreply.md), [createReplyAll](../api-reference/v1.0/api/message_createreplyall.md), [createForward](../api-reference/v1.0/api/message_createforward.md)) does not become part of the body of the resultant message draft.</span></span>


## <a name="drives-files-and-content-streaming"></a><span data-ttu-id="26d34-204">Unidades, archivos y streaming de contenido</span><span class="sxs-lookup"><span data-stu-id="26d34-204">Drives, files and content streaming</span></span>

* <span data-ttu-id="26d34-205">La primera vez que accede a una unidad personal del usuario a través de Microsoft Graph antes de que el usuario acceda a su sitio personal a través del explorador, se produce una respuesta 401.</span><span class="sxs-lookup"><span data-stu-id="26d34-205">First time access to a user's personal drive through the Microsoft Graph before the user accesses their personal site through a browser leads to a 401 response.</span></span>

## <a name="query-parameter-limitations"></a><span data-ttu-id="26d34-206">Limitaciones del parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="26d34-206">Query parameter limitations</span></span>

* <span data-ttu-id="26d34-207">No se admiten varios espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="26d34-207">Multiple namespaces are not supported.</span></span>
* <span data-ttu-id="26d34-208">Las solicitudes GET en `$ref` y la conversión no se admiten en usuarios, grupos, dispositivos, entidades de seguridad y aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="26d34-208">GETs on `$ref` and casting is not supported on users, groups, devices, service principals and applications.</span></span>
* <span data-ttu-id="26d34-p118">No se admite `@odata.bind`. Esto significa que los desarrolladores no podrán establecer correctamente `Accepted` o `RejectedSenders` en un grupo.</span><span class="sxs-lookup"><span data-stu-id="26d34-p118">`@odata.bind` is not supported.  This means that developers won’t be able to properly set the `Accepted` or `RejectedSenders` on a group.</span></span>
* <span data-ttu-id="26d34-211">`@odata.id` no está presente en las navegaciones de no contención (como los mensajes) cuando se usan metadatos mínimos</span><span class="sxs-lookup"><span data-stu-id="26d34-211">`@odata.id` is not present on non-containment navigations (like messages) when using minimal metadata.</span></span>
* <span data-ttu-id="26d34-212">`$expand`:</span><span class="sxs-lookup"><span data-stu-id="26d34-212"></span></span>
  * <span data-ttu-id="26d34-213">No es compatible con `nextLink`</span><span class="sxs-lookup"><span data-stu-id="26d34-213">No support for `nextLink`</span></span>
  * <span data-ttu-id="26d34-214">No es compatible con más de un nivel de expansión</span><span class="sxs-lookup"><span data-stu-id="26d34-214">No support for more than 1 level of expand</span></span>
  * <span data-ttu-id="26d34-215">No es compatible con parámetros adicionales (`$filter`, `$select`)</span><span class="sxs-lookup"><span data-stu-id="26d34-215">No support with extra parameters (`$filter`, `$select`)</span></span>
* <span data-ttu-id="26d34-216">`$filter`:</span><span class="sxs-lookup"><span data-stu-id="26d34-216"></span></span>
  * <span data-ttu-id="26d34-217">El punto de conexión `/attachments` no admite filtros.</span><span class="sxs-lookup"><span data-stu-id="26d34-217">`/attachments` endpoint does not support filters.</span></span> <span data-ttu-id="26d34-218">Si están presentes, se ignora el parámetro `$filter`.</span><span class="sxs-lookup"><span data-stu-id="26d34-218">If present, the `$filter` parameter is ignored.</span></span>
  * <span data-ttu-id="26d34-219">No se admite el filtrado de cargas de trabajo cruzadas.</span><span class="sxs-lookup"><span data-stu-id="26d34-219">Cross-workload filtering is not supported.</span></span>
* <span data-ttu-id="26d34-220">`$search`:</span><span class="sxs-lookup"><span data-stu-id="26d34-220"></span></span>
  * <span data-ttu-id="26d34-221">La búsqueda de texto completo solo está disponible para un subconjunto de entidades tales como mensajes.</span><span class="sxs-lookup"><span data-stu-id="26d34-221">Full-text search is only available for a subset of entities such as messages.</span></span>
  * <span data-ttu-id="26d34-222">No se admite la búsqueda de cargas de trabajo cruzadas.</span><span class="sxs-lookup"><span data-stu-id="26d34-222">Cross-workload searching is not supported.</span></span>

## <a name="delta-query"></a><span data-ttu-id="26d34-223">Consulta delta</span><span class="sxs-lookup"><span data-stu-id="26d34-223">Delta query</span></span>

* <span data-ttu-id="26d34-224">El contexto OData a veces se devuelve de forma incorrecta cuando se realiza el seguimiento de cambios en las relaciones.</span><span class="sxs-lookup"><span data-stu-id="26d34-224">OData context is sometimes returned incorrectly when tracking changes to relationships.</span></span>
* <span data-ttu-id="26d34-225">Las extensiones de esquema (heredadas) no se devuelven con la instrucción $select, pero se devuelven sin $select.</span><span class="sxs-lookup"><span data-stu-id="26d34-225">Schema extensions (legacy) are not returned with $select statement, but are returned without $select.</span></span>
* <span data-ttu-id="26d34-226">Los clientes no pueden controlar los cambios para abrir las extensiones o las extensiones de esquema registradas.</span><span class="sxs-lookup"><span data-stu-id="26d34-226">Clients cannot track changes to open extensions or registered schema extensions.</span></span>

## <a name="application-and-serviceprincipal-api-changes"></a><span data-ttu-id="26d34-227">Cambios en la API servicePrincipal y en aplicaciones</span><span class="sxs-lookup"><span data-stu-id="26d34-227">Application and servicePrincipal API changes</span></span>

<span data-ttu-id="26d34-p120">Existen cambios actuales en las entidades [application](../api-reference/beta/resources/application.md) y [servicePrincipal](../api-reference/beta/resources/serviceprincipal.md) en el desarrollo. A continuación se muestra un resumen de las limitaciones actuales y las características de la API en el desarrollo.</span><span class="sxs-lookup"><span data-stu-id="26d34-p120">There are changes to the [application](../api-reference/beta/resources/application.md) and [servicePrincipal](../api-reference/beta/resources/serviceprincipal.md) entities currently in development. The following is a summary of current limitations and in-development API features.</span></span>

<span data-ttu-id="26d34-230">Limitaciones actuales:</span><span class="sxs-lookup"><span data-stu-id="26d34-230">Current limitations:</span></span>

* <span data-ttu-id="26d34-231">Algunas propiedades de aplicaciones (como appRoles y addIns) no estarán disponibles hasta que se completen todos los cambios.</span><span class="sxs-lookup"><span data-stu-id="26d34-231">Some application properties (such as appRoles and addIns) will not be available until all changes are completed.</span></span>
* <span data-ttu-id="26d34-232">Solo pueden registrarse las aplicaciones multiinquilino.</span><span class="sxs-lookup"><span data-stu-id="26d34-232">Only multi-tenant apps can be registered.</span></span>
* <span data-ttu-id="26d34-233">La actualización de aplicaciones está restringida a las aplicaciones que se han registrado después de la actualización de la versión beta inicial.</span><span class="sxs-lookup"><span data-stu-id="26d34-233">Updating apps is restricted to apps registered after the initial beta update.</span></span>
* <span data-ttu-id="26d34-234">Los usuarios de Azure Active Directory pueden registrar aplicaciones y agregar propietarios adicionales.</span><span class="sxs-lookup"><span data-stu-id="26d34-234">Azure Active Directory users can register apps and add additional owners.</span></span>
* <span data-ttu-id="26d34-235">Compatibilidad con los protocolos OpenID Connect y OAuth.</span><span class="sxs-lookup"><span data-stu-id="26d34-235">Support for OpenID Connect and OAuth protocols.</span></span>
* <span data-ttu-id="26d34-236">Error en las asignaciones de directivas en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="26d34-236">Policy assignments to an application fail.</span></span>
* <span data-ttu-id="26d34-237">Las operaciones de ownedObjects que necesiten appId producirán un error (Por ejemplo, users/{id|userPrincipalName}/ownedObjects/{id}/...).</span><span class="sxs-lookup"><span data-stu-id="26d34-237">Operations on ownedObjects that require appId fail (For example, users/{id|userPrincipalName}/ownedObjects/{id}/...).</span></span>

<span data-ttu-id="26d34-238">En desarrollo:</span><span class="sxs-lookup"><span data-stu-id="26d34-238">In development:</span></span>

* <span data-ttu-id="26d34-239">Capacidad de registrar aplicaciones de inquilino único.</span><span class="sxs-lookup"><span data-stu-id="26d34-239">Ability to register single tenant apps.</span></span>
* <span data-ttu-id="26d34-240">Actualizaciones de servicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="26d34-240">Updates to servicePrincipal.</span></span>
* <span data-ttu-id="26d34-241">Migración de aplicaciones de Azure AD existentes en un modelo actualizado.</span><span class="sxs-lookup"><span data-stu-id="26d34-241">Migration of existing Azure AD apps to updated model.</span></span>
* <span data-ttu-id="26d34-242">Compatibilidad para appRoles, clientes autorizados previamente, notificaciones opcionales, notificaciones de pertenencia a grupos y personalización de marca.</span><span class="sxs-lookup"><span data-stu-id="26d34-242">Support for appRoles, pre-authorized clients, optional claims, group membership claims, and branding</span></span>
* <span data-ttu-id="26d34-243">Los usuarios de cuentas de Microsoft (MSA) pueden registrar aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="26d34-243">Microsoft account (MSA) users can register apps.</span></span>
* <span data-ttu-id="26d34-244">Compatibilidad con los protocolos SAML y WsFed.</span><span class="sxs-lookup"><span data-stu-id="26d34-244">Support for SAML and WsFed protocols.</span></span>

## <a name="extensions"></a><span data-ttu-id="26d34-245">Extensiones</span><span class="sxs-lookup"><span data-stu-id="26d34-245">Extensions</span></span>

### <a name="change-tracking-is-not-supported"></a><span data-ttu-id="26d34-246">No se admite el seguimiento de cambios</span><span class="sxs-lookup"><span data-stu-id="26d34-246">Change tracking is not supported</span></span>

<span data-ttu-id="26d34-247">El seguimiento de cambios (consulta delta) aún no se admite para las propiedades de extensiones abiertas o de esquema.</span><span class="sxs-lookup"><span data-stu-id="26d34-247">Change tracking (delta query) is not supported for open or schema extension properties.</span></span>

### <a name="creating-a-resource-and-open-extension-at-the-same-time"></a><span data-ttu-id="26d34-248">Crear un recurso y una extensión abierta al mismo tiempo</span><span class="sxs-lookup"><span data-stu-id="26d34-248">Creating a resource and open extension at the same time</span></span>

<span data-ttu-id="26d34-p121">No se puede especificar una extensión abierta a la vez que se crea una instancia de **administrativeUnit**, **device**, **group**, **organization** o **user**. Debe crear primero la instancia y después especificar los datos de extensión abierta en una solicitud ``POST`` posterior en esa instancia.</span><span class="sxs-lookup"><span data-stu-id="26d34-p121">You cannot specify an open extension at the same time you create an instance of **administrativeUnit**, **device**, **group**, **organization** or **user**. You must first create the instance and then specify the open extension data in a subsequent ``POST`` request on that instance.</span></span>

### <a name="creating-a-resource-instance-and-adding-schema-extension-data-at-the-same-time"></a><span data-ttu-id="26d34-251">Creación de una instancia de recurso y adición de datos de extensión de esquema al mismo tiempo</span><span class="sxs-lookup"><span data-stu-id="26d34-251">Creating a resource instance and adding schema extension data at the same time</span></span>

<span data-ttu-id="26d34-252">No se puede especificar una extensión de esquema en la misma operación de creación de una instancia de **contacto**, **evento**, **mensaje** o **publicación**.</span><span class="sxs-lookup"><span data-stu-id="26d34-252">You cannot specify a schema extension in the same operation as creating an instance of **contact**, **event**, **message**, or **post**.</span></span>
<span data-ttu-id="26d34-253">Debe crear primero la instancia de recurso y, a continuación, aplicar una revisión `PATCH` a esa instancia para agregar una extensión de esquema y datos personalizados.</span><span class="sxs-lookup"><span data-stu-id="26d34-253">You must first create the resource instance and then do a `PATCH` to that instance to add a schema extension and custom data.</span></span>

### <a name="limit-of-100-schema-extension-property-values-allowed-per-resource-instance"></a><span data-ttu-id="26d34-254">Límite de 100 valores de propiedad de extensión de esquema permitido por cada instancia del recurso</span><span class="sxs-lookup"><span data-stu-id="26d34-254">Limit of 100 schema extension property values allowed per resource instance</span></span>

<span data-ttu-id="26d34-255">En la actualidad, los recursos de directorio, como **dispositivos**, **grupos** y **usuarios**, limitan a 100 el número total de valores de propiedad de extensión de esquema que pueden establecerse en un recurso.</span><span class="sxs-lookup"><span data-stu-id="26d34-255">Directory resources, such as **device**, **group** and **user**, currently limit the total number of schema extension property values that can be set on a resource instance, to 100.</span></span>

### <a name="filtering-on-schema-extension-properties-not-supported-on-all-entity-types"></a><span data-ttu-id="26d34-256">No todos los tipos de entidad admiten el filtrado por propiedades de extensión de esquema</span><span class="sxs-lookup"><span data-stu-id="26d34-256">Filtering on schema extension properties not supported on all entity types</span></span>

<span data-ttu-id="26d34-257">Los tipos de entidad de Outlook no admiten el filtrado por propiedades de extensión de esquema (con la expresión `$filter`): **contact**, **event**, **message**o **post**.</span><span class="sxs-lookup"><span data-stu-id="26d34-257">Filtering on schema extension properties (using the `$filter` expresssion) is not supported for Outlook entity types - **contact**, **event**, **message**, or **post**.</span></span>

## <a name="json-batching"></a><span data-ttu-id="26d34-258">Procesamiento por lotes JSON</span><span class="sxs-lookup"><span data-stu-id="26d34-258">JSON Batching</span></span>

### <a name="no-nested-batch"></a><span data-ttu-id="26d34-259">No hay ningún lote anidado</span><span class="sxs-lookup"><span data-stu-id="26d34-259">No nested batch</span></span>

<span data-ttu-id="26d34-260">Las solicitudes por lotes JSON no deben contener ninguna solicitud de proceso por lotes anidados.</span><span class="sxs-lookup"><span data-stu-id="26d34-260">JSON batch requests must not contain any nested batch requests.</span></span>

### <a name="all-individual-requests-must-be-synchronous"></a><span data-ttu-id="26d34-261">Todas las solicitudes individuales deben ser sincrónicas</span><span class="sxs-lookup"><span data-stu-id="26d34-261">All individual requests must be synchronous</span></span>

<span data-ttu-id="26d34-p123">Todas las solicitudes de contenido en una solicitud por lotes se deben ejecutar de forma sincrónica. Si está presente, se omitirá la preferencia `respond-async`.</span><span class="sxs-lookup"><span data-stu-id="26d34-p123">All requests contained in a batch request must be executed synchronously. If present, the `respond-async` preference will be ignored.</span></span>

### <a name="no-transactions"></a><span data-ttu-id="26d34-264">No hay transacciones</span><span class="sxs-lookup"><span data-stu-id="26d34-264">No transactions</span></span>

<span data-ttu-id="26d34-p124">Microsoft Graph no admite actualmente el procesamiento transaccional de solicitudes individuales. Se omitirá la propiedad `atomicityGroup` en solicitudes individuales.</span><span class="sxs-lookup"><span data-stu-id="26d34-p124">Microsoft Graph does not currently support transactional processing of individual requests. The `atomicityGroup` property on individual requests will be ignored.</span></span>

### <a name="uris-must-be-relative"></a><span data-ttu-id="26d34-267">Los URI deben ser relativos</span><span class="sxs-lookup"><span data-stu-id="26d34-267">URIs must be relative</span></span>

<span data-ttu-id="26d34-p125">Especifique siempre los identificadores URI relativos en solicitudes por lotes. Microsoft Graph crea estas direcciones URL absolutas mediante el punto de conexión de la versión que está incluido en la URL por lotes.</span><span class="sxs-lookup"><span data-stu-id="26d34-p125">Always specify relative URIs in batch requests. Microsoft Graph then makes these URLs absolute by using the version endpoint included in the batch URL.</span></span>

### <a name="limit-on-batch-size"></a><span data-ttu-id="26d34-270">Límite de tamaño por lotes</span><span class="sxs-lookup"><span data-stu-id="26d34-270">Limit on batch size</span></span>

<span data-ttu-id="26d34-271">Las solicitudes por lotes JSON están limitadas actualmente a veinte solicitudes individuales.</span><span class="sxs-lookup"><span data-stu-id="26d34-271">JSON batch requests are currently limited to 20 individual requests.</span></span>

### <a name="simplified-dependencies"></a><span data-ttu-id="26d34-272">Dependencias simplificadas</span><span class="sxs-lookup"><span data-stu-id="26d34-272">Simplified dependencies</span></span>

<span data-ttu-id="26d34-p126">Las solicitudes individuales pueden depender de otras solicitudes individuales. Actualmente, las solicitudes solo pueden depender de una sola solicitud y deben seguir uno de estos tres modelos:</span><span class="sxs-lookup"><span data-stu-id="26d34-p126">Individual requests can depend on other individual requests. Currently, requests can only depend on a single other request, and must follow one of these three patterns:</span></span>

1. <span data-ttu-id="26d34-275">En paralelo: ninguna solicitud individual indica una dependencia de la propiedad `dependsOn`.</span><span class="sxs-lookup"><span data-stu-id="26d34-275">Parallel - no individual request states a dependency in the `dependsOn` property.</span></span>
2. <span data-ttu-id="26d34-276">En serie: todas las solicitudes individuales dependen de la anterior solicitud individual.</span><span class="sxs-lookup"><span data-stu-id="26d34-276">Serial - all individual requests depend on the previous individual request.</span></span>
3. <span data-ttu-id="26d34-277">Igual: todas las solicitudes individuales que indican una dependencia de la propiedad `dependsOn`, indican la misma dependencia.</span><span class="sxs-lookup"><span data-stu-id="26d34-277">Same - all individual requests that state a dependency in the `dependsOn` property, state the same dependency.</span></span>

<span data-ttu-id="26d34-278">A medida que madure el procesamiento por lotes JSON, se irán quitando estas limitaciones.</span><span class="sxs-lookup"><span data-stu-id="26d34-278">As JSON batching matures, these limitations will be removed.</span></span>

## <a name="cloud-solution-provider-apps"></a><span data-ttu-id="26d34-279">Aplicaciones del Proveedor de soluciones en la nube</span><span class="sxs-lookup"><span data-stu-id="26d34-279">Cloud Solution Provider apps</span></span>

### <a name="csp-apps-must-use-azure-ad-endpoint"></a><span data-ttu-id="26d34-280">Las aplicaciones de CSP deben usar el punto de conexión de Azure AD</span><span class="sxs-lookup"><span data-stu-id="26d34-280">CSP apps must use Azure AD endpoint</span></span>

<span data-ttu-id="26d34-p127">Las aplicaciones del Proveedor soluciones en la nube (CSP) deben adquirir tokens de los puntos de conexión de Azure AD (v1) para llamar correctamente a Microsoft Graph en sus clientes gestionados por el asociado. Actualmente, no se admite adquirir un token a través del punto de conexión más reciente de Azure AD v2.0.</span><span class="sxs-lookup"><span data-stu-id="26d34-p127">Cloud solution provider (CSP) apps must acquire tokens from the Azure AD (v1) endpoints to successfully call Microsoft Graph in their partner-managed customers. Currently, acquiring a token through the newer Azure AD v2.0 endpoint is not supported.</span></span>

### <a name="pre-consent-for-csp-apps-doesnt-work-in-some-customer-tenants"></a><span data-ttu-id="26d34-283">El consentimiento previo de las aplicaciones de CSP no funciona en algunos inquilinos de cliente</span><span class="sxs-lookup"><span data-stu-id="26d34-283">Pre-consent for CSP apps doesn't work in some customer tenants</span></span>

<span data-ttu-id="26d34-284">En determinadas circunstancias, el consentimiento previo de las aplicaciones de CSP puede que no funcione para algunos de los inquilinos de cliente.</span><span class="sxs-lookup"><span data-stu-id="26d34-284">Under certain circumstances, pre-consent for CSP apps may not work for some of your customer tenants.</span></span>

- <span data-ttu-id="26d34-285">Para las aplicaciones que usan permisos delegados, al usar la aplicación por primera vez con un nuevo inquilino de cliente puede recibir este error después del inicio de sesión: `AADSTS50000: There was an error issuing a token`.</span><span class="sxs-lookup"><span data-stu-id="26d34-285">For apps using delegated permissions, when using the app for the first time with a new customer tenant you might receive this error after sign-in: `AADSTS50000: There was an error issuing a token`.</span></span>
- <span data-ttu-id="26d34-286">Para las aplicaciones que usan permisos de aplicación, su aplicación puede adquirir un token, pero obtiene inesperadamente un mensaje de acceso denegado al llamar a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="26d34-286">For apps using application permissions, your app can acquire a token, but unexpectedly gets an access denied message when calling Microsoft Graph.</span></span>

<span data-ttu-id="26d34-287">Estamos trabajando en solucionar este problema tan pronto como sea posible para que el consentimiento previo funcione en todos los inquilinos de cliente.</span><span class="sxs-lookup"><span data-stu-id="26d34-287">We are working to fix this issue as soon as possible, so that pre-consent will work for all your customer tenants.</span></span>

<span data-ttu-id="26d34-288">Mientras tanto, para desbloquear el desarrollo y las pruebas, puede usar la siguiente solución alternativa.</span><span class="sxs-lookup"><span data-stu-id="26d34-288">In the meantime, to unblock development and testing you can use the following workaround.</span></span>

><span data-ttu-id="26d34-p128">**NOTA:** Esta no es una solución permanente y solo está prevista para desbloquear el desarrollo.  Esta solución alternativa no será necesaria una vez que se solucione el problema mencionado anteriormente.  Esta solución alternativa no necesita deshacerse una vez que se implemente la corrección.</span><span class="sxs-lookup"><span data-stu-id="26d34-p128">**NOTE:** This is not a permanent solution and is only intended to unblock development.  This workaround will not be required once the aforementioned issue is fixed.  This workaround does not need to be undone once the fix is in place.</span></span>

1. <span data-ttu-id="26d34-p129">Abra una sesión de PowerShell de Azure AD v2 y conéctese al inquilino `customer`. Para ello, escriba sus credenciales de administrador en la ventana de inicio de sesión. Puede descargar e instalar PowerShell V2 para Azure AD desde [aquí](https://www.powershellgallery.com/packages/AzureAD).</span><span class="sxs-lookup"><span data-stu-id="26d34-p129">Open an Azure AD v2 PowerShell session and connect to your `customer` tenant by entering your admin credentials into the sign-in window. You can download and install Azure AD PowerShell V2 from [here](https://www.powershellgallery.com/packages/AzureAD).</span></span>

    ```PowerShell
    Connect-AzureAd -TenantId {customerTenantIdOrDomainName}
    ```

2. <span data-ttu-id="26d34-294">Cree la entidad de servicio de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="26d34-294">Create the Microsoft Graph service principal.</span></span>

    ```PowerShell
    New-AzureADServicePrincipal -AppId 00000003-0000-0000-c000-000000000000
    ```

## <a name="functionality-available-only-in-office-365-rest-or-azure-ad-graph-apis"></a><span data-ttu-id="26d34-295">Esta función solo está disponible en las API de REST de Office 365 o las API de Graph de Azure AD</span><span class="sxs-lookup"><span data-stu-id="26d34-295">Functionality available only in Office 365 REST or Azure AD Graph APIs</span></span>

<span data-ttu-id="26d34-p130">Algunas funciones todavía no están disponibles en Microsoft Graph. Si no ve la funcionalidad que busca, puede usar las [API de REST de Office 365](https://msdn.microsoft.com/es-ES/office/office365/api/api-catalog) específicas del punto de conexión. Para Azure Active Directory, consulte la publicación del blog [Microsoft Graph o Azure AD Graph](https://dev.office.com/blogs/microsoft-graph-or-azure-ad-graph) sobre las características que solo están disponibles a través de la API de Azure AD Graph.</span><span class="sxs-lookup"><span data-stu-id="26d34-p130">Some functionality is not yet available in Microsoft Graph. If you don't see the functionality you're looking for, you can use the endpoint-specific [Office 365 REST APIs](https://msdn.microsoft.com/es-ES/office/office365/api/api-catalog). For Azure Active Directory, please refer to the [Microsoft Graph or Azure AD Graph](https://dev.office.com/blogs/microsoft-graph-or-azure-ad-graph) blog post on the features that are only available through Azure AD Graph API.</span></span>

## <a name="feedback"></a><span data-ttu-id="26d34-299">Comentarios</span><span class="sxs-lookup"><span data-stu-id="26d34-299">Feedback</span></span>

> <span data-ttu-id="26d34-p131">Su opinión es importante para nosotros. Conecte con nosotros en [Desbordamiento de pila](http://stackoverflow.com/questions/tagged/microsoftgraph).</span><span class="sxs-lookup"><span data-stu-id="26d34-p131">Your feedback is important to us. Connect with us on [Stack Overflow](http://stackoverflow.com/questions/tagged/microsoftgraph).</span></span>
