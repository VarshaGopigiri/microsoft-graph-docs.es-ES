# <a name="get-message"></a><span data-ttu-id="a5761-101">Obtener mensaje</span><span class="sxs-lookup"><span data-stu-id="a5761-101">Get message</span></span>

<span data-ttu-id="a5761-102">Recupere las propiedades y las relaciones de un objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="a5761-102">Retrieve the properties and relationships of a [message](../resources/message.md) object.</span></span>

<span data-ttu-id="a5761-103">Dado que el recurso **message** admite [extensiones](../../../concepts/extensibility_overview.md), también puede utilizar la operación `GET` para obtener propiedades personalizadas y datos de extensión en una instancia **message**.</span><span class="sxs-lookup"><span data-stu-id="a5761-103">Since the **message** resource supports [extensions](../../../concepts/extensibility_overview.md), you can also use the `GET` operation to get custom properties and extension data in a **message** instance.</span></span>

<span data-ttu-id="a5761-104">Actualmente, esta operación devuelve los cuerpos de los mensajes solo en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="a5761-104">Currently, this operation returns message bodies in only HTML format.</span></span>


### <a name="get-messages-in-another-users-message-folder"></a><span data-ttu-id="a5761-105">Obtener mensajes en la carpeta de mensajes de otro usuario</span><span class="sxs-lookup"><span data-stu-id="a5761-105">Get messages in another user's message folder</span></span>

