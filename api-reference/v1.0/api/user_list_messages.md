# <a name="list-messages"></a><span data-ttu-id="72cba-101">Enumerar mensajes</span><span class="sxs-lookup"><span data-stu-id="72cba-101">List messages</span></span>

<span data-ttu-id="72cba-102">Obtenga los mensajes del buzón del usuario que ha iniciado sesión (incluidas las carpetas Elementos eliminados y Otros correos).</span><span class="sxs-lookup"><span data-stu-id="72cba-102">Get the messages in the signed-in user's mailbox (including the Deleted Items and Clutter folders).</span></span>

<span data-ttu-id="72cba-103">Actualmente, esta operación devuelve los cuerpos de los mensajes solo en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="72cba-103">Currently, this operation returns message bodies in only HTML format.</span></span>


### <a name="get-messages-in-another-users-message-folder"></a><span data-ttu-id="72cba-104">Obtener mensajes en la carpeta de mensajes de otro usuario</span><span class="sxs-lookup"><span data-stu-id="72cba-104">Get messages in another user's message folder</span></span>

<span data-ttu-id="72cba-105">Si dispone de permisos de la aplicación o si tiene los [permisos](#permissions) delegados apropiados de un usuario, es posible obtener los contactos de la carpeta de contactos de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="72cba-105">If you have application permissions, or if you have the appropriate delegated [permissions](#permissions) from one user, it's possible to get contacts from another user's contact folder.</span></span> <span data-ttu-id="72cba-106">Esta sección se centra en escenarios que implican permisos delegados.</span><span class="sxs-lookup"><span data-stu-id="72cba-106">This section focuses on scenarios that involve delegated permissions.</span></span>

<span data-ttu-id="72cba-107">Por ejemplo, su aplicación ha adquirido permisos delegados del usuario John.</span><span class="sxs-lookup"><span data-stu-id="72cba-107">For example, your app has acquired delegated permissions from the user, John.</span></span> <span data-ttu-id="72cba-108">Suponga que otro usuario, Garth, ha compartido una carpeta de mensajes con John.</span><span class="sxs-lookup"><span data-stu-id="72cba-108">Suppose another user, Garth, has shared a contact folder with John.</span></span> <span data-ttu-id="72cba-109">Puede obtener los mensajes de dicha carpeta compartida especificando el identificador de usuario de Garth (o su nombre principal de usuario) en la consulta de ejemplo que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="72cba-109">You can get the contacts in that shared folder by specifying Garth’s user ID (or user principal name) in the example query shown below.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/{Garth-id | Garth-userPrincipalName}/messages
```

<span data-ttu-id="72cba-110">Esta capacidad se aplica a todas las operaciones de mensajes GET compatibles para un usuario individual, como se muestra en la sección [solicitud HTTP](#http-request) a continuación.</span><span class="sxs-lookup"><span data-stu-id="72cba-110">This capability applies to all the supported GET contacts operations for an individual user, as listed in the [HTTP request](#http-request) section below.</span></span> <span data-ttu-id="72cba-111">También se aplica si Garth ha delegado todo el buzón en John.</span><span class="sxs-lookup"><span data-stu-id="72cba-111">It also applies if Garth has delegated his entire mailbox to John.</span></span>

<span data-ttu-id="72cba-112">Si Garth no ha compartido su carpeta de mensajes con John ni ha delegado su buzón en John, especificar el identificador de usuario del Garth o el nombre principal de usuario en esas operaciones GET devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="72cba-112">If Garth has not shared his contact folder with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> <span data-ttu-id="72cba-113">En tales casos, especificar un identificador de usuario o un nombre principal de usuario solo funciona para obtener los mensajes de las carpetas de mensajes del usuario que ha iniciado sesión, y la consulta es equivalente a usar el método abreviado de /me:</span><span class="sxs-lookup"><span data-stu-id="72cba-113">In such cases, specifying a user ID or user principal name only works for getting a contact in the signed-in user’s own contact folders, and the query is equivalent to using the /me shortcut:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/messages
```

<span data-ttu-id="72cba-114">Esta capacidad solo está disponible en las operaciones GET de:</span><span class="sxs-lookup"><span data-stu-id="72cba-114">This capability is available in only GET operations of:</span></span>

- <span data-ttu-id="72cba-115">Uso compartido de carpetas de contactos, calendarios y carpetas de mensajes</span><span class="sxs-lookup"><span data-stu-id="72cba-115">Shared contact folders, calendars, and message folders</span></span> 
- <span data-ttu-id="72cba-116">Contactos, eventos y mensajes en carpetas compartidas</span><span class="sxs-lookup"><span data-stu-id="72cba-116">Contacts and events in shared folders</span></span>
- <span data-ttu-id="72cba-117">Los recursos anteriores en buzones delegados</span><span class="sxs-lookup"><span data-stu-id="72cba-117">The above resources in delegated mailboxes</span></span>

<span data-ttu-id="72cba-118">Esta capacidad no está disponible en otras operaciones de contactos, eventos, mensajes y sus carpetas.</span><span class="sxs-lookup"><span data-stu-id="72cba-118">This capability is not available in other operations for contacts, events, and their folders.</span></span>


## <a name="permissions"></a><span data-ttu-id="72cba-119">Permisos</span><span class="sxs-lookup"><span data-stu-id="72cba-119">Permissions</span></span>
<span data-ttu-id="72cba-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="72cba-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="72cba-122">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="72cba-122">Permission type</span></span>      | <span data-ttu-id="72cba-123">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="72cba-123">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="72cba-124">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="72cba-124">Delegated (work or school account)</span></span> | <span data-ttu-id="72cba-125">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="72cba-125">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="72cba-126">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="72cba-126">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="72cba-127">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="72cba-127">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="72cba-128">Aplicación</span><span class="sxs-lookup"><span data-stu-id="72cba-128">Application</span></span> | <span data-ttu-id="72cba-129">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="72cba-129">Mail.Read, Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="72cba-130">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="72cba-130">HTTP request</span></span>

<span data-ttu-id="72cba-131">Para obtener todos los mensajes del buzón de un usuario:</span><span class="sxs-lookup"><span data-stu-id="72cba-131">To get all the messages in a user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/messages
GET /users/{id | userPrincipalName}/messages
```

<span data-ttu-id="72cba-132">Para obtener los mensajes de una carpeta específica del buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="72cba-132">To get messages in a specific folder in the user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}/messages
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages
```

## <a name="optional-query-parameters"></a><span data-ttu-id="72cba-133">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="72cba-133">Optional query parameters</span></span>
<span data-ttu-id="72cba-134">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="72cba-134">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="72cba-135">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="72cba-135">Request headers</span></span>
| <span data-ttu-id="72cba-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72cba-136">Header</span></span>       | <span data-ttu-id="72cba-137">Valor</span><span class="sxs-lookup"><span data-stu-id="72cba-137">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="72cba-138">Authorization</span><span class="sxs-lookup"><span data-stu-id="72cba-138">Authorization</span></span>  | <span data-ttu-id="72cba-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="72cba-p106">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="72cba-141">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="72cba-141">Request body</span></span>
<span data-ttu-id="72cba-142">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="72cba-142">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="72cba-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="72cba-143">Response</span></span>

<span data-ttu-id="72cba-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="72cba-144">If successful, this method returns a `200 OK` response code and collection of [Message](../resources/message.md) objects in the response body.</span></span>

<span data-ttu-id="72cba-145">El tamaño de página predeterminada para esta solicitud es de 10 mensajes.</span><span class="sxs-lookup"><span data-stu-id="72cba-145">The default page size for this request is 10 messages.</span></span>

## <a name="example"></a><span data-ttu-id="72cba-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="72cba-146">Example</span></span>
##### <a name="request"></a><span data-ttu-id="72cba-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="72cba-147">Request</span></span>
<span data-ttu-id="72cba-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="72cba-148">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_messages"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages
```
##### <a name="response"></a><span data-ttu-id="72cba-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="72cba-149">Response</span></span>
<span data-ttu-id="72cba-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="72cba-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
