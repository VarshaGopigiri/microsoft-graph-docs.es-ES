# <a name="list-channels"></a><span data-ttu-id="a2d42-101">Canales de lista</span><span class="sxs-lookup"><span data-stu-id="a2d42-101">List channels</span></span>



<span data-ttu-id="a2d42-102">Recuperar la lista de [canales](../resources/channel.md) en este equipo.</span><span class="sxs-lookup"><span data-stu-id="a2d42-102">Retrieve the list of [channels](../resources/channel.md) in this team.</span></span>

## <a name="permissions"></a><span data-ttu-id="a2d42-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="a2d42-103">Permissions</span></span>
<span data-ttu-id="a2d42-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a2d42-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="a2d42-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a2d42-106">Permission type</span></span>      | <span data-ttu-id="a2d42-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a2d42-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a2d42-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a2d42-108">Delegated (work or school account)</span></span> | <span data-ttu-id="a2d42-109">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a2d42-109">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="a2d42-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a2d42-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a2d42-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2d42-111">Not supported.</span></span>    |
|<span data-ttu-id="a2d42-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a2d42-112">Application</span></span> | <span data-ttu-id="a2d42-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a2d42-113">Group.Read.All, Group.ReadWrite.All</span></span>    |

## <a name="http-request"></a><span data-ttu-id="a2d42-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a2d42-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /teams/{id}/channels
```

## <a name="optional-query-parameters"></a><span data-ttu-id="a2d42-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a2d42-115">Optional query parameters</span></span>
<span data-ttu-id="a2d42-116">Este método admite la $filter, $select, y $expanda [parámetros de consulta de OData](../../../concepts/query_parameters.md) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2d42-116">This method supports the $filter, $select, and $expand [OData query parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a2d42-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a2d42-117">Request headers</span></span>
| <span data-ttu-id="a2d42-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2d42-118">Header</span></span>       | <span data-ttu-id="a2d42-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a2d42-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a2d42-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="a2d42-120">Authorization</span></span>  | <span data-ttu-id="a2d42-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a2d42-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a2d42-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a2d42-123">Request body</span></span>
<span data-ttu-id="a2d42-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a2d42-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a2d42-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2d42-125">Response</span></span>

<span data-ttu-id="a2d42-126">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [canal](../resources/channel.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2d42-126">If successful, this method returns a `200 OK` response code and collection of [Channel](../resources/channel.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a2d42-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a2d42-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a2d42-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a2d42-128">Request</span></span>
<span data-ttu-id="a2d42-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2d42-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_channels"
}-->
```http
GET https://graph.microsoft.com/beta/teams/{id}/channels
```
##### <a name="response"></a><span data-ttu-id="a2d42-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2d42-130">Response</span></span>
<span data-ttu-id="a2d42-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a2d42-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.channel",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 262

{
  "value": [
    {
      "description": "description-value",
      "displayName": "display-name-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List channels",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
