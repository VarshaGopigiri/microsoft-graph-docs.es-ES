# <a name="get-message"></a><span data-ttu-id="adf4c-101">Obtener mensaje</span><span class="sxs-lookup"><span data-stu-id="adf4c-101">Get message</span></span>

<span data-ttu-id="adf4c-102">Recupere las propiedades y las relaciones de un objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="adf4c-102">Retrieve the properties and relationships of a [message](../resources/message.md) object.</span></span>

<span data-ttu-id="adf4c-103">Dado que el recurso **message** admite [extensiones](../../../concepts/extensibility_overview.md), también puede utilizar la operación `GET` para obtener propiedades personalizadas y datos de extensión en una instancia **message**.</span><span class="sxs-lookup"><span data-stu-id="adf4c-103">Since the **message** resource supports [extensions](../../../concepts/extensibility_overview.md), you can also use the `GET` operation to get custom properties and extension data in a **message** instance.</span></span>

<span data-ttu-id="adf4c-104">Actualmente, esta operación devuelve los cuerpos de los mensajes solo en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="adf4c-104">Currently, this operation returns message bodies in only HTML format.</span></span>


### <a name="get-messages-in-another-users-message-folder"></a><span data-ttu-id="adf4c-105">Obtener mensajes en la carpeta de mensajes de otro usuario</span><span class="sxs-lookup"><span data-stu-id="adf4c-105">Get messages in another user's message folder</span></span>

