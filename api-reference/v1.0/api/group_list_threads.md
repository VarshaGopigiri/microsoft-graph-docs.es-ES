# <a name="list-threads"></a><span data-ttu-id="45c35-101">List threads</span><span class="sxs-lookup"><span data-stu-id="45c35-101">List threads</span></span>
<span data-ttu-id="45c35-102">Obtenga todos los hilos de un grupo.</span><span class="sxs-lookup"><span data-stu-id="45c35-102">Get all the threads of a group.</span></span>

><span data-ttu-id="45c35-103">Nota: También puede [obtener todos los hilos de una conversación](conversation_list_threads.md).</span><span class="sxs-lookup"><span data-stu-id="45c35-103">Note: You can also [get all the threads of a conversation](conversation_list_threads.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="45c35-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="45c35-104">Permissions</span></span>
<span data-ttu-id="45c35-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="45c35-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="45c35-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="45c35-107">Permission type</span></span>      | <span data-ttu-id="45c35-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="45c35-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="45c35-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="45c35-109">Delegated (work or school account)</span></span> | <span data-ttu-id="45c35-110">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="45c35-110">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="45c35-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="45c35-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="45c35-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="45c35-112">Not supported.</span></span>    |
|<span data-ttu-id="45c35-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="45c35-113">Application</span></span> | <span data-ttu-id="45c35-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="45c35-114">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="45c35-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="45c35-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads
```

## <a name="optional-query-parameters"></a><span data-ttu-id="45c35-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="45c35-116">Optional query parameters</span></span>
<span data-ttu-id="45c35-117">Este método admite los [parámetros de consulta de OData](../../../concepts/query_parameters.md) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="45c35-117">This method supports the [OData Query Parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="45c35-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="45c35-118">Request headers</span></span>
| <span data-ttu-id="45c35-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45c35-119">Header</span></span>       | <span data-ttu-id="45c35-120">Valor</span><span class="sxs-lookup"><span data-stu-id="45c35-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="45c35-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="45c35-121">Authorization</span></span>  | <span data-ttu-id="45c35-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="45c35-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="45c35-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="45c35-124">Request body</span></span>
<span data-ttu-id="45c35-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="45c35-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="45c35-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="45c35-126">Response</span></span>
<span data-ttu-id="45c35-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [ConversationThread](../resources/conversationthread.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="45c35-127">If successful, this method returns a `200 OK` response code and collection of [ConversationThread](../resources/conversationthread.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="45c35-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="45c35-128">Example</span></span>
#### <a name="request"></a><span data-ttu-id="45c35-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="45c35-129">Request</span></span>
<span data-ttu-id="45c35-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="45c35-130">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>
<!-- {
  "blockType": "request",
  "name": "get_threads"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/threads
```

#### <a name="response"></a><span data-ttu-id="45c35-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="45c35-131">Response</span></span>
<span data-ttu-id="45c35-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="45c35-132">Here is an example of the response.</span></span>
><span data-ttu-id="45c35-133">**Nota:** Se puede reducir el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="45c35-133">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="45c35-134">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="45c35-134">All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversationThread",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 536

{
  "value": [
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
      ]
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List threads",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
