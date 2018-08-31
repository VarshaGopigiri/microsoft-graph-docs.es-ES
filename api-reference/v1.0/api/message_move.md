# <a name="message-move"></a><span data-ttu-id="74f91-101">mensaje: mover</span><span class="sxs-lookup"><span data-stu-id="74f91-101">message: move</span></span>

<span data-ttu-id="74f91-102">Mueve un mensaje a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="74f91-102">Move a DriveItem to a new folder</span></span> <span data-ttu-id="74f91-103">Esto crea una nueva copia del mensaje en la carpeta de destino y elimina el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="74f91-103">Move the message to a folder. This creates a new copy of the message in the destination folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="74f91-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="74f91-104">Permissions</span></span>

<span data-ttu-id="74f91-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="74f91-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="74f91-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="74f91-107">Permission type</span></span> | <span data-ttu-id="74f91-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="74f91-108">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
|<span data-ttu-id="74f91-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="74f91-109">Delegated (work or school account)</span></span> | <span data-ttu-id="74f91-110">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="74f91-110">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="74f91-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="74f91-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="74f91-112">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="74f91-112">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="74f91-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="74f91-113">Application</span></span> | <span data-ttu-id="74f91-114">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="74f91-114">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="74f91-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="74f91-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/messages/{id}/move
POST /users/{id | userPrincipalName}/messages/{id}/move
POST /me/mailFolders/{id}/messages/{id}/move
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/move
```

## <a name="request-headers"></a><span data-ttu-id="74f91-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="74f91-116">Request headers</span></span>

| <span data-ttu-id="74f91-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74f91-117">Header</span></span> | <span data-ttu-id="74f91-118">Valor</span><span class="sxs-lookup"><span data-stu-id="74f91-118">Value</span></span> |
|:-------|:------|
| <span data-ttu-id="74f91-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="74f91-119">Authorization</span></span> | <span data-ttu-id="74f91-120">`Bearer {token}`.</span><span class="sxs-lookup"><span data-stu-id="74f91-120"></span></span> <span data-ttu-id="74f91-121">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="74f91-121">Required.</span></span> |
| <span data-ttu-id="74f91-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="74f91-122">Content-Type</span></span> | <span data-ttu-id="74f91-123">`application/json`.</span><span class="sxs-lookup"><span data-stu-id="74f91-123"></span></span> <span data-ttu-id="74f91-124">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="74f91-124">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="74f91-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="74f91-125">Request body</span></span>

<span data-ttu-id="74f91-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="74f91-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="74f91-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="74f91-127">Parameter</span></span>   | <span data-ttu-id="74f91-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="74f91-128">Type</span></span> |<span data-ttu-id="74f91-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="74f91-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="74f91-130">destinationId</span><span class="sxs-lookup"><span data-stu-id="74f91-130">destinationId</span></span>|<span data-ttu-id="74f91-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="74f91-131">String</span></span>|<span data-ttu-id="74f91-132">El identificador de la carpeta de destino, o un nombre de carpeta conocido.</span><span class="sxs-lookup"><span data-stu-id="74f91-132">The destination folder ID, or the , , , or  well-known folder name.</span></span> <span data-ttu-id="74f91-133">Para obtener una lista de los nombres de carpetas conocidos compatibles, vea [Tipo de recurso mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="74f91-133">For a list of supported well-known folder names, see [mailFolder resource type](../resources/mailfolder.md).</span></span>|

## <a name="response"></a><span data-ttu-id="74f91-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74f91-134">Response</span></span>

<span data-ttu-id="74f91-135">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y un recurso [message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="74f91-135">If successful, this method returns `201 Created` response code and a [Driveitem](../resources/message.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="74f91-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="74f91-136">Example</span></span>

<span data-ttu-id="74f91-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="74f91-137">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="74f91-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="74f91-138">Request</span></span>

<span data-ttu-id="74f91-139">La siguiente solicitud mueve el mensaje especificado a la carpeta de Elementos eliminados, identificada por su bien conocido nombre de la carpeta `deleteditems`.</span><span class="sxs-lookup"><span data-stu-id="74f91-139">The following request moves the specified message to the Deleted Items folder, identified by its well-known folder name `deleteditems`.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkADhAAATs28OAAA="],
  "name": "message_move"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/messages/AAMkADhAAATs28OAAA=/move
Content-type: application/json

{
  "destinationId": "deleteditems"
}
```

##### <a name="response"></a><span data-ttu-id="74f91-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74f91-140">Response</span></span>

<span data-ttu-id="74f91-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="74f91-141">Here is an example of the response.</span></span>

> <span data-ttu-id="74f91-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="74f91-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->

```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#message",
    "@odata.type":"#microsoft.graph.message",
    "@odata.etag":"W/\"FwAAABYAAAC4ofQHEIqCSbQPot83AFcbAAAW/0tB\"",
    "id":"AAMkADhAAAW-VPeAAA=",
    "createdDateTime":"2018-08-12T08:43:22Z",
    "lastModifiedDateTime":"2018-08-15T19:47:54Z",
    "changeKey":"FwAAABYAAAC4ofQHEIqCSbQPot83AFcbAAAW/0tB",
    "categories":[

    ],
    "receivedDateTime":"2018-08-12T08:43:22Z",
    "sentDateTime":"2018-08-12T08:43:20Z",
    "hasAttachments":false,
    "internetMessageId":"<00535324-5988-4b6a-b9af-d44cf2d0b691@MWHPR2201MB1022.namprd22.prod.outlook.com>",
    "subject":"Undeliverable: Meet for lunch?",
    "bodyPreview":"Delivery has failed to these recipients or groups:\r\n\r\nfannyd@contoso.onmicrosoft.com (fannyd@contoso.onmicrosoft.com)\r\nYour message couldn't be delivered. Despite repeated attempts to deliver your message, querying the Domain Name System (DNS) for the rec",
    "importance":"normal",
    "parentFolderId":"AAMkADhAAAAAAEKAAA=",
    "conversationId":"AAQkADhJzfbkARFhe5kKhjihSA=",
    "isDeliveryReceiptRequested":null,
    "isReadReceiptRequested":false,
    "isRead":false,
    "isDraft":false,
    "webLink":"https://outlook.office365.com/owa/?ItemID=AAMkADhAAAW%2FVPeAAA%3D&exvsurl=1&viewmodel=ReadMessageItem",
    "inferenceClassification":"focused",
    "body":{
        "contentType":"html",
        "content":"<html></html>"
    },
    "sender":{
        "emailAddress":{
            "name":"Microsoft Outlook",
            "address":"MicrosoftExchange329e71ec88ae4615bbc36ab6ce41109e@contoso.onmicrosoft.com"
        }
    },
    "from":{
        "emailAddress":{
            "name":"Microsoft Outlook",
            "address":"MicrosoftExchange329e71ec88ae4615bbc36ab6ce41109e@contoso.onmicrosoft.com"
        }
    },
    "toRecipients":[
        {
            "emailAddress":{
                "name":"fannyd@contoso.onmicrosoft.com",
                "address":"fannyd@contoso.onmicrosoft.com"
            }
        },
        {
            "emailAddress":{
                "name":"danas@contoso.onmicrosoft.com",
                "address":"danas@contoso.onmicrosoft.com"
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

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: move",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
