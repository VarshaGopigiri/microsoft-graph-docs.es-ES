# <a name="message-createforward"></a><span data-ttu-id="68607-101">message: createForward</span><span class="sxs-lookup"><span data-stu-id="68607-101">message: createForward</span></span>

<span data-ttu-id="68607-102">Cree un borrador para reenviar el [mensaje](../resources/message.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="68607-102">Create a draft to forward the specified [message](../resources/message.md).</span></span> <span data-ttu-id="68607-103">Después, puede [actualizar](../api/message_update.md) el borrador para agregar contenido al **cuerpo**, cambiar otras propiedades del mensaje o, simplemente, [enviar](../api/message_send.md) el borrador.</span><span class="sxs-lookup"><span data-stu-id="68607-103">You can then [update](../api/message_update.md) the draft to add content to the **body** or change other message properties, or, simply [send](../api/message_send.md) the draft.</span></span>

## <a name="permissions"></a><span data-ttu-id="68607-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="68607-104">Permissions</span></span>

<span data-ttu-id="68607-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="68607-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="68607-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="68607-107">Permission type</span></span>      | <span data-ttu-id="68607-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="68607-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="68607-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="68607-109">Delegated (work or school account)</span></span> | <span data-ttu-id="68607-110">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="68607-110">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="68607-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="68607-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="68607-112">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="68607-112">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="68607-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="68607-113">Application</span></span> | <span data-ttu-id="68607-114">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="68607-114">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="68607-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="68607-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/messages/{id}/createForward
POST /users/{id | userPrincipalName}/messages/{id}/createForward
POST /me/mailFolders/{id}/messages/{id}/createForward
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/createForward
```

## <a name="request-headers"></a><span data-ttu-id="68607-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="68607-116">Request headers</span></span>

| <span data-ttu-id="68607-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="68607-117">Name</span></span>       | <span data-ttu-id="68607-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="68607-118">Type</span></span> | <span data-ttu-id="68607-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="68607-119">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="68607-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="68607-120">Authorization</span></span>  | <span data-ttu-id="68607-121">string</span><span class="sxs-lookup"><span data-stu-id="68607-121">string</span></span>  | <span data-ttu-id="68607-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="68607-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="68607-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="68607-124">Request body</span></span>

<span data-ttu-id="68607-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="68607-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="68607-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68607-126">Response</span></span>

<span data-ttu-id="68607-127">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68607-127">If successful, this method returns `201 Created` response code and [Message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="68607-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="68607-128">Example</span></span>

<span data-ttu-id="68607-129">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="68607-129">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="68607-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="68607-130">Request</span></span>

<span data-ttu-id="68607-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="68607-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_createforward"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/createForward
```

##### <a name="response"></a><span data-ttu-id="68607-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68607-132">Response</span></span>

<span data-ttu-id="68607-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="68607-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->

```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 248

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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: createForward",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
