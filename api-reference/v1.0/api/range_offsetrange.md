# <a name="range-offsetrange"></a><span data-ttu-id="50164-101">Range: OffsetRange</span><span class="sxs-lookup"><span data-stu-id="50164-101">Range: OffsetRange</span></span>

<span data-ttu-id="50164-p101">Obtiene un objeto que representa un intervalo desplazado con respecto al intervalo especificado. La dimensión del intervalo devuelto coincidirá con este intervalo. Si el intervalo resultante se fuerza fuera de los límites de la cuadrícula de la hoja de cálculo, se producirá una excepción.</span><span class="sxs-lookup"><span data-stu-id="50164-p101">Gets an object which represents a range that's offset from the specified range. The dimension of the returned range will match this range. If the resulting range is forced outside the bounds of the worksheet grid, an exception will be thrown.</span></span>
## <a name="permissions"></a><span data-ttu-id="50164-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="50164-105">Permissions</span></span>
<span data-ttu-id="50164-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="50164-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="50164-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="50164-108">Permission type</span></span>      | <span data-ttu-id="50164-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="50164-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="50164-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="50164-110">Delegated (work or school account)</span></span> | <span data-ttu-id="50164-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="50164-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="50164-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="50164-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="50164-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="50164-113">Not supported.</span></span>    |
|<span data-ttu-id="50164-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="50164-114">Application</span></span> | <span data-ttu-id="50164-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="50164-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="50164-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="50164-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/OffsetRange
GET /workbook/worksheets/{id|name}/range(address='<address>')/OffsetRange
GET /workbook/tables/{id|name}/columns/{id|name}/range/OffsetRange

```
## <a name="request-headers"></a><span data-ttu-id="50164-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="50164-117">Request headers</span></span>
| <span data-ttu-id="50164-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="50164-118">Name</span></span>       | <span data-ttu-id="50164-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="50164-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="50164-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="50164-120">Authorization</span></span>  | <span data-ttu-id="50164-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="50164-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="50164-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="50164-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="50164-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="50164-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="50164-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="50164-126">Request body</span></span>
<span data-ttu-id="50164-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="50164-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="50164-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="50164-128">Parameter</span></span>    | <span data-ttu-id="50164-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="50164-129">Type</span></span>   |<span data-ttu-id="50164-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="50164-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="50164-131">rowOffset</span><span class="sxs-lookup"><span data-stu-id="50164-131">rowOffset</span></span>|<span data-ttu-id="50164-132">number</span><span class="sxs-lookup"><span data-stu-id="50164-132">number</span></span>|<span data-ttu-id="50164-p105">Número de filas (número positivo, negativo o 0) que debe desplazarse el intervalo. Los valores positivos desplazan hacia abajo, mientras que los negativos lo hacen hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="50164-p105">The number of rows (positive, negative, or 0) by which the range is to be offset. Positive values are offset downward, and negative values are offset upward.</span></span>|
|<span data-ttu-id="50164-135">columnOffset</span><span class="sxs-lookup"><span data-stu-id="50164-135">columnOffset</span></span>|<span data-ttu-id="50164-136">number</span><span class="sxs-lookup"><span data-stu-id="50164-136">number</span></span>|<span data-ttu-id="50164-p106">Número de columnas (número positivo, negativo o 0) que debe desplazarse el rango. Los valores positivos desplazan hacia la derecha, mientras que los negativos lo hacen hacia la izquierda.</span><span class="sxs-lookup"><span data-stu-id="50164-p106">The number of columns (positive, negative, or 0) by which the range is to be offset. Positive values are offset to the right, and negative values are offset to the left.</span></span>|

## <a name="response"></a><span data-ttu-id="50164-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50164-139">Response</span></span>

<span data-ttu-id="50164-140">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="50164-140">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="50164-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="50164-141">Example</span></span>
<span data-ttu-id="50164-142">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="50164-142">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="50164-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="50164-143">Request</span></span>
<span data-ttu-id="50164-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="50164-144">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="50164-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50164-145">Response</span></span>
<span data-ttu-id="50164-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="50164-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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