# <a name="list-messages"></a><span data-ttu-id="77a9b-101">Enumerar mensajes</span><span class="sxs-lookup"><span data-stu-id="77a9b-101">List messages</span></span>

<span data-ttu-id="77a9b-102">Obtenga los mensajes del buzón del usuario que ha iniciado sesión (incluidas las carpetas Elementos eliminados y Otros correos).</span><span class="sxs-lookup"><span data-stu-id="77a9b-102">Get the messages in the signed-in user's mailbox (including the Deleted Items and Clutter folders).</span></span>

<span data-ttu-id="77a9b-103">Actualmente, esta operación devuelve los cuerpos de los mensajes solo en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="77a9b-103">Currently, this operation returns message bodies in only HTML format.</span></span>


### <a name="get-messages-in-another-users-message-folder"></a><span data-ttu-id="77a9b-104">Obtener mensajes en la carpeta de mensajes de otro usuario</span><span class="sxs-lookup"><span data-stu-id="77a9b-104">Get messages in another user's message folder</span></span>

<span data-ttu-id="77a9b-105">Si dispone de permisos de la aplicación o si tiene los [permisos](#permissions) delegados apropiados de un usuario, es posible obtener los contactos de la carpeta de contactos de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="77a9b-105">If you have application permissions, or if you have the appropriate delegated [permissions](#permissions) from one user, it's possible to get messages from another user's message folder.</span></span> <span data-ttu-id="77a9b-106">Esta sección se centra en escenarios que implican permisos delegados.</span><span class="sxs-lookup"><span data-stu-id="77a9b-106">This section focuses on scenarios that involve delegated permissions.</span></span>

<span data-ttu-id="77a9b-107">Por ejemplo, su aplicación ha adquirido permisos delegados del usuario John.</span><span class="sxs-lookup"><span data-stu-id="77a9b-107">For example, your app has acquired delegated permissions from the user, John.</span></span> <span data-ttu-id="77a9b-108">Suponga que otro usuario, Garth, ha compartido una carpeta de mensajes con John.</span><span class="sxs-lookup"><span data-stu-id="77a9b-108">Suppose another user, Garth, has shared a message folder with John.</span></span> <span data-ttu-id="77a9b-109">Puede obtener los mensajes de dicha carpeta compartida especificando el identificador de usuario de Garth (o su nombre principal de usuario) en la consulta de ejemplo que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="77a9b-109">You can get the messages in that shared folder by specifying Garth’s user ID (or user principal name) in the example query shown below.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/{Garth-id | Garth-userPrincipalName}/messages
```

<span data-ttu-id="77a9b-110">Esta capacidad se aplica a todas las operaciones de mensajes GET compatibles para un usuario individual, como se muestra en la sección [solicitud HTTP](#http-request) a continuación.</span><span class="sxs-lookup"><span data-stu-id="77a9b-110">This capability applies to all the supported GET messages operations for an individual user, as listed in the [HTTP request](#http-request) section below.</span></span> <span data-ttu-id="77a9b-111">También se aplica si Garth ha delegado todo el buzón en John.</span><span class="sxs-lookup"><span data-stu-id="77a9b-111">It also applies if Garth has delegated his entire mailbox to John.</span></span>

<span data-ttu-id="77a9b-112">Si Garth no ha compartido su carpeta de mensajes con John ni ha delegado su buzón en John, especificar el identificador de usuario del Garth o el nombre principal de usuario en esas operaciones GET devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="77a9b-112">If Garth has not shared his message folder with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> <span data-ttu-id="77a9b-113">En tales casos, especificar un identificador de usuario o un nombre principal de usuario solo funciona para obtener los mensajes de las carpetas de mensajes del usuario que ha iniciado sesión, y la consulta es equivalente a usar el método abreviado de /me:</span><span class="sxs-lookup"><span data-stu-id="77a9b-113">In such cases, specifying a user ID or user principal name only works for getting messages in the signed-in user’s own message folders, and the query is equivalent to using the /me shortcut:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/messages
```

<span data-ttu-id="77a9b-114">Esta capacidad solo está disponible en las operaciones GET de:</span><span class="sxs-lookup"><span data-stu-id="77a9b-114">This capability is available in only GET operations of:</span></span>

- <span data-ttu-id="77a9b-115">Uso compartido de carpetas de contactos, calendarios y carpetas de mensajes</span><span class="sxs-lookup"><span data-stu-id="77a9b-115">Shared contact folders, calendars, and message folders</span></span> 
- <span data-ttu-id="77a9b-116">Contactos, eventos y mensajes en carpetas compartidas</span><span class="sxs-lookup"><span data-stu-id="77a9b-116">Contacts, events, and messages in shared folders</span></span>
- <span data-ttu-id="77a9b-117">Los recursos anteriores en buzones delegados</span><span class="sxs-lookup"><span data-stu-id="77a9b-117">The above resources in delegated mailboxes</span></span>

<span data-ttu-id="77a9b-118">Esta capacidad no está disponible en otras operaciones de contactos, eventos, mensajes y sus carpetas.</span><span class="sxs-lookup"><span data-stu-id="77a9b-118">This capability is not available in other operations for contacts, events, messages, and their folders.</span></span>


## <a name="permissions"></a><span data-ttu-id="77a9b-119">Permisos</span><span class="sxs-lookup"><span data-stu-id="77a9b-119">Permissions</span></span>
<span data-ttu-id="77a9b-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="77a9b-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="77a9b-122">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="77a9b-122">Permission type</span></span>      | <span data-ttu-id="77a9b-123">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="77a9b-123">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="77a9b-124">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="77a9b-124">Delegated (work or school account)</span></span> | <span data-ttu-id="77a9b-125">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="77a9b-125">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="77a9b-126">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="77a9b-126">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="77a9b-127">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="77a9b-127">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="77a9b-128">Aplicación</span><span class="sxs-lookup"><span data-stu-id="77a9b-128">Application</span></span> | <span data-ttu-id="77a9b-129">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="77a9b-129">Mail.Read, Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="77a9b-130">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="77a9b-130">HTTP request</span></span>

<span data-ttu-id="77a9b-131">Para obtener todos los mensajes del buzón de un usuario:</span><span class="sxs-lookup"><span data-stu-id="77a9b-131">To get all the messages in a user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/messages
GET /users/{id | userPrincipalName}/messages
```

<span data-ttu-id="77a9b-132">Para obtener los mensajes de una carpeta específica del buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="77a9b-132">To get messages in a specific folder in the user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}/messages
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages
```

## <a name="optional-query-parameters"></a><span data-ttu-id="77a9b-133">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="77a9b-133">Optional query parameters</span></span>
<span data-ttu-id="77a9b-134">Este método admite los [parámetros de consulta de OData]((http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters)) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77a9b-134">This method supports the [OData Query Parameters]((http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters)) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="77a9b-135">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="77a9b-135">Request headers</span></span>
| <span data-ttu-id="77a9b-136">Nombre</span><span class="sxs-lookup"><span data-stu-id="77a9b-136">Name</span></span>       | <span data-ttu-id="77a9b-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="77a9b-137">Type</span></span> | <span data-ttu-id="77a9b-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="77a9b-138">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="77a9b-139">Authorization</span><span class="sxs-lookup"><span data-stu-id="77a9b-139">Authorization</span></span>  | <span data-ttu-id="77a9b-140">string</span><span class="sxs-lookup"><span data-stu-id="77a9b-140">string</span></span>  | <span data-ttu-id="77a9b-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="77a9b-p106">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="77a9b-143">Prefer: outlook.body-content-type</span><span class="sxs-lookup"><span data-stu-id="77a9b-143">Prefer: outlook.body-content-type</span></span> | <span data-ttu-id="77a9b-144">string</span><span class="sxs-lookup"><span data-stu-id="77a9b-144">string</span></span> | <span data-ttu-id="77a9b-145">Formato de las propiedades **body** y **uniqueBody** que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="77a9b-145">The format of the **body** and **uniqueBody** properties to be returned in.</span></span> <span data-ttu-id="77a9b-146">Los valores pueden ser "text" o "html".</span><span class="sxs-lookup"><span data-stu-id="77a9b-146">Values can be "text" or "html".</span></span> <span data-ttu-id="77a9b-147">Si no se especifica el encabezado, las propiedades **body** y **uniqueBody** se devuelven en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="77a9b-147">If the header is not specified, the **body** and **uniqueBody** properties are returned in HTML format.</span></span> <span data-ttu-id="77a9b-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="77a9b-148">Optional.</span></span> |


## <a name="request-body"></a><span data-ttu-id="77a9b-149">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="77a9b-149">Request body</span></span>
<span data-ttu-id="77a9b-150">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="77a9b-150">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="77a9b-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77a9b-151">Response</span></span>

<span data-ttu-id="77a9b-152">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77a9b-152">If successful, this method returns a `200 OK` response code and collection of [Message](../resources/message.md) objects in the response body.</span></span>

<span data-ttu-id="77a9b-153">El tamaño de página predeterminada para esta solicitud es de 10 mensajes.</span><span class="sxs-lookup"><span data-stu-id="77a9b-153">The default page size for this request is 10 messages.</span></span>

## <a name="example"></a><span data-ttu-id="77a9b-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="77a9b-154">Example</span></span>
##### <a name="request"></a><span data-ttu-id="77a9b-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="77a9b-155">Request</span></span>
<span data-ttu-id="77a9b-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="77a9b-156">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_messages"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages
```
##### <a name="response"></a><span data-ttu-id="77a9b-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77a9b-157">Response</span></span>
<span data-ttu-id="77a9b-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="77a9b-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 317

{
  "value": [
    {
      "receivedDateTime": "datetime-value",
      "sentDateTime": "datetime-value",
      "hasAttachments": true,
      "subject": "subject-value",
      "body": {
        "contentType": "",
        "content": "content-value"
      },
      "bodyPreview": "bodyPreview-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List messages",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
