# <a name="range-offsetrange"></a><span data-ttu-id="71f6c-101">Range: OffsetRange</span><span class="sxs-lookup"><span data-stu-id="71f6c-101">Range: OffsetRange</span></span>

<span data-ttu-id="71f6c-p101">Obtiene un objeto que representa un intervalo desplazado con respecto al intervalo especificado. La dimensión del intervalo devuelto coincidirá con este intervalo. Si el intervalo resultante se fuerza fuera de los límites de la cuadrícula de la hoja de cálculo, se producirá una excepción.</span><span class="sxs-lookup"><span data-stu-id="71f6c-p101">Gets an object which represents a range that's offset from the specified range. The dimension of the returned range will match this range. If the resulting range is forced outside the bounds of the worksheet grid, an exception will be thrown.</span></span>
## <a name="permissions"></a><span data-ttu-id="71f6c-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="71f6c-105">Permissions</span></span>
<span data-ttu-id="71f6c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="71f6c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="71f6c-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="71f6c-108">Permission type</span></span>      | <span data-ttu-id="71f6c-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="71f6c-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="71f6c-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="71f6c-110">Delegated (work or school account)</span></span> | <span data-ttu-id="71f6c-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="71f6c-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="71f6c-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="71f6c-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="71f6c-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71f6c-113">Not supported.</span></span>    |
|<span data-ttu-id="71f6c-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="71f6c-114">Application</span></span> | <span data-ttu-id="71f6c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71f6c-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="71f6c-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="71f6c-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/OffsetRange
GET /workbook/worksheets/{id|name}/range(address='<address>')/OffsetRange
GET /workbook/tables/{id|name}/columns/{id|name}/range/OffsetRange

```
## <a name="request-headers"></a><span data-ttu-id="71f6c-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="71f6c-117">Request headers</span></span>
| <span data-ttu-id="71f6c-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="71f6c-118">Name</span></span>       | <span data-ttu-id="71f6c-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="71f6c-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="71f6c-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="71f6c-120">Authorization</span></span>  | <span data-ttu-id="71f6c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="71f6c-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="71f6c-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="71f6c-123">Request body</span></span>
<span data-ttu-id="71f6c-124">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="71f6c-124">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="71f6c-125">Parámetro</span><span class="sxs-lookup"><span data-stu-id="71f6c-125">Parameter</span></span>    | <span data-ttu-id="71f6c-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="71f6c-126">Type</span></span>   |<span data-ttu-id="71f6c-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="71f6c-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="71f6c-128">rowOffset</span><span class="sxs-lookup"><span data-stu-id="71f6c-128">rowOffset</span></span>|<span data-ttu-id="71f6c-129">number</span><span class="sxs-lookup"><span data-stu-id="71f6c-129">number</span></span>|<span data-ttu-id="71f6c-p104">Número de filas (número positivo, negativo o 0) que debe desplazarse el intervalo. Los valores positivos desplazan hacia abajo, mientras que los negativos lo hacen hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="71f6c-p104">The number of rows (positive, negative, or 0) by which the range is to be offset. Positive values are offset downward, and negative values are offset upward.</span></span>|
|<span data-ttu-id="71f6c-132">columnOffset</span><span class="sxs-lookup"><span data-stu-id="71f6c-132">columnOffset</span></span>|<span data-ttu-id="71f6c-133">number</span><span class="sxs-lookup"><span data-stu-id="71f6c-133">number</span></span>|<span data-ttu-id="71f6c-p105">Número de columnas (número positivo, negativo o 0) que debe desplazarse el rango. Los valores positivos desplazan hacia la derecha, mientras que los negativos lo hacen hacia la izquierda.</span><span class="sxs-lookup"><span data-stu-id="71f6c-p105">The number of columns (positive, negative, or 0) by which the range is to be offset. Positive values are offset to the right, and negative values are offset to the left.</span></span>|

## <a name="response"></a><span data-ttu-id="71f6c-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71f6c-136">Response</span></span>

<span data-ttu-id="71f6c-137">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71f6c-137">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="71f6c-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71f6c-138">Example</span></span>
<span data-ttu-id="71f6c-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="71f6c-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="71f6c-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="71f6c-140">Request</span></span>
<span data-ttu-id="71f6c-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="71f6c-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_offsetrange"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/OffsetRange
Content-type: application/json
Content-length: 49

{
  "rowOffset": {
  },
  "columnOffset": {
  }
}
```

##### <a name="response"></a><span data-ttu-id="71f6c-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71f6c-142">Response</span></span>
<span data-ttu-id="71f6c-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="71f6c-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: OffsetRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->