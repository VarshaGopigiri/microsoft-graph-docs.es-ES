# <a name="update-conversationthread"></a><span data-ttu-id="c916a-101">Update conversationthread</span><span class="sxs-lookup"><span data-stu-id="c916a-101">Update conversationthread</span></span>

<span data-ttu-id="c916a-102">Bloquea o desbloquea un hilo para permitir o impedir futuras publicaciones en el hilo.</span><span class="sxs-lookup"><span data-stu-id="c916a-102">Lock or unlock a thread, to allow or avoid further posting to the thread.</span></span>
## <a name="permissions"></a><span data-ttu-id="c916a-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="c916a-103">Permissions</span></span>
<span data-ttu-id="c916a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c916a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c916a-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c916a-106">Permission type</span></span>      | <span data-ttu-id="c916a-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c916a-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c916a-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c916a-108">Delegated (work or school account)</span></span> | <span data-ttu-id="c916a-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c916a-109">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="c916a-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c916a-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c916a-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c916a-111">Not supported.</span></span>    |
|<span data-ttu-id="c916a-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c916a-112">Application</span></span> | <span data-ttu-id="c916a-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c916a-113">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c916a-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c916a-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /groups/{id}/threads/{id}
PATCH /groups/{id}/conversations/{id}/threads/{id}

```
## <a name="request-headers"></a><span data-ttu-id="c916a-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c916a-115">Request headers</span></span>
| <span data-ttu-id="c916a-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c916a-116">Header</span></span>       | <span data-ttu-id="c916a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c916a-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c916a-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="c916a-118">Authorization</span></span>  | <span data-ttu-id="c916a-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c916a-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="c916a-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c916a-121">Content-Type</span></span>  | <span data-ttu-id="c916a-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c916a-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c916a-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c916a-124">Request body</span></span>
<span data-ttu-id="c916a-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="c916a-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="c916a-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c916a-128">Property</span></span>     | <span data-ttu-id="c916a-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="c916a-129">Type</span></span>   |<span data-ttu-id="c916a-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="c916a-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c916a-131">isLocked</span><span class="sxs-lookup"><span data-stu-id="c916a-131">isLocked</span></span>|<span data-ttu-id="c916a-132">Boolean</span><span class="sxs-lookup"><span data-stu-id="c916a-132">Boolean</span></span>|<span data-ttu-id="c916a-p105">Indica si el hilo está bloqueado. Establecer en `true` para impedir publicaciones.</span><span class="sxs-lookup"><span data-stu-id="c916a-p105">Indicates if the thread is locked. Set to `true` to disallow posting.</span></span>|

## <a name="response"></a><span data-ttu-id="c916a-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c916a-135">Response</span></span>

<span data-ttu-id="c916a-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [conversationThread](../resources/conversationthread.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c916a-136">If successful, this method returns a `200 OK` response code and updated [conversationThread](../resources/conversationthread.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c916a-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c916a-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c916a-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c916a-138">Request</span></span>
<span data-ttu-id="c916a-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c916a-139">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="c916a-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c916a-140">Response</span></span>
<span data-ttu-id="c916a-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c916a-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
