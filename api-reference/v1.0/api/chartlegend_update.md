# <a name="update-chartlegend"></a><span data-ttu-id="69659-101">Actualizar chartlegend</span><span class="sxs-lookup"><span data-stu-id="69659-101">Update chartlegend</span></span>

<span data-ttu-id="69659-102">Actualizar las propiedades del objeto chartlegend.</span><span class="sxs-lookup"><span data-stu-id="69659-102">Update the properties of chartlegend object.</span></span>
## <a name="permissions"></a><span data-ttu-id="69659-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="69659-103">Permissions</span></span>
<span data-ttu-id="69659-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="69659-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="69659-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="69659-106">Permission type</span></span>      | <span data-ttu-id="69659-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="69659-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="69659-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="69659-108">Delegated (work or school account)</span></span> | <span data-ttu-id="69659-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="69659-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="69659-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="69659-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="69659-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="69659-111">Not supported.</span></span>    |
|<span data-ttu-id="69659-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="69659-112">Application</span></span> | <span data-ttu-id="69659-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="69659-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="69659-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="69659-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/legend
```
## <a name="optional-request-headers"></a><span data-ttu-id="69659-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="69659-115">Optional request headers</span></span>
| <span data-ttu-id="69659-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="69659-116">Name</span></span>       | <span data-ttu-id="69659-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="69659-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="69659-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="69659-118">Authorization</span></span>  | <span data-ttu-id="69659-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="69659-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="69659-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="69659-121">Request body</span></span>
<span data-ttu-id="69659-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="69659-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="69659-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="69659-125">Property</span></span>     | <span data-ttu-id="69659-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="69659-126">Type</span></span>   |<span data-ttu-id="69659-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="69659-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="69659-128">overlay</span><span class="sxs-lookup"><span data-stu-id="69659-128">overlay</span></span>|<span data-ttu-id="69659-129">boolean</span><span class="sxs-lookup"><span data-stu-id="69659-129">boolean</span></span>|<span data-ttu-id="69659-130">Valor booleano que indica si la leyenda del gráfico debe superponerse al cuerpo principal del gráfico.</span><span class="sxs-lookup"><span data-stu-id="69659-130">Boolean value for whether the chart legend should overlap with the main body of the chart.</span></span>|
|<span data-ttu-id="69659-131">position</span><span class="sxs-lookup"><span data-stu-id="69659-131">position</span></span>|<span data-ttu-id="69659-132">string</span><span class="sxs-lookup"><span data-stu-id="69659-132">string</span></span>|<span data-ttu-id="69659-p104">Representa la posición de la leyenda del gráfico. Valores posibles: `Top`, `Bottom`, `Left`, `Right`, `Corner`, `Custom`.</span><span class="sxs-lookup"><span data-stu-id="69659-p104">Represents the position of the legend on the chart. Possible values are: `Top`, `Bottom`, `Left`, `Right`, `Corner`, `Custom`.</span></span>|
|<span data-ttu-id="69659-135">visible</span><span class="sxs-lookup"><span data-stu-id="69659-135">visible</span></span>|<span data-ttu-id="69659-136">boolean</span><span class="sxs-lookup"><span data-stu-id="69659-136">boolean</span></span>|<span data-ttu-id="69659-137">Valor booleano que representa la visibilidad de un objeto ChartLegend.</span><span class="sxs-lookup"><span data-stu-id="69659-137">A boolean value the represents the visibility of a ChartLegend object.</span></span>|

## <a name="response"></a><span data-ttu-id="69659-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="69659-138">Response</span></span>

<span data-ttu-id="69659-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartLegend](../resources/chartlegend.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="69659-139">If successful, this method returns a `200 OK` response code and updated [ChartLegend](../resources/chartlegend.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="69659-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="69659-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="69659-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="69659-141">Request</span></span>
<span data-ttu-id="69659-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="69659-142">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="69659-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="69659-143">Response</span></span>
<span data-ttu-id="69659-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="69659-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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