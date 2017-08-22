# <a name="update-conversationthread"></a><span data-ttu-id="ae823-101">Update conversationthread</span><span class="sxs-lookup"><span data-stu-id="ae823-101">Update conversationthread</span></span>

<span data-ttu-id="ae823-102">Bloquea o desbloquea un hilo para permitir o impedir futuras publicaciones en el hilo.</span><span class="sxs-lookup"><span data-stu-id="ae823-102">Lock or unlock a thread, to allow or avoid further posting to the thread.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ae823-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ae823-103">Prerequisites</span></span>
<span data-ttu-id="ae823-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="ae823-104">One of the following **scopes** is required to execute this API: *Group.ReadWrite.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="ae823-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ae823-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /groups/{id}/threads/{id}
PATCH /groups/{id}/conversations/{id}/threads/{id}

```
## <a name="request-headers"></a><span data-ttu-id="ae823-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ae823-106">Request headers</span></span>
| <span data-ttu-id="ae823-107">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae823-107">Header</span></span>       | <span data-ttu-id="ae823-108">Valor</span><span class="sxs-lookup"><span data-stu-id="ae823-108">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ae823-109">Authorization</span><span class="sxs-lookup"><span data-stu-id="ae823-109">Authorization</span></span>  | <span data-ttu-id="ae823-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ae823-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="ae823-112">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ae823-112">Content-Type</span></span>  | <span data-ttu-id="ae823-p102">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ae823-p102">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ae823-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ae823-115">Request body</span></span>
<span data-ttu-id="ae823-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="ae823-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="ae823-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ae823-119">Property</span></span>     | <span data-ttu-id="ae823-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="ae823-120">Type</span></span>   |<span data-ttu-id="ae823-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae823-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ae823-122">isLocked</span><span class="sxs-lookup"><span data-stu-id="ae823-122">isLocked</span></span>|<span data-ttu-id="ae823-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="ae823-123">Boolean</span></span>|<span data-ttu-id="ae823-p104">Indica si el hilo está bloqueado. Establecer en `true` para impedir publicaciones.</span><span class="sxs-lookup"><span data-stu-id="ae823-p104">Indicates if the thread is locked. Set to `true` to disallow posting.</span></span>|

## <a name="response"></a><span data-ttu-id="ae823-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae823-126">Response</span></span>

<span data-ttu-id="ae823-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [conversationThread](../resources/conversationthread.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ae823-127">If successful, this method returns a `200 OK` response code and updated [conversationThread](../resources/conversationthread.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ae823-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ae823-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ae823-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ae823-129">Request</span></span>
<span data-ttu-id="ae823-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ae823-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_conversationthread"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}
Content-type: application/json
Content-length: 419

{
  "@odata.type":"#Microsoft.OutlookServices.ConversationThread",
  "isLocked": true
}
```
##### <a name="response"></a><span data-ttu-id="ae823-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae823-131">Response</span></span>
<span data-ttu-id="ae823-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ae823-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversationThread"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 419

{
  "toRecipients": [
    {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    }
  ],
  "topic": "topic-value",
  "hasAttachments": true,
  "lastDeliveredDateTime": "datetime-value",
  "uniqueSenders": [
    "uniqueSenders-value"
  ],
  "ccRecipients": [
    {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    }
  ],
  "isLocked": true 
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update conversationthread",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
