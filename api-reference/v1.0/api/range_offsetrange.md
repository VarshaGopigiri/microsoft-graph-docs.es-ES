# <a name="range-offsetrange"></a><span data-ttu-id="d5bfe-101">Range: OffsetRange</span><span class="sxs-lookup"><span data-stu-id="d5bfe-101">Range: OffsetRange</span></span>

<span data-ttu-id="d5bfe-p101">Obtiene un objeto que representa un intervalo desplazado con respecto al intervalo especificado. La dimensión del intervalo devuelto coincidirá con este intervalo. Si el intervalo resultante se fuerza fuera de los límites de la cuadrícula de la hoja de cálculo, se producirá una excepción.</span><span class="sxs-lookup"><span data-stu-id="d5bfe-p101">Gets an object which represents a range that's offset from the specified range. The dimension of the returned range will match this range. If the resulting range is forced outside the bounds of the worksheet grid, an exception will be thrown.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d5bfe-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d5bfe-105">Prerequisites</span></span>
<span data-ttu-id="d5bfe-106">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="d5bfe-106">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="d5bfe-107">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5bfe-107">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="d5bfe-108">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d5bfe-108">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/OffsetRange
GET /workbook/worksheets/{id|name}/range(<address>)/OffsetRange
GET /workbook/tables/{id|name}/columns/{id|name}/range/OffsetRange

```
## <a name="request-headers"></a><span data-ttu-id="d5bfe-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d5bfe-109">Request headers</span></span>
| <span data-ttu-id="d5bfe-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="d5bfe-110">Name</span></span>       | <span data-ttu-id="d5bfe-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5bfe-111">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="d5bfe-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="d5bfe-112">Authorization</span></span>  | <span data-ttu-id="d5bfe-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d5bfe-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="d5bfe-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d5bfe-115">Request body</span></span>
<span data-ttu-id="d5bfe-116">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="d5bfe-116">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="d5bfe-117">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d5bfe-117">Parameter</span></span>    | <span data-ttu-id="d5bfe-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="d5bfe-118">Type</span></span>   |<span data-ttu-id="d5bfe-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5bfe-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d5bfe-120">rowOffset</span><span class="sxs-lookup"><span data-stu-id="d5bfe-120">rowOffset</span></span>|<span data-ttu-id="d5bfe-121">number</span><span class="sxs-lookup"><span data-stu-id="d5bfe-121">number</span></span>|<span data-ttu-id="d5bfe-p103">Número de filas (número positivo, negativo o 0) que debe desplazarse el intervalo. Los valores positivos desplazan hacia abajo, mientras que los negativos lo hacen hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="d5bfe-p103">The number of rows (positive, negative, or 0) by which the range is to be offset. Positive values are offset downward, and negative values are offset upward.</span></span>|
|<span data-ttu-id="d5bfe-124">columnOffset</span><span class="sxs-lookup"><span data-stu-id="d5bfe-124">columnOffset</span></span>|<span data-ttu-id="d5bfe-125">number</span><span class="sxs-lookup"><span data-stu-id="d5bfe-125">number</span></span>|<span data-ttu-id="d5bfe-p104">Número de columnas (número positivo, negativo o 0) que debe desplazarse el rango. Los valores positivos desplazan hacia la derecha, mientras que los negativos lo hacen hacia la izquierda.</span><span class="sxs-lookup"><span data-stu-id="d5bfe-p104">The number of columns (positive, negative, or 0) by which the range is to be offset. Positive values are offset to the right, and negative values are offset to the left.</span></span>|

## <a name="response"></a><span data-ttu-id="d5bfe-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d5bfe-128">Response</span></span>

<span data-ttu-id="d5bfe-129">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d5bfe-129">If successful, this method returns `200, OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d5bfe-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d5bfe-130">Example</span></span>
<span data-ttu-id="d5bfe-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d5bfe-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="d5bfe-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d5bfe-132">Request</span></span>
<span data-ttu-id="d5bfe-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d5bfe-133">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="d5bfe-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d5bfe-134">Response</span></span>
<span data-ttu-id="d5bfe-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d5bfe-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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