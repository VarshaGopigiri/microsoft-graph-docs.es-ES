# <a name="get-post"></a><span data-ttu-id="15d08-101">Obtener publicación</span><span class="sxs-lookup"><span data-stu-id="15d08-101">Get post</span></span>

<span data-ttu-id="15d08-p101">Obtiene las propiedades y relaciones de una publicación de un hilo determinado. Puede especificar la conversación primaria y el hilo, o bien, especificar el hilo sin hacer referencia a la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="15d08-p101">Get the properties and relationships of a post in a specified thread. You can specify both the parent conversation and the thread, or, you can specify the thread without referencing the parent conversation.</span></span>

<span data-ttu-id="15d08-104">Dado que el recurso **post** admite [extensiones](../../../concepts/extensibility_overview.md), también puede utilizar la operación `GET` para obtener propiedades personalizadas y datos de extensión en una instancia **post**.</span><span class="sxs-lookup"><span data-stu-id="15d08-104">Since the **post** resource supports [extensions](../../../concepts/extensibility_overview.md), you can also use the `GET` operation to get custom properties and extension data in a **post** instance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="15d08-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="15d08-105">Prerequisites</span></span>
<span data-ttu-id="15d08-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="15d08-106">One of the following **scopes** is required to execute this API:</span></span>

<span data-ttu-id="15d08-107">*Group.Read.All*, *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="15d08-107">*Group.Read.All*, *Group.Readwrite.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="15d08-108">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="15d08-108">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}/posts/{id}
GET /groups/{id}/conversations/{id}/threads/{id}/posts/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="15d08-109">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="15d08-109">Optional query parameters</span></span>
<span data-ttu-id="15d08-110">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="15d08-110">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="15d08-111">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="15d08-111">Request headers</span></span>
| <span data-ttu-id="15d08-112">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15d08-112">Header</span></span>       | <span data-ttu-id="15d08-113">Valor</span><span class="sxs-lookup"><span data-stu-id="15d08-113">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="15d08-114">Authorization</span><span class="sxs-lookup"><span data-stu-id="15d08-114">Authorization</span></span>  | <span data-ttu-id="15d08-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="15d08-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="15d08-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="15d08-117">Request body</span></span>
<span data-ttu-id="15d08-118">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="15d08-118">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="15d08-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="15d08-119">Response</span></span>

<span data-ttu-id="15d08-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [post](../resources/post.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="15d08-120">If successful, this method returns a `200 OK` response code and [post](../resources/post.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="15d08-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="15d08-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="15d08-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="15d08-122">Request</span></span>
<span data-ttu-id="15d08-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="15d08-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_post"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/posts/{id}
```
##### <a name="response"></a><span data-ttu-id="15d08-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="15d08-124">Response</span></span>
<span data-ttu-id="15d08-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="15d08-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.post"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 414

{
  "body": {
    "contentType": "",
    "content": "content-value"
  },
  "receivedDateTime": "datetime-value",
  "hasAttachments": true,
  "from": {
    "emailAddress": {
      "name": "name-value",
      "address": "address-value"
    }
  },
  "sender": {
    "emailAddress": {
      "name": "name-value",
      "address": "address-value"
    }
  }
}
```

## <a name="see-also"></a><span data-ttu-id="15d08-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="15d08-128">See also</span></span>

- [<span data-ttu-id="15d08-129">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="15d08-129">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="15d08-130">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="15d08-130">Add custom data to users using open extensions (preview)</span></span>](../../../concepts/extensibility_open_users.md)
<!--
- [Add custom data to groups using schema extensions (preview)](../../../concepts/extensibility_schema_groups.md)
-->


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get post",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
