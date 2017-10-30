# <a name="range-boundingrect"></a><span data-ttu-id="48242-101">Range: BoundingRect</span><span class="sxs-lookup"><span data-stu-id="48242-101">Range: BoundingRect</span></span>

<span data-ttu-id="48242-p101">Obtiene el objeto de intervalo más pequeño que abarca los intervalos especificados. Por ejemplo, el valor GetBoundingRect de "B2:C5" y "D10:E15" es "B2:E16".</span><span class="sxs-lookup"><span data-stu-id="48242-p101">Gets the smallest range object that encompasses the given ranges. For example, the GetBoundingRect of "B2:C5" and "D10:E15" is "B2:E16".</span></span>
## <a name="permissions"></a><span data-ttu-id="48242-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="48242-104">Permissions</span></span>
<span data-ttu-id="48242-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="48242-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="48242-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="48242-107">Permission type</span></span>      | <span data-ttu-id="48242-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="48242-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="48242-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="48242-109">Delegated (work or school account)</span></span> | <span data-ttu-id="48242-110">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="48242-110">Files.ReadWrite</span></span>    |
|<span data-ttu-id="48242-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="48242-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="48242-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="48242-112">Not supported.</span></span>    |
|<span data-ttu-id="48242-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="48242-113">Application</span></span> | <span data-ttu-id="48242-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="48242-114">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="48242-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="48242-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/BoundingRect
GET /workbook/worksheets/{id|name}/range(address='<address>')/BoundingRect
GET /workbook/tables/{id|name}/columns/{id|name}/range/BoundingRect

```
## <a name="request-headers"></a><span data-ttu-id="48242-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="48242-116">Request headers</span></span>
| <span data-ttu-id="48242-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="48242-117">Name</span></span>       | <span data-ttu-id="48242-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="48242-118">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="48242-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="48242-119">Authorization</span></span>  | <span data-ttu-id="48242-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="48242-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="48242-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="48242-122">Request body</span></span>
<span data-ttu-id="48242-123">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="48242-123">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="48242-124">Parámetro</span><span class="sxs-lookup"><span data-stu-id="48242-124">Parameter</span></span>    | <span data-ttu-id="48242-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="48242-125">Type</span></span>   |<span data-ttu-id="48242-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="48242-126">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="48242-127">anotherRange</span><span class="sxs-lookup"><span data-stu-id="48242-127">anotherRange</span></span>|<span data-ttu-id="48242-128">string</span><span class="sxs-lookup"><span data-stu-id="48242-128">string</span></span>|<span data-ttu-id="48242-129">Objeto o dirección de intervalo o nombre de intervalo.</span><span class="sxs-lookup"><span data-stu-id="48242-129">The range object or address or range name.</span></span>|

## <a name="response"></a><span data-ttu-id="48242-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48242-130">Response</span></span>

<span data-ttu-id="48242-131">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="48242-131">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="48242-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="48242-132">Example</span></span>
<span data-ttu-id="48242-133">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="48242-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="48242-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48242-134">Request</span></span>
<span data-ttu-id="48242-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="48242-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_boundingrect"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/BoundingRect
Content-type: application/json
Content-length: 42

{
  "anotherRange": "anotherRange-value"
}
```

##### <a name="response"></a><span data-ttu-id="48242-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48242-136">Response</span></span>
<span data-ttu-id="48242-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="48242-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.range"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 169

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnIndex": 99,
  "valueTypes": "valueTypes-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: BoundingRect",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->