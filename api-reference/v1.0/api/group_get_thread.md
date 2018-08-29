# <a name="get-conversation-thread"></a><span data-ttu-id="501cc-101">Obtener hilo de conversación</span><span class="sxs-lookup"><span data-stu-id="501cc-101">Get conversation thread</span></span>
<span data-ttu-id="501cc-102">Obtiene un objeto de [conversación](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="501cc-102">Get a [thread](../resources/conversationthread.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="501cc-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="501cc-103">Permissions</span></span>
<span data-ttu-id="501cc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="501cc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="501cc-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="501cc-106">Permission type</span></span>      | <span data-ttu-id="501cc-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="501cc-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="501cc-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="501cc-108">Delegated (work or school account)</span></span> | <span data-ttu-id="501cc-109">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="501cc-109">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="501cc-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="501cc-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="501cc-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="501cc-111">Not supported.</span></span>    |
|<span data-ttu-id="501cc-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="501cc-112">Application</span></span> | <span data-ttu-id="501cc-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="501cc-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="501cc-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="501cc-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="501cc-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="501cc-115">Optional query parameters</span></span>
<span data-ttu-id="501cc-116">Este método admite los [parámetros de consulta de OData](../../../concepts/query_parameters.md) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="501cc-116">This method supports the [OData Query Parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="501cc-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="501cc-117">Request headers</span></span>
| <span data-ttu-id="501cc-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="501cc-118">Header</span></span>       | <span data-ttu-id="501cc-119">Valor</span><span class="sxs-lookup"><span data-stu-id="501cc-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="501cc-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="501cc-120">Authorization</span></span>  | <span data-ttu-id="501cc-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="501cc-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="501cc-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="501cc-123">Request body</span></span>
<span data-ttu-id="501cc-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="501cc-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="501cc-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="501cc-125">Response</span></span>
<span data-ttu-id="501cc-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto de [conversación](../resources/conversationthread.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="501cc-126">If successful, this method returns a `200 OK` response code and a [thread](../resources/conversationthread.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="501cc-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="501cc-127">Example</span></span>
#### <a name="request"></a><span data-ttu-id="501cc-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="501cc-128">Request</span></span>
<span data-ttu-id="501cc-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="501cc-129">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["02bd9fd6-8f93-4758-87c3-1fb73740a315", "AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q=="],
  "name": "get_group_thread"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/threads/AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q==
```

#### <a name="response"></a><span data-ttu-id="501cc-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="501cc-130">Response</span></span>
<span data-ttu-id="501cc-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="501cc-131">The following is an example of the response.</span></span>
><span data-ttu-id="501cc-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="501cc-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversationThread"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 655

{
    "id": "AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q==",
    "topic": "New Training Plans",
    "hasAttachments": false,
    "lastDeliveredDateTime": "2017-07-31T18:59:05Z",
    "uniqueSenders": [
        "HR Taskforce"
    ],
    "preview": "Meeting to plan new trainings.\r\n\r\n\r\n\r\nJoin Microsoft Teams Online Meeting<https://teams.microsoft.com/l/meetup-join/19%3a900876baa3134907b0dcb41a0d220e31%40thread.skype/1501527539926?tenantId=dcd219dd-bc68-4b9b-bf0b-4a33a796be35>",
    "isLocked": false
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get conversation thread",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
