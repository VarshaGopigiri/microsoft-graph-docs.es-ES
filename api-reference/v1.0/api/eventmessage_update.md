# <a name="update-eventmessage"></a><span data-ttu-id="b8de5-101">Update eventmessage</span><span class="sxs-lookup"><span data-stu-id="b8de5-101">Update eventmessage</span></span>

<span data-ttu-id="b8de5-102">Actualiza las propiedades del objeto eventmessage.</span><span class="sxs-lookup"><span data-stu-id="b8de5-102">Update the properties of eventmessage object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b8de5-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b8de5-103">Prerequisites</span></span>
<span data-ttu-id="b8de5-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="b8de5-104">One of the following **scopes** is required to execute this API: *Mail.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="b8de5-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b8de5-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/messages/{id}
PATCH /users/{id | userPrincipalName}/messages/{id}

PATCH /me/mailFolders/{id}/messages/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="b8de5-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b8de5-106">Request headers</span></span>
| <span data-ttu-id="b8de5-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="b8de5-107">Name</span></span>       | <span data-ttu-id="b8de5-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8de5-108">Type</span></span> | <span data-ttu-id="b8de5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8de5-109">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="b8de5-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="b8de5-110">Authorization</span></span>  | <span data-ttu-id="b8de5-111">string</span><span class="sxs-lookup"><span data-stu-id="b8de5-111">string</span></span>  | <span data-ttu-id="b8de5-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b8de5-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="b8de5-114">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b8de5-114">Content-Type</span></span> | <span data-ttu-id="b8de5-115">string</span><span class="sxs-lookup"><span data-stu-id="b8de5-115">string</span></span>  | <span data-ttu-id="b8de5-p102">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b8de5-p102">Nature of the data in the body of an entity. Required.</span></span> |
## <a name="request-body"></a><span data-ttu-id="b8de5-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b8de5-118">Request body</span></span>
<span data-ttu-id="b8de5-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado. Son propiedades Writable/Updatable</span><span class="sxs-lookup"><span data-stu-id="b8de5-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed. Writable/Updatable properties are</span></span>

| <span data-ttu-id="b8de5-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b8de5-123">Property</span></span>     | <span data-ttu-id="b8de5-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8de5-124">Type</span></span>   |<span data-ttu-id="b8de5-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8de5-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b8de5-126">categories</span><span class="sxs-lookup"><span data-stu-id="b8de5-126">categories</span></span>|<span data-ttu-id="b8de5-127">String</span><span class="sxs-lookup"><span data-stu-id="b8de5-127">String</span></span>|<span data-ttu-id="b8de5-128">Categorías asociadas al mensaje.</span><span class="sxs-lookup"><span data-stu-id="b8de5-128">The categories associated with the message.</span></span>|
|<span data-ttu-id="b8de5-129">importance</span><span class="sxs-lookup"><span data-stu-id="b8de5-129">importance</span></span>|<span data-ttu-id="b8de5-130">String</span><span class="sxs-lookup"><span data-stu-id="b8de5-130">String</span></span>|<span data-ttu-id="b8de5-p104">La importancia del mensaje. Valores posibles: `Low`, `Normal`, `High`.</span><span class="sxs-lookup"><span data-stu-id="b8de5-p104">The importance of the message. Possible values are: `Low`, `Normal`, `High`.</span></span>|
|<span data-ttu-id="b8de5-133">isDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="b8de5-133">isDeliveryReceiptRequested</span></span>|<span data-ttu-id="b8de5-134">Booleano</span><span class="sxs-lookup"><span data-stu-id="b8de5-134">Boolean</span></span>|<span data-ttu-id="b8de5-135">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="b8de5-135">Indicates whether a read receipt is requested for the message.</span></span>|
|<span data-ttu-id="b8de5-136">isRead</span><span class="sxs-lookup"><span data-stu-id="b8de5-136">isRead</span></span>|<span data-ttu-id="b8de5-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="b8de5-137">Boolean</span></span>|<span data-ttu-id="b8de5-138">Indica si se ha leído el mensaje.</span><span class="sxs-lookup"><span data-stu-id="b8de5-138">Indicates whether the message has been read.</span></span>|
|<span data-ttu-id="b8de5-139">isReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="b8de5-139">isReadReceiptRequested</span></span>|<span data-ttu-id="b8de5-140">Booleano</span><span class="sxs-lookup"><span data-stu-id="b8de5-140">Boolean</span></span>|<span data-ttu-id="b8de5-141">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="b8de5-141">Indicates whether a read receipt is requested for the message.</span></span>|

## <a name="response"></a><span data-ttu-id="b8de5-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8de5-142">Response</span></span>

<span data-ttu-id="b8de5-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [eventMessage](../resources/eventmessage.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b8de5-143">If successful, this method returns a `200 OK` response code and updated [eventMessage](../resources/eventmessage.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="b8de5-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b8de5-144">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b8de5-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b8de5-145">Request</span></span>
<span data-ttu-id="b8de5-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b8de5-146">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_eventmessage"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/messages/{id}
Content-type: application/json
Content-length: 248

{
  "isRead": "true",
}
```
##### <a name="response"></a><span data-ttu-id="b8de5-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8de5-147">Response</span></span>
<span data-ttu-id="b8de5-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b8de5-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.eventmessage"
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
    "contentType": "",
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value",
  "meetingMessageType": "meetingMessageType-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update eventmessage",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
