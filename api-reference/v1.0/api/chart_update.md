# <a name="update-chart"></a><span data-ttu-id="ce758-101">Actualizar gráfico</span><span class="sxs-lookup"><span data-stu-id="ce758-101">Update chart</span></span>

<span data-ttu-id="ce758-102">Actualizar las propiedades del objeto chart.</span><span class="sxs-lookup"><span data-stu-id="ce758-102">Update the properties of chart object.</span></span>
## <a name="permissions"></a><span data-ttu-id="ce758-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="ce758-103">Permissions</span></span>
<span data-ttu-id="ce758-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ce758-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ce758-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ce758-106">Permission type</span></span>      | <span data-ttu-id="ce758-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ce758-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ce758-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ce758-108">Delegated (work or school account)</span></span> | <span data-ttu-id="ce758-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ce758-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="ce758-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ce758-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ce758-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ce758-111">Not supported.</span></span>    |
|<span data-ttu-id="ce758-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ce758-112">Application</span></span> | <span data-ttu-id="ce758-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ce758-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ce758-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ce758-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts/{name}
```
## <a name="optional-request-headers"></a><span data-ttu-id="ce758-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="ce758-115">Optional request headers</span></span>
| <span data-ttu-id="ce758-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="ce758-116">Name</span></span>       | <span data-ttu-id="ce758-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce758-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="ce758-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="ce758-118">Authorization</span></span>  | <span data-ttu-id="ce758-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ce758-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ce758-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="ce758-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="ce758-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="ce758-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="ce758-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ce758-124">Request body</span></span>
<span data-ttu-id="ce758-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="ce758-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="ce758-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ce758-128">Property</span></span>     | <span data-ttu-id="ce758-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="ce758-129">Type</span></span>   |<span data-ttu-id="ce758-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce758-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ce758-131">height</span><span class="sxs-lookup"><span data-stu-id="ce758-131">height</span></span>|<span data-ttu-id="ce758-132">doble</span><span class="sxs-lookup"><span data-stu-id="ce758-132">double</span></span>|<span data-ttu-id="ce758-133">Representa el alto, en puntos, del objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="ce758-133">Represents the height, in points, of the chart object.</span></span>|
|<span data-ttu-id="ce758-134">left</span><span class="sxs-lookup"><span data-stu-id="ce758-134">left</span></span>|<span data-ttu-id="ce758-135">doble</span><span class="sxs-lookup"><span data-stu-id="ce758-135">double</span></span>|<span data-ttu-id="ce758-136">Distancia, en puntos, desde el lado izquierdo del gráfico hasta el origen de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="ce758-136">The distance, in points, from the left side of the chart to the worksheet origin.</span></span>|
|<span data-ttu-id="ce758-137">name</span><span class="sxs-lookup"><span data-stu-id="ce758-137">name</span></span>|<span data-ttu-id="ce758-138">cadena</span><span class="sxs-lookup"><span data-stu-id="ce758-138">string</span></span>|<span data-ttu-id="ce758-139">Representa el nombre de un objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="ce758-139">Represents the name of a chart object.</span></span>|
|<span data-ttu-id="ce758-140">top</span><span class="sxs-lookup"><span data-stu-id="ce758-140">top</span></span>|<span data-ttu-id="ce758-141">doble</span><span class="sxs-lookup"><span data-stu-id="ce758-141">double</span></span>|<span data-ttu-id="ce758-142">Representa la distancia, en puntos, desde el borde superior del objeto hasta la parte superior de la fila 1 (en una hoja de cálculo) o la parte superior del área del gráfico (en un gráfico).</span><span class="sxs-lookup"><span data-stu-id="ce758-142">Represents the distance, in points, from the top edge of the object to the top of row 1 (on a worksheet) or the top of the chart area (on a chart).</span></span>|
|<span data-ttu-id="ce758-143">width</span><span class="sxs-lookup"><span data-stu-id="ce758-143">width</span></span>|<span data-ttu-id="ce758-144">doble</span><span class="sxs-lookup"><span data-stu-id="ce758-144">double</span></span>|<span data-ttu-id="ce758-145">Representa el ancho, en puntos, del objeto graph.</span><span class="sxs-lookup"><span data-stu-id="ce758-145">Represents the width, in points, of the chart object.</span></span>|

## <a name="response"></a><span data-ttu-id="ce758-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ce758-146">Response</span></span>

<span data-ttu-id="ce758-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [WorkbookChart](../resources/chart.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce758-147">If successful, this method returns a `200 OK` response code and updated [message](../resources/chart.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ce758-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ce758-148">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ce758-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ce758-149">Request</span></span>
<span data-ttu-id="ce758-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ce758-150">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chart"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}
Content-type: application/json
Content-length: 52

{
  "height": 99,
  "left": 99
}
```
##### <a name="response"></a><span data-ttu-id="ce758-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ce758-151">Response</span></span>
<span data-ttu-id="ce758-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ce758-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChart"
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