# <a name="get-chartpoint"></a><span data-ttu-id="d6388-101">Get ChartPoint</span><span class="sxs-lookup"><span data-stu-id="d6388-101">Get ChartPoint</span></span>

<span data-ttu-id="d6388-102">Recuperar las propiedades y relaciones del objeto chartpoint.</span><span class="sxs-lookup"><span data-stu-id="d6388-102">Retrieve the properties and relationships of chartpoint object.</span></span>
## <a name="permissions"></a><span data-ttu-id="d6388-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="d6388-103">Permissions</span></span>
<span data-ttu-id="d6388-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d6388-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d6388-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d6388-106">Permission type</span></span>      | <span data-ttu-id="d6388-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d6388-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d6388-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d6388-108">Delegated (work or school account)</span></span> | <span data-ttu-id="d6388-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d6388-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="d6388-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d6388-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d6388-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d6388-111">Not supported.</span></span>    |
|<span data-ttu-id="d6388-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d6388-112">Application</span></span> | <span data-ttu-id="d6388-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d6388-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d6388-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d6388-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/charts(<name>)/series(<undefined>)/points(<undefined>)
```
## <a name="optional-query-parameters"></a><span data-ttu-id="d6388-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="d6388-115">Optional query parameters</span></span>
<span data-ttu-id="d6388-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d6388-116">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="d6388-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d6388-117">Request headers</span></span>
| <span data-ttu-id="d6388-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="d6388-118">Name</span></span>      |<span data-ttu-id="d6388-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6388-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="d6388-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="d6388-120">Authorization</span></span>  | <span data-ttu-id="d6388-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d6388-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d6388-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d6388-123">Request body</span></span>
<span data-ttu-id="d6388-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d6388-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d6388-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d6388-125">Response</span></span>

<span data-ttu-id="d6388-126">Si se ejecuta correctamente, este método devuelve código de respuesta `200 OK` y el objeto [ChartPoint](../resources/chartpoint.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d6388-126">If successful, this method returns a `200 OK` response code and [ChartPoint](../resources/chartpoint.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d6388-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d6388-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d6388-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d6388-128">Request</span></span>
<span data-ttu-id="d6388-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d6388-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_chartpoint"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/series(<undefined>)/points(<undefined>)
```
##### <a name="response"></a><span data-ttu-id="d6388-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d6388-130">Response</span></span>
<span data-ttu-id="d6388-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d6388-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartPoint"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 20

{
  "value": {
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get ChartPoint",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->