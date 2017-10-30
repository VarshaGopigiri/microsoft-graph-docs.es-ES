# <a name="list-borders"></a><span data-ttu-id="c6049-101">List borders</span><span class="sxs-lookup"><span data-stu-id="c6049-101">List borders</span></span>

<span data-ttu-id="c6049-102">Recuperar una lista de objetos rangeborder.</span><span class="sxs-lookup"><span data-stu-id="c6049-102">Retrieve a list of rangeborder objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="c6049-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="c6049-103">Permissions</span></span>
<span data-ttu-id="c6049-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c6049-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c6049-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c6049-106">Permission type</span></span>      | <span data-ttu-id="c6049-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c6049-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c6049-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c6049-108">Delegated (work or school account)</span></span> | <span data-ttu-id="c6049-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c6049-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c6049-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c6049-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c6049-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c6049-111">Not supported.</span></span>    |
|<span data-ttu-id="c6049-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c6049-112">Application</span></span> | <span data-ttu-id="c6049-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c6049-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c6049-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c6049-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/format/borders
GET /workbook/worksheets/{id|name}/range(address='<address>')/format/borders
GET /workbook/tables/{id|name}/columns/{id|name}/range/format/borders
```
## <a name="optional-query-parameters"></a><span data-ttu-id="c6049-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c6049-115">Optional query parameters</span></span>
<span data-ttu-id="c6049-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c6049-116">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="c6049-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c6049-117">Request headers</span></span>
| <span data-ttu-id="c6049-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="c6049-118">Name</span></span>      |<span data-ttu-id="c6049-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6049-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="c6049-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="c6049-120">Authorization</span></span>  | <span data-ttu-id="c6049-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c6049-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c6049-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c6049-123">Request body</span></span>
<span data-ttu-id="c6049-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c6049-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c6049-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6049-125">Response</span></span>

<span data-ttu-id="c6049-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [RangeBorder](../resources/rangeborder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c6049-126">If successful, this method returns a `200 OK` response code and collection of [RangeBorder](../resources/rangeborder.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c6049-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6049-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c6049-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c6049-128">Request</span></span>
<span data-ttu-id="c6049-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c6049-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_borders"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/format/borders
```
##### <a name="response"></a><span data-ttu-id="c6049-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6049-130">Response</span></span>
<span data-ttu-id="c6049-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c6049-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.rangeBorder",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 185

{
  "value": [
    {
      "id": "id-value",
      "color": "color-value",
      "style": "style-value",
      "sideIndex": "sideIndex-value",
      "weight": "weight-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List borders",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->