<span data-ttu-id="adf4c-106">Si dispone de permisos de la aplicación o si tiene los [permisos](#permissions) delegados apropiados de un usuario, es posible obtener los contactos de la carpeta de contactos de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="adf4c-106">If you have application permissions, or if you have the appropriate delegated [permissions](#permissions) from one user, it's possible to get messages from another user's message folder.</span></span> <span data-ttu-id="adf4c-107">Esta sección se centra en escenarios que implican permisos delegados.</span><span class="sxs-lookup"><span data-stu-id="adf4c-107">This section focuses on scenarios that involve delegated permissions.</span></span>

<span data-ttu-id="adf4c-108">Por ejemplo, su aplicación ha adquirido permisos delegados del usuario John.</span><span class="sxs-lookup"><span data-stu-id="adf4c-108">For example, your app has acquired delegated permissions from the user, John.</span></span> <span data-ttu-id="adf4c-109">Suponga que otro usuario, Garth, ha compartido una carpeta de mensajes con John.</span><span class="sxs-lookup"><span data-stu-id="adf4c-109">Suppose another user, Garth, has shared a message folder with John.</span></span> <span data-ttu-id="adf4c-110">Puede obtener un mensaje de dicha carpeta compartida especificando el identificador de usuario de Garth (o su nombre principal de usuario) en la consulta de ejemplo que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="adf4c-110">You can get a message in that shared folder by specifying Garth’s user ID (or user principal name) in the example query shown below.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/{Garth-id | Garth-userPrincipalName}/messages/{id}
```

<span data-ttu-id="adf4c-111">Esta capacidad se aplica a todas las operaciones de mensajes GET compatibles para un usuario individual, como se muestra en la sección [solicitud HTTP](#http-request) a continuación.</span><span class="sxs-lookup"><span data-stu-id="adf4c-111">This capability applies to all the supported GET messages operations for an individual user, as listed in the [HTTP request](#http-request) section below.</span></span> <span data-ttu-id="adf4c-112">También se aplica si Garth ha delegado todo el buzón en John.</span><span class="sxs-lookup"><span data-stu-id="adf4c-112">It also applies if Garth has delegated his entire mailbox to John.</span></span>

<span data-ttu-id="adf4c-113">Si Garth no ha compartido su carpeta de mensajes con John ni ha delegado su buzón en John, especificar el identificador de usuario del Garth o el nombre principal de usuario en esas operaciones GET devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="adf4c-113">If Garth has not shared his message folder with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> <span data-ttu-id="adf4c-114">En tales casos, especificar un identificador de usuario o un nombre principal de usuario solo funciona para obtener un mensaje de las carpetas de mensajes del usuario que ha iniciado sesión, y la consulta es equivalente a usar el método abreviado de /me:</span><span class="sxs-lookup"><span data-stu-id="adf4c-114">In such cases, specifying a user ID or user principal name only works for getting a message in the signed-in user’s own message folders, and the query is equivalent to using the /me shortcut:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/messages/{id}
```

<span data-ttu-id="adf4c-115">Esta capacidad solo está disponible en las operaciones GET de:</span><span class="sxs-lookup"><span data-stu-id="adf4c-115">This capability is available in only GET operations of:</span></span>

- <span data-ttu-id="adf4c-116">Uso compartido de carpetas de contactos, calendarios y carpetas de mensajes</span><span class="sxs-lookup"><span data-stu-id="adf4c-116">Shared contact folders, calendars, and message folders</span></span> 
- <span data-ttu-id="adf4c-117">Contactos, eventos y mensajes en carpetas compartidas</span><span class="sxs-lookup"><span data-stu-id="adf4c-117">Contacts, events, and messages in shared folders</span></span>
- <span data-ttu-id="adf4c-118">Los recursos anteriores en buzones delegados</span><span class="sxs-lookup"><span data-stu-id="adf4c-118">The above resources in delegated mailboxes</span></span>

<span data-ttu-id="adf4c-119">Esta capacidad no está disponible en otras operaciones de contactos, eventos, mensajes y sus carpetas.</span><span class="sxs-lookup"><span data-stu-id="adf4c-119">This capability is not available in other operations for contacts, events, messages, and their folders.</span></span>


## <a name="permissions"></a><span data-ttu-id="adf4c-120">Permisos</span><span class="sxs-lookup"><span data-stu-id="adf4c-120">Permissions</span></span>
<span data-ttu-id="adf4c-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="adf4c-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="adf4c-123">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="adf4c-123">Permission type</span></span>      | <span data-ttu-id="adf4c-124">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="adf4c-124">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="adf4c-125">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="adf4c-125">Delegated (work or school account)</span></span> | <span data-ttu-id="adf4c-126">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="adf4c-126">Mail.Read</span></span>    |
|<span data-ttu-id="adf4c-127">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="adf4c-127">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="adf4c-128">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="adf4c-128">Mail.Read</span></span>    |
|<span data-ttu-id="adf4c-129">Aplicación</span><span class="sxs-lookup"><span data-stu-id="adf4c-129">Application</span></span> | <span data-ttu-id="adf4c-130">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="adf4c-130">Mail.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="adf4c-131">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="adf4c-131">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/messages/{id}
GET /users/{id | userPrincipalName}/messages/{id}
GET /me/mailFolders/{id}/messages/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="adf4c-132">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="adf4c-132">Optional query parameters</span></span>
<span data-ttu-id="adf4c-133">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="adf4c-133">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="adf4c-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="adf4c-134">Request headers</span></span>
| <span data-ttu-id="adf4c-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="adf4c-135">Name</span></span>       | <span data-ttu-id="adf4c-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="adf4c-136">Type</span></span> | <span data-ttu-id="adf4c-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="adf4c-137">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="adf4c-138">Autorización</span><span class="sxs-lookup"><span data-stu-id="adf4c-138">Authorization</span></span>  | <span data-ttu-id="adf4c-139">cadena</span><span class="sxs-lookup"><span data-stu-id="adf4c-139">string</span></span>  | <span data-ttu-id="adf4c-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="adf4c-p106">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="adf4c-142">Prefer: outlook.body-content-type</span><span class="sxs-lookup"><span data-stu-id="adf4c-142">Prefer: outlook.body-content-type</span></span> | <span data-ttu-id="adf4c-143">cadena</span><span class="sxs-lookup"><span data-stu-id="adf4c-143">string</span></span> | <span data-ttu-id="adf4c-144">Formato de las propiedades **body** y **uniqueBody** que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="adf4c-144">The format of the **body** and **uniqueBody** properties to be returned in.</span></span> <span data-ttu-id="adf4c-145">Los valores pueden ser "text" o "html".</span><span class="sxs-lookup"><span data-stu-id="adf4c-145">Values can be "text" or "html".</span></span> <span data-ttu-id="adf4c-146">Se devuelve un encabezado `Preference-Applied` como confirmación si se especifica este encabezado `Prefer`.</span><span class="sxs-lookup"><span data-stu-id="adf4c-146">A `Preference-Applied` header is returned as confirmation if this `Prefer` header is specified.</span></span> <span data-ttu-id="adf4c-147">Si no se especifica el encabezado, las propiedades **body** y **uniqueBody** se devuelven en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="adf4c-147">If the header is not specified, the **body** and **uniqueBody** properties are returned in HTML format.</span></span> <span data-ttu-id="adf4c-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="adf4c-148">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="adf4c-149">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="adf4c-149">Request body</span></span>
<span data-ttu-id="adf4c-150">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="adf4c-150">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="adf4c-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="adf4c-151">Response</span></span>

<span data-ttu-id="adf4c-152">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="adf4c-152">If successful, this method returns a `200 OK` response code and [message](../resources/message.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="adf4c-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="adf4c-153">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="adf4c-154">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="adf4c-154">Request 1</span></span>
<span data-ttu-id="adf4c-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="adf4c-155">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkADhMGAAA="],
  "name": "get_message"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/AAMkADhMGAAA=
```
##### <a name="response-1"></a><span data-ttu-id="adf4c-156">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="adf4c-156">Response 1</span></span>
<span data-ttu-id="adf4c-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="adf4c-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('7f180cbb-a5ae-457c-b7e8-6f5b42ba33e7')/messages/$entity",
    "@odata.etag":"W/\"CQAAABYAAAC4ofQHEIqCSbQPot83AFcbAAAnjjuZ\"",
    "id":"AAMkADhMGAAA=",
    "createdDateTime":"2018-09-09T03:15:05Z",
    "lastModifiedDateTime":"2018-09-09T03:15:08Z",
    "changeKey":"CQAAABYAAAC4ofQHEIqCSbQPot83AFcbAAAnjjuZ",
    "categories":[

    ],
    "receivedDateTime":"2018-09-09T03:15:08Z",
    "sentDateTime":"2018-09-09T03:15:06Z",
    "hasAttachments":false,
    "internetMessageId":"<MWHPR6E1BE060@MWHPR1120.namprd22.prod.outlook.com>",
    "subject":"9/9/2018: concert",
    "bodyPreview":"The group represents Nevada.",
    "importance":"normal",
    "parentFolderId":"AAMkADcbAAAAAAEJAAA=",
    "conversationId":"AAQkADOUpag6yWs=",
    "isDeliveryReceiptRequested":false,
    "isReadReceiptRequested":false,
    "isRead":true,
    "isDraft":false,
    "webLink":"https://outlook.office365.com/owa/?ItemID=AAMkADMGAAA%3D&exvsurl=1&viewmodel=ReadMessageItem",
    "inferenceClassification":"focused",
    "body":{
        "contentType":"html",
        "content":"<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n<meta content=\"text/html; charset=us-ascii\">\r\n</head>\r\n<body>\r\nThe group represents Nevada.\r\n</body>\r\n</html>\r\n"
    },
    "sender":{
        "emailAddress":{
            "name":"Adele Vance",
            "address":"adelev@contoso.OnMicrosoft.com"
        }
    },
    "from":{
        "emailAddress":{
            "name":"Adele Vance",
            "address":"adelev@contoso.OnMicrosoft.com"
        }
    },
    "toRecipients":[
        {
            "emailAddress":{
                "name":"Alex Wilber",
                "address":"AlexW@contoso.OnMicrosoft.com"
            }
        }
    ],
    "ccRecipients":[

    ],
    "bccRecipients":[

    ],
    "replyTo":[

    ],
    "flag":{
        "flagStatus":"notFlagged"
    }
}
```

##### <a name="request-2"></a><span data-ttu-id="adf4c-160">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="adf4c-160">Request 2</span></span>
<span data-ttu-id="adf4c-161">En el ejemplo siguiente se usa un parámetro de consulta `$select` para obtener los encabezados de mensaje de Internet de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="adf4c-161">The next example uses a `$select` query parameter to get the Internet message headers of a message.</span></span> 
<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkADhAAAW-VPeAAA="],
  "name": "get_message_headers"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/AAMkADhAAAW-VPeAAA=/?$select=internetMessageHeaders
```
##### <a name="response-2"></a><span data-ttu-id="adf4c-162">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="adf4c-162">Response 2</span></span>
<span data-ttu-id="adf4c-163">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="adf4c-163">Here is an example of the response.</span></span> <span data-ttu-id="adf4c-164">Nota: El conjunto de encabezados de mensaje en el objeto de respuesta se trunca por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="adf4c-164">Note: The set of message headers in the response object is truncated for brevity.</span></span> <span data-ttu-id="adf4c-165">En una llamada real se devolverán todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="adf4c-165">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('7f180cbb-a5ae-457c-b7e8-6f5b42ba33e7')/messages(internetMessageHeaders)/$entity",
    "@odata.etag":"W/\"FwAAABYAAAC4ofQHEIqCSbQPot83AFcbAAAW/0tB\"",
    "id":"AAMkADhAAAW-VPeAAA=",
    "internetMessageHeaders":[
        {
            "name":"MIME-Version",
            "value":"1.0"
        },
        {
            "name":"Content-Type",
            "value":"multipart/report"
        },
        {
            "name":"x-custom-header-group-name",
            "value":"Washington"
        },
        {
            "name":"x-custom-header-group-id",
            "value":"WA001"
        }
    ]
}
```


## <a name="see-also"></a><span data-ttu-id="adf4c-166">Consulte también</span><span class="sxs-lookup"><span data-stu-id="adf4c-166">See also</span></span>

- [<span data-ttu-id="adf4c-167">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="adf4c-167">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="adf4c-168">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="adf4c-168">Add custom data to users using open extensions (preview)</span></span>](../../../concepts/extensibility_open_users.md)
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