<span data-ttu-id="a5761-106">Si dispone de permisos de la aplicación o si tiene los [permisos](#permissions) delegados apropiados de un usuario, es posible obtener los contactos de la carpeta de contactos de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="a5761-106">If you have application permissions, or if you have the appropriate delegated [permissions](#permissions) from one user, it's possible to get messages from another user's message folder.</span></span> <span data-ttu-id="a5761-107">Esta sección se centra en escenarios que implican permisos delegados.</span><span class="sxs-lookup"><span data-stu-id="a5761-107">This section focuses on scenarios that involve delegated permissions.</span></span>

<span data-ttu-id="a5761-108">Por ejemplo, su aplicación ha adquirido permisos delegados del usuario John.</span><span class="sxs-lookup"><span data-stu-id="a5761-108">For example, your app has acquired delegated permissions from the user, John.</span></span> <span data-ttu-id="a5761-109">Suponga que otro usuario, Garth, ha compartido una carpeta de mensajes con John.</span><span class="sxs-lookup"><span data-stu-id="a5761-109">Suppose another user, Garth, has shared a message folder with John.</span></span> <span data-ttu-id="a5761-110">Puede obtener un mensaje de dicha carpeta compartida especificando el identificador de usuario de Garth (o su nombre principal de usuario) en la consulta de ejemplo que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="a5761-110">You can get a message in that shared folder by specifying Garth’s user ID (or user principal name) in the example query shown below.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/{Garth-id | Garth-userPrincipalName}/messages/{id}
```

<span data-ttu-id="a5761-111">Esta capacidad se aplica a todas las operaciones de mensajes GET compatibles para un usuario individual, como se muestra en la sección [solicitud HTTP](#http-request) a continuación.</span><span class="sxs-lookup"><span data-stu-id="a5761-111">This capability applies to all the supported GET messages operations for an individual user, as listed in the [HTTP request](#http-request) section below.</span></span> <span data-ttu-id="a5761-112">También se aplica si Garth ha delegado todo el buzón en John.</span><span class="sxs-lookup"><span data-stu-id="a5761-112">It also applies if Garth has delegated his entire mailbox to John.</span></span>

<span data-ttu-id="a5761-113">Si Garth no ha compartido su carpeta de mensajes con John ni ha delegado su buzón en John, especificar el identificador de usuario del Garth o el nombre principal de usuario en esas operaciones GET devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="a5761-113">If Garth has not shared his message folder with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> <span data-ttu-id="a5761-114">En tales casos, especificar un identificador de usuario o un nombre principal de usuario solo funciona para obtener un mensaje de las carpetas de mensajes del usuario que ha iniciado sesión, y la consulta es equivalente a usar el método abreviado de /me:</span><span class="sxs-lookup"><span data-stu-id="a5761-114">In such cases, specifying a user ID or user principal name only works for getting a message in the signed-in user’s own message folders, and the query is equivalent to using the /me shortcut:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/messages/{id}
```

<span data-ttu-id="a5761-115">Esta capacidad solo está disponible en las operaciones GET de:</span><span class="sxs-lookup"><span data-stu-id="a5761-115">This capability is available in only GET operations of:</span></span>

- <span data-ttu-id="a5761-116">Uso compartido de carpetas de contactos, calendarios y carpetas de mensajes</span><span class="sxs-lookup"><span data-stu-id="a5761-116">Shared contact folders, calendars, and message folders</span></span> 
- <span data-ttu-id="a5761-117">Contactos, eventos y mensajes en carpetas compartidas</span><span class="sxs-lookup"><span data-stu-id="a5761-117">Contacts, events, and messages in shared folders</span></span>
- <span data-ttu-id="a5761-118">Los recursos anteriores en buzones delegados</span><span class="sxs-lookup"><span data-stu-id="a5761-118">The above resources in delegated mailboxes</span></span>

<span data-ttu-id="a5761-119">Esta capacidad no está disponible en otras operaciones de contactos, eventos, mensajes y sus carpetas.</span><span class="sxs-lookup"><span data-stu-id="a5761-119">This capability is not available in other operations for contacts, events, messages, and their folders.</span></span>


## <a name="permissions"></a><span data-ttu-id="a5761-120">Permisos</span><span class="sxs-lookup"><span data-stu-id="a5761-120">Permissions</span></span>
<span data-ttu-id="a5761-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a5761-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a5761-123">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a5761-123">Permission type</span></span>      | <span data-ttu-id="a5761-124">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a5761-124">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a5761-125">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a5761-125">Delegated (work or school account)</span></span> | <span data-ttu-id="a5761-126">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a5761-126">Mail.Read</span></span>    |
|<span data-ttu-id="a5761-127">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a5761-127">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a5761-128">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a5761-128">Mail.Read</span></span>    |
|<span data-ttu-id="a5761-129">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a5761-129">Application</span></span> | <span data-ttu-id="a5761-130">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a5761-130">Mail.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="a5761-131">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a5761-131">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/messages/{id}
GET /users/{id | userPrincipalName}/messages/{id}
GET /me/mailFolders/{id}/messages/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a5761-132">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a5761-132">Optional query parameters</span></span>
<span data-ttu-id="a5761-133">Este método admite los [parámetros de consulta de OData]((http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters)) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5761-133">This method supports the [OData Query Parameters]((http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters)) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="a5761-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a5761-134">Request headers</span></span>
| <span data-ttu-id="a5761-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="a5761-135">Name</span></span>       | <span data-ttu-id="a5761-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5761-136">Type</span></span> | <span data-ttu-id="a5761-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5761-137">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="a5761-138">Authorization</span><span class="sxs-lookup"><span data-stu-id="a5761-138">Authorization</span></span>  | <span data-ttu-id="a5761-139">string</span><span class="sxs-lookup"><span data-stu-id="a5761-139">string</span></span>  | <span data-ttu-id="a5761-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a5761-p106">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a5761-142">Prefer: outlook.body-content-type</span><span class="sxs-lookup"><span data-stu-id="a5761-142">Prefer: outlook.body-content-type</span></span> | <span data-ttu-id="a5761-143">string</span><span class="sxs-lookup"><span data-stu-id="a5761-143">string</span></span> | <span data-ttu-id="a5761-144">Formato de las propiedades **body** y **uniqueBody** que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="a5761-144">The format of the **body** and **uniqueBody** properties to be returned in.</span></span> <span data-ttu-id="a5761-145">Los valores pueden ser "text" o "html".</span><span class="sxs-lookup"><span data-stu-id="a5761-145">Values can be "text" or "html".</span></span> <span data-ttu-id="a5761-146">Se devuelve un encabezado `Preference-Applied` como confirmación si se especifica este encabezado `Prefer`.</span><span class="sxs-lookup"><span data-stu-id="a5761-146">A `Preference-Applied` header is returned as confirmation if this `Prefer` header is specified.</span></span> <span data-ttu-id="a5761-147">Si no se especifica el encabezado, las propiedades **body** y **uniqueBody** se devuelven en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="a5761-147">If the header is not specified, the **body** and **uniqueBody** properties are returned in HTML format.</span></span> <span data-ttu-id="a5761-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a5761-148">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a5761-149">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a5761-149">Request body</span></span>
<span data-ttu-id="a5761-150">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a5761-150">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a5761-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5761-151">Response</span></span>

<span data-ttu-id="a5761-152">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5761-152">If successful, this method returns a `200 OK` response code and [message](../resources/message.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a5761-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a5761-153">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a5761-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a5761-154">Request</span></span>
<span data-ttu-id="a5761-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a5761-155">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_message"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/{id}
```
##### <a name="response"></a><span data-ttu-id="a5761-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5761-156">Response</span></span>
<span data-ttu-id="a5761-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a5761-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 248

{
  "receivedDateTime": "datetime-value",
  "sentDateTime": "datetime-value",
  "hasAttachments": true,
  "subject": "subject-value",
  "body": {
    "contentType": "html",
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value"
}
```

## <a name="see-also"></a><span data-ttu-id="a5761-160">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a5761-160">See also</span></span>

- [<span data-ttu-id="a5761-161">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="a5761-161">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="a5761-162">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="a5761-162">Add custom data to users using open extensions (preview)</span></span>](../../../concepts/extensibility_open_users.md)
<!--
- [Add custom data to groups using schema extensions (preview)](../../../concepts/extensibility_schema_groups.md)
-->


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get message",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
