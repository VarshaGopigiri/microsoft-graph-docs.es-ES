# <a name="update-eventmessage"></a><span data-ttu-id="d3a15-101">Update eventMessage</span><span class="sxs-lookup"><span data-stu-id="d3a15-101">Update eventmessage</span></span>

<span data-ttu-id="d3a15-102">Actualiza las propiedades de un objeto [eventMessage](../resources/eventmessage.md).</span><span class="sxs-lookup"><span data-stu-id="d3a15-102">Update the properties of eventmessage object.</span></span>
## <a name="permissions"></a><span data-ttu-id="d3a15-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="d3a15-103">Permissions</span></span>
<span data-ttu-id="d3a15-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d3a15-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d3a15-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d3a15-106">Permission type</span></span>      | <span data-ttu-id="d3a15-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d3a15-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d3a15-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d3a15-108">Delegated (work or school account)</span></span> | <span data-ttu-id="d3a15-109">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d3a15-109">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="d3a15-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d3a15-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d3a15-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d3a15-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="d3a15-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d3a15-112">Application</span></span> | <span data-ttu-id="d3a15-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d3a15-113">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="d3a15-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d3a15-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/messages/{id}
PATCH /users/{id | userPrincipalName}/messages/{id}

PATCH /me/mailFolders/{id}/messages/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="d3a15-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d3a15-115">Request headers</span></span>
| <span data-ttu-id="d3a15-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="d3a15-116">Name</span></span>       | <span data-ttu-id="d3a15-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="d3a15-117">Type</span></span> | <span data-ttu-id="d3a15-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3a15-118">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="d3a15-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="d3a15-119">Authorization</span></span>  | <span data-ttu-id="d3a15-120">string</span><span class="sxs-lookup"><span data-stu-id="d3a15-120">string</span></span>  | <span data-ttu-id="d3a15-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d3a15-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d3a15-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d3a15-123">Content-Type</span></span> | <span data-ttu-id="d3a15-124">string</span><span class="sxs-lookup"><span data-stu-id="d3a15-124">string</span></span>  | <span data-ttu-id="d3a15-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d3a15-p103">Nature of the data in the body of an entity. Required.</span></span> |
## <a name="request-body"></a><span data-ttu-id="d3a15-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d3a15-127">Request body</span></span>
<span data-ttu-id="d3a15-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado. Son propiedades Writable/Updatable</span><span class="sxs-lookup"><span data-stu-id="d3a15-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed. Writable/Updatable properties are</span></span>

| <span data-ttu-id="d3a15-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d3a15-132">Property</span></span>     | <span data-ttu-id="d3a15-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="d3a15-133">Type</span></span>   |<span data-ttu-id="d3a15-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3a15-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d3a15-135">categories</span><span class="sxs-lookup"><span data-stu-id="d3a15-135">categories</span></span>|<span data-ttu-id="d3a15-136">String</span><span class="sxs-lookup"><span data-stu-id="d3a15-136">String</span></span>|<span data-ttu-id="d3a15-137">Categorías asociadas al mensaje.</span><span class="sxs-lookup"><span data-stu-id="d3a15-137">The categories associated with the message.</span></span>|
|<span data-ttu-id="d3a15-138">importance</span><span class="sxs-lookup"><span data-stu-id="d3a15-138">importance</span></span>|<span data-ttu-id="d3a15-139">String</span><span class="sxs-lookup"><span data-stu-id="d3a15-139">String</span></span>|<span data-ttu-id="d3a15-p105">Importancia del mensaje. Valores posibles: `Low`, `Normal`, `High`.</span><span class="sxs-lookup"><span data-stu-id="d3a15-p105">The importance of the message. Possible values are: `Low`, `Normal`, `High`.</span></span>|
|<span data-ttu-id="d3a15-142">isDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="d3a15-142">isDeliveryReceiptRequested</span></span>|<span data-ttu-id="d3a15-143">Booleano</span><span class="sxs-lookup"><span data-stu-id="d3a15-143">Boolean</span></span>|<span data-ttu-id="d3a15-144">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d3a15-144">Indicates whether a read receipt is requested for the message.</span></span>|
|<span data-ttu-id="d3a15-145">isRead</span><span class="sxs-lookup"><span data-stu-id="d3a15-145">isRead</span></span>|<span data-ttu-id="d3a15-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="d3a15-146">Boolean</span></span>|<span data-ttu-id="d3a15-147">Indica si se ha leído el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d3a15-147">Indicates whether the message has been read.</span></span>|
|<span data-ttu-id="d3a15-148">isReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="d3a15-148">isReadReceiptRequested</span></span>|<span data-ttu-id="d3a15-149">Booleano</span><span class="sxs-lookup"><span data-stu-id="d3a15-149">Boolean</span></span>|<span data-ttu-id="d3a15-150">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d3a15-150">Indicates whether a read receipt is requested for the message.</span></span>|

## <a name="response"></a><span data-ttu-id="d3a15-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d3a15-151">Response</span></span>

<span data-ttu-id="d3a15-152">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [eventMessage](../resources/eventmessage.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d3a15-152">If successful, this method returns a `200 OK` response code and updated [eventMessage](../resources/eventmessage.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d3a15-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d3a15-153">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d3a15-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d3a15-154">Request</span></span>
<span data-ttu-id="d3a15-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d3a15-155">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="d3a15-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d3a15-156">Response</span></span>
<span data-ttu-id="d3a15-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d3a15-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.eventMessage"
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
