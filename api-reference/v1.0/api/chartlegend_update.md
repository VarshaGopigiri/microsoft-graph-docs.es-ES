# <a name="update-chartlegend"></a><span data-ttu-id="60336-101">Actualizar chartlegend</span><span class="sxs-lookup"><span data-stu-id="60336-101">Update chartlegend</span></span>

<span data-ttu-id="60336-102">Actualiza las propiedades del objeto chartlegend.</span><span class="sxs-lookup"><span data-stu-id="60336-102">Update the properties of chartlegend object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="60336-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="60336-103">Prerequisites</span></span>
<span data-ttu-id="60336-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="60336-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="60336-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="60336-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="60336-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="60336-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/legend
```
## <a name="optional-request-headers"></a><span data-ttu-id="60336-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="60336-107">Optional request headers</span></span>
| <span data-ttu-id="60336-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="60336-108">Name</span></span>       | <span data-ttu-id="60336-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="60336-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="60336-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="60336-110">Authorization</span></span>  | <span data-ttu-id="60336-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="60336-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="60336-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="60336-113">Request body</span></span>
<span data-ttu-id="60336-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="60336-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="60336-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="60336-117">Property</span></span>     | <span data-ttu-id="60336-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="60336-118">Type</span></span>   |<span data-ttu-id="60336-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="60336-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="60336-120">overlay</span><span class="sxs-lookup"><span data-stu-id="60336-120">overlay</span></span>|<span data-ttu-id="60336-121">boolean</span><span class="sxs-lookup"><span data-stu-id="60336-121">boolean</span></span>|<span data-ttu-id="60336-122">Valor booleano que indica si la leyenda del gráfico debe superponerse al cuerpo principal del gráfico.</span><span class="sxs-lookup"><span data-stu-id="60336-122">Boolean value for whether the chart legend should overlap with the main body of the chart.</span></span>|
|<span data-ttu-id="60336-123">position</span><span class="sxs-lookup"><span data-stu-id="60336-123">position</span></span>|<span data-ttu-id="60336-124">string</span><span class="sxs-lookup"><span data-stu-id="60336-124">string</span></span>|<span data-ttu-id="60336-p103">Representa la posición de la leyenda del gráfico. Valores posibles: `Top`, `Bottom`, `Left`, `Right`, `Corner`, `Custom`.</span><span class="sxs-lookup"><span data-stu-id="60336-p103">Represents the position of the legend on the chart. Possible values are: `Top`, `Bottom`, `Left`, `Right`, `Corner`, `Custom`.</span></span>|
|<span data-ttu-id="60336-127">visible</span><span class="sxs-lookup"><span data-stu-id="60336-127">visible</span></span>|<span data-ttu-id="60336-128">boolean</span><span class="sxs-lookup"><span data-stu-id="60336-128">boolean</span></span>|<span data-ttu-id="60336-129">Valor booleano que representa la visibilidad de un objeto ChartLegend.</span><span class="sxs-lookup"><span data-stu-id="60336-129">A boolean value the represents the visibility of a ChartLegend object.</span></span>|

## <a name="response"></a><span data-ttu-id="60336-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60336-130">Response</span></span>

<span data-ttu-id="60336-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartLegend](../resources/chartlegend.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="60336-131">If successful, this method returns a `200 OK` response code and updated [ChartLegend](../resources/chartlegend.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="60336-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="60336-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="60336-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="60336-133">Request</span></span>
<span data-ttu-id="60336-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="60336-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartlegend"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/legend
Content-type: application/json
Content-length: 72

{
  "visible": true,
  "position": "position-value",
  "overlay": true
}
```
##### <a name="response"></a><span data-ttu-id="60336-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60336-135">Response</span></span>
<span data-ttu-id="60336-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="60336-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartLegend"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 72

{
  "visible": true,
  "position": "position-value",
  "overlay": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chartlegend",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->