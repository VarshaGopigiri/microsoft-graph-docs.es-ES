# <a name="get-channel"></a><span data-ttu-id="6847d-101">Obtener el canal</span><span class="sxs-lookup"><span data-stu-id="6847d-101">Get channel</span></span>



<span data-ttu-id="6847d-102">Recuperar las propiedades y relaciones de un [canal](../resources/channel.md).</span><span class="sxs-lookup"><span data-stu-id="6847d-102">Retrieve the properties and relationships of a [channel](../resources/channel.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="6847d-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="6847d-103">Permissions</span></span>
<span data-ttu-id="6847d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6847d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6847d-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6847d-106">Permission type</span></span>      | <span data-ttu-id="6847d-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6847d-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6847d-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6847d-108">Delegated (work or school account)</span></span> | <span data-ttu-id="6847d-109">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6847d-109">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="6847d-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6847d-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6847d-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6847d-111">Not supported.</span></span>    |
|<span data-ttu-id="6847d-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6847d-112">Application</span></span> | <span data-ttu-id="6847d-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6847d-113">Group.Read.All, Group.ReadWrite.All</span></span>    |

## <a name="http-request"></a><span data-ttu-id="6847d-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6847d-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /teams/{id}/channels/{id}

```

## <a name="optional-query-parameters"></a><span data-ttu-id="6847d-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6847d-115">Optional query parameters</span></span>

<span data-ttu-id="6847d-116">Este método admite la $filter, $select, y $expanda [parámetros de consulta de OData](../../../concepts/query_parameters.md) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6847d-116">This method supports the $filter, $select, and $expand [OData query parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6847d-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6847d-117">Request headers</span></span>
| <span data-ttu-id="6847d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6847d-118">Header</span></span>       | <span data-ttu-id="6847d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6847d-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="6847d-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="6847d-120">Authorization</span></span>  | <span data-ttu-id="6847d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6847d-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="6847d-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6847d-123">Request body</span></span>
<span data-ttu-id="6847d-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6847d-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6847d-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6847d-125">Response</span></span>

<span data-ttu-id="6847d-126">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto de [canal](../resources/channel.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6847d-126">If successful, this method returns a `200 OK` response code and a [channel](../resources/channel.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6847d-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6847d-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6847d-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6847d-128">Request</span></span>
<span data-ttu-id="6847d-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6847d-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_channel"
}-->
```http
GET https://graph.microsoft.com/beta/teams/{id}/channels/{id}
```
##### <a name="response"></a><span data-ttu-id="6847d-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6847d-130">Response</span></span>
<span data-ttu-id="6847d-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6847d-131">Here is an example of the response.</span></span> 

><span data-ttu-id="6847d-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6847d-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.channel"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 201

{
    "description": "description-value",
    "displayName": "display-name-value",
    "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
