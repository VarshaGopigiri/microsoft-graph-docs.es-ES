# <a name="list-conversations"></a><span data-ttu-id="4f4bc-101">List conversations</span><span class="sxs-lookup"><span data-stu-id="4f4bc-101">List conversations</span></span>
<span data-ttu-id="4f4bc-102">Recupera la lista de conversaciones en este grupo.</span><span class="sxs-lookup"><span data-stu-id="4f4bc-102">Retrieve the list of conversations in this group.</span></span>

## <a name="permissions"></a><span data-ttu-id="4f4bc-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="4f4bc-103">Permissions</span></span>
<span data-ttu-id="4f4bc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4f4bc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="4f4bc-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4f4bc-106">Permission type</span></span>      | <span data-ttu-id="4f4bc-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4f4bc-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4f4bc-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4f4bc-108">Delegated (work or school account)</span></span> | <span data-ttu-id="4f4bc-109">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4f4bc-109">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="4f4bc-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4f4bc-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4f4bc-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4f4bc-111">Not supported.</span></span>    |
|<span data-ttu-id="4f4bc-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4f4bc-112">Application</span></span> | <span data-ttu-id="4f4bc-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4f4bc-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="4f4bc-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4f4bc-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/conversations
```

## <a name="optional-query-parameters"></a><span data-ttu-id="4f4bc-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="4f4bc-115">Optional query parameters</span></span>
<span data-ttu-id="4f4bc-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4f4bc-116">This method supports the [OData Query Parameters](http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="4f4bc-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4f4bc-117">Request headers</span></span>
| <span data-ttu-id="4f4bc-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f4bc-118">Header</span></span>       | <span data-ttu-id="4f4bc-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4f4bc-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="4f4bc-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="4f4bc-120">Authorization</span></span>  | <span data-ttu-id="4f4bc-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4f4bc-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="4f4bc-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4f4bc-123">Request body</span></span>
<span data-ttu-id="4f4bc-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4f4bc-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4f4bc-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4f4bc-125">Response</span></span>
<span data-ttu-id="4f4bc-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Conversation](../resources/conversation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4f4bc-126">If successful, this method returns a `200 OK` response code and collection of [Conversation](../resources/conversation.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4f4bc-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4f4bc-127">Example</span></span>
#### <a name="request"></a><span data-ttu-id="4f4bc-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4f4bc-128">Request</span></span>
<span data-ttu-id="4f4bc-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4f4bc-129">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>
<!-- {
  "blockType": "request",
  "name": "get_conversations"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/conversations
```
#### <a name="response"></a><span data-ttu-id="4f4bc-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4f4bc-130">Response</span></span>
<span data-ttu-id="4f4bc-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4f4bc-131">Here is an example of the response.</span></span>
><span data-ttu-id="4f4bc-132">**Nota:** Se puede reducir el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="4f4bc-132">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="4f4bc-133">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4f4bc-133">All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversation",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 262

{
  "value": [
    {
      "topic": "topic-value",
      "hasAttachments": true,
      "lastDeliveredDateTime": "datetime-value",
      "uniqueSenders": [
        "uniqueSenders-value"
      ],
      "preview": "preview-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List conversations",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->