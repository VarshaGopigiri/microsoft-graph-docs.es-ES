# <a name="get-message"></a><span data-ttu-id="bf5e3-101">Obtener mensaje</span><span class="sxs-lookup"><span data-stu-id="bf5e3-101">Get message</span></span>

<span data-ttu-id="bf5e3-102">Recupere las propiedades y las relaciones de un objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="bf5e3-102">Retrieve the properties and relationships of a [message](../resources/message.md) object.</span></span>

<span data-ttu-id="bf5e3-103">Actualmente, esta operación devuelve los cuerpos de los mensajes solo en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="bf5e3-103">Currently, this operation returns message bodies in only HTML format.</span></span>

<span data-ttu-id="bf5e3-104">Existen dos escenarios en los que una aplicación puede obtener un mensaje en la carpeta de correo de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="bf5e3-104">There are two scenarios where an app can get a message in another user's mail folder:</span></span>

* <span data-ttu-id="bf5e3-105">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="bf5e3-105">If the app has application permissions, or,</span></span>
* <span data-ttu-id="bf5e3-106">si la aplicación tiene los correspondientes [permisos](#permissions) delegados de un usuario, y otro usuario ha compartido una carpeta de correos con ese usuario, o se le ha concedido acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="bf5e3-106">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a mail folder with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="bf5e3-107">Consulte los [detalles y un ejemplo](../../../concepts/outlook-share-messages-folders.md).</span><span class="sxs-lookup"><span data-stu-id="bf5e3-107">See [details and an example](../../../concepts/outlook-share-messages-folders.md).</span></span>

<span data-ttu-id="bf5e3-108">Dado que el recurso **message** admite [extensiones](../../../concepts/extensibility_overview.md), también puede utilizar la operación `GET` para obtener propiedades personalizadas y datos de extensión en una instancia de **message**.</span><span class="sxs-lookup"><span data-stu-id="bf5e3-108">Since the **message** resource supports [extensions](../../../concepts/extensibility_overview.md), you can also use the `GET` operation to get custom properties and extension data in a **message** instance.</span></span>


## <a name="permissions"></a><span data-ttu-id="bf5e3-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="bf5e3-109">Permissions</span></span>
<span data-ttu-id="bf5e3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="bf5e3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="bf5e3-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bf5e3-112">Permission type</span></span>      | <span data-ttu-id="bf5e3-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bf5e3-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bf5e3-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bf5e3-114">Delegated (work or school account)</span></span> | <span data-ttu-id="bf5e3-115">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="bf5e3-115">Mail.Read</span></span>    |
|<span data-ttu-id="bf5e3-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bf5e3-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bf5e3-117">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="bf5e3-117">Mail.Read</span></span>    |
|<span data-ttu-id="bf5e3-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bf5e3-118">Application</span></span> | <span data-ttu-id="bf5e3-119">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="bf5e3-119">Mail.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="bf5e3-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bf5e3-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/messages/{id}
GET /users/{id | userPrincipalName}/messages/{id}
GET /me/mailFolders/{id}/messages/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="bf5e3-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bf5e3-121">Optional query parameters</span></span>
<span data-ttu-id="bf5e3-122">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf5e3-122">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="bf5e3-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bf5e3-123">Request headers</span></span>
| <span data-ttu-id="bf5e3-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="bf5e3-124">Name</span></span>       | <span data-ttu-id="bf5e3-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="bf5e3-125">Type</span></span> | <span data-ttu-id="bf5e3-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf5e3-126">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="bf5e3-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="bf5e3-127">Authorization</span></span>  | <span data-ttu-id="bf5e3-128">cadena</span><span class="sxs-lookup"><span data-stu-id="bf5e3-128">string</span></span>  | <span data-ttu-id="bf5e3-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bf5e3-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="bf5e3-131">Preferido: outlook.body-content-type</span><span class="sxs-lookup"><span data-stu-id="bf5e3-131">Prefer: outlook.body-content-type</span></span> | <span data-ttu-id="bf5e3-132">cadena</span><span class="sxs-lookup"><span data-stu-id="bf5e3-132">string</span></span> | <span data-ttu-id="bf5e3-133">Formato de las propiedades **body** y **uniqueBody** que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="bf5e3-133">The format of the **body** and **uniqueBody** properties to be returned in.</span></span> <span data-ttu-id="bf5e3-134">Los valores pueden ser "text" o "html".</span><span class="sxs-lookup"><span data-stu-id="bf5e3-134">Values can be "text" or "html".</span></span> <span data-ttu-id="bf5e3-135">Se devuelve un encabezado `Preference-Applied` como confirmación si se especifica este encabezado `Prefer`.</span><span class="sxs-lookup"><span data-stu-id="bf5e3-135">A `Preference-Applied` header is returned as confirmation if this `Prefer` header is specified.</span></span> <span data-ttu-id="bf5e3-136">Si no se especifica el encabezado, las propiedades **body** y **uniqueBody** se devuelven en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="bf5e3-136">If the header is not specified, the **body** and **uniqueBody** properties are returned in HTML format.</span></span> <span data-ttu-id="bf5e3-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bf5e3-137">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bf5e3-138">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bf5e3-138">Request body</span></span>
<span data-ttu-id="bf5e3-139">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bf5e3-139">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bf5e3-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf5e3-140">Response</span></span>

<span data-ttu-id="bf5e3-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf5e3-141">If successful, this method returns a `200 OK` response code and [message](../resources/message.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="bf5e3-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bf5e3-142">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="bf5e3-143">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="bf5e3-143">Request 1</span></span>
<span data-ttu-id="bf5e3-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf5e3-144">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkADhMGAAA="],
  "name": "get_message"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/AAMkADhMGAAA=
```
##### <a name="response-1"></a><span data-ttu-id="bf5e3-145">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="bf5e3-145">Response 1</span></span>
<span data-ttu-id="bf5e3-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bf5e3-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request-2"></a><span data-ttu-id="bf5e3-149">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="bf5e3-149">Request 2</span></span>
<span data-ttu-id="bf5e3-150">En el ejemplo siguiente se usa un parámetro de consulta `$select` para obtener los encabezados de mensaje de Internet de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="bf5e3-150">The next example uses a `$select` query parameter to get the Internet message headers of a message.</span></span> 
<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkADhAAAW-VPeAAA="],
  "name": "get_message_headers"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/AAMkADhAAAW-VPeAAA=/?$select=internetMessageHeaders
```
##### <a name="response-2"></a><span data-ttu-id="bf5e3-151">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="bf5e3-151">Response 2</span></span>
<span data-ttu-id="bf5e3-152">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf5e3-152">Here is an example of the response.</span></span> <span data-ttu-id="bf5e3-153">Nota: El conjunto de encabezados de mensaje en el objeto de respuesta se trunca por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="bf5e3-153">Note: The set of message headers in the response object is truncated for brevity.</span></span> <span data-ttu-id="bf5e3-154">Se devolverán todos los encabezados de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bf5e3-154">All of the properties will be returned from an actual call.</span></span>
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


## <a name="see-also"></a><span data-ttu-id="bf5e3-155">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bf5e3-155">See also</span></span>

- [<span data-ttu-id="bf5e3-156">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="bf5e3-156">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="bf5e3-157">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="bf5e3-157">Add custom data to users using open extensions (preview)</span></span>](../../../concepts/extensibility_open_users.md)
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
