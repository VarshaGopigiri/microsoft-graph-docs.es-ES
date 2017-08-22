# <a name="update-chart"></a><span data-ttu-id="ad174-101">Actualizar gráfico</span><span class="sxs-lookup"><span data-stu-id="ad174-101">Update chart</span></span>

<span data-ttu-id="ad174-102">Actualiza las propiedades del objeto chart.</span><span class="sxs-lookup"><span data-stu-id="ad174-102">Update the properties of chart object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ad174-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ad174-103">Prerequisites</span></span>
<span data-ttu-id="ad174-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="ad174-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="ad174-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ad174-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="ad174-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ad174-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)
```
## <a name="optional-request-headers"></a><span data-ttu-id="ad174-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="ad174-107">Optional request headers</span></span>
| <span data-ttu-id="ad174-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="ad174-108">Name</span></span>       | <span data-ttu-id="ad174-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad174-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="ad174-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="ad174-110">Authorization</span></span>  | <span data-ttu-id="ad174-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ad174-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="ad174-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ad174-113">Request body</span></span>
<span data-ttu-id="ad174-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="ad174-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="ad174-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ad174-117">Property</span></span>     | <span data-ttu-id="ad174-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad174-118">Type</span></span>   |<span data-ttu-id="ad174-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad174-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ad174-120">height</span><span class="sxs-lookup"><span data-stu-id="ad174-120">height</span></span>|<span data-ttu-id="ad174-121">Double</span><span class="sxs-lookup"><span data-stu-id="ad174-121">double</span></span>|<span data-ttu-id="ad174-122">Representa el alto, en puntos, del objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="ad174-122">Represents the height, in points, of the chart object.</span></span>|
|<span data-ttu-id="ad174-123">left</span><span class="sxs-lookup"><span data-stu-id="ad174-123">left</span></span>|<span data-ttu-id="ad174-124">Double</span><span class="sxs-lookup"><span data-stu-id="ad174-124">double</span></span>|<span data-ttu-id="ad174-125">Distancia, en puntos, desde el lado izquierdo del gráfico hasta el origen de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="ad174-125">The distance, in points, from the left side of the chart to the worksheet origin.</span></span>|
|<span data-ttu-id="ad174-126">name</span><span class="sxs-lookup"><span data-stu-id="ad174-126">name</span></span>|<span data-ttu-id="ad174-127">string</span><span class="sxs-lookup"><span data-stu-id="ad174-127">string</span></span>|<span data-ttu-id="ad174-128">Representa el nombre de un objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="ad174-128">Represents the name of a chart object.</span></span>|
|<span data-ttu-id="ad174-129">top</span><span class="sxs-lookup"><span data-stu-id="ad174-129">top</span></span>|<span data-ttu-id="ad174-130">Double</span><span class="sxs-lookup"><span data-stu-id="ad174-130">double</span></span>|<span data-ttu-id="ad174-131">Representa la distancia, en puntos, desde el borde superior del objeto hasta la parte superior de la fila 1 (en una hoja de cálculo) o la parte superior del área del gráfico (en un gráfico).</span><span class="sxs-lookup"><span data-stu-id="ad174-131">Represents the distance, in points, from the top edge of the object to the top of row 1 (on a worksheet) or the top of the chart area (on a chart).</span></span>|
|<span data-ttu-id="ad174-132">width</span><span class="sxs-lookup"><span data-stu-id="ad174-132">width</span></span>|<span data-ttu-id="ad174-133">double</span><span class="sxs-lookup"><span data-stu-id="ad174-133">double</span></span>|<span data-ttu-id="ad174-134">Representa el ancho, en puntos, del objeto graph.</span><span class="sxs-lookup"><span data-stu-id="ad174-134">Represents the width, in points, of the chart object.</span></span>|

## <a name="response"></a><span data-ttu-id="ad174-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad174-135">Response</span></span>

<span data-ttu-id="ad174-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Chart](../resources/chart.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ad174-136">If successful, this method returns a `200 OK` response code and updated [Chart](../resources/chart.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ad174-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ad174-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ad174-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ad174-138">Request</span></span>
<span data-ttu-id="ad174-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ad174-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chart"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)
Content-type: application/json
Content-length: 52

{
  "height": 99,
  "left": 99
}
```
##### <a name="response"></a><span data-ttu-id="ad174-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad174-140">Response</span></span>
<span data-ttu-id="ad174-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ad174-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chart"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 52

{
  "id": "id-value",
  "height": 99,
  "left": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chart",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->