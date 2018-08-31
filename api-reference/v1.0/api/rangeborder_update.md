# <a name="update-rangeborder"></a><span data-ttu-id="d7596-101">Actualizar rangeborder</span><span class="sxs-lookup"><span data-stu-id="d7596-101">Update rangeborder</span></span>

<span data-ttu-id="d7596-102">Actualizar las propiedades del objeto rangeborder.</span><span class="sxs-lookup"><span data-stu-id="d7596-102">Update the properties of rangeborder object.</span></span>
## <a name="permissions"></a><span data-ttu-id="d7596-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="d7596-103">Permissions</span></span>
<span data-ttu-id="d7596-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d7596-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d7596-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d7596-106">Permission type</span></span>      | <span data-ttu-id="d7596-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d7596-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d7596-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d7596-108">Delegated (work or school account)</span></span> | <span data-ttu-id="d7596-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d7596-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="d7596-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d7596-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d7596-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d7596-111">Not supported.</span></span>    |
|<span data-ttu-id="d7596-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d7596-112">Application</span></span> | <span data-ttu-id="d7596-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d7596-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d7596-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d7596-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names/{name}/range/format/borders/{sideIndex}
PATCH /workbook/worksheets/{id|name}/range(address='<address>')/format/borders/{sideIndex}
PATCH /workbook/tables/{id|name}/columns/{id|name}/range/format/borders/{sideIndex}
```
## <a name="optional-request-headers"></a><span data-ttu-id="d7596-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="d7596-115">Optional request headers</span></span>
| <span data-ttu-id="d7596-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="d7596-116">Name</span></span>       | <span data-ttu-id="d7596-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7596-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="d7596-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="d7596-118">Authorization</span></span>  | <span data-ttu-id="d7596-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d7596-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d7596-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="d7596-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="d7596-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="d7596-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="d7596-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d7596-124">Request body</span></span>
<span data-ttu-id="d7596-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="d7596-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="d7596-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d7596-128">Property</span></span>     | <span data-ttu-id="d7596-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="d7596-129">Type</span></span>   |<span data-ttu-id="d7596-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7596-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d7596-131">color</span><span class="sxs-lookup"><span data-stu-id="d7596-131">color</span></span>|<span data-ttu-id="d7596-132">cadena</span><span class="sxs-lookup"><span data-stu-id="d7596-132">string</span></span>|<span data-ttu-id="d7596-133">Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").</span><span class="sxs-lookup"><span data-stu-id="d7596-133">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange").</span></span>|
|<span data-ttu-id="d7596-134">style</span><span class="sxs-lookup"><span data-stu-id="d7596-134">style</span></span>|<span data-ttu-id="d7596-135">cadena</span><span class="sxs-lookup"><span data-stu-id="d7596-135">string</span></span>|<span data-ttu-id="d7596-136">Una de las constantes de estilo de línea que especifica el estilo de línea para el borde.</span><span class="sxs-lookup"><span data-stu-id="d7596-136">One of the constants of line style specifying the line style for the border. Possible values are: , , , , , , , .</span></span> <span data-ttu-id="d7596-137">Los valores posibles son: `None`, `Continuous`, `Dash`, `DashDot`, `DashDotDot`, `Dot`, `Double` y `SlantDashDot`.</span><span class="sxs-lookup"><span data-stu-id="d7596-137">The possible values are `None`, `Continuous`, `Dash`, `DashDot`, `DashDotDot`, `Dot`, `Double`, `SlantDashDot`, , , , or .</span></span>|
|<span data-ttu-id="d7596-138">weight</span><span class="sxs-lookup"><span data-stu-id="d7596-138">weight</span></span>|<span data-ttu-id="d7596-139">cadena</span><span class="sxs-lookup"><span data-stu-id="d7596-139">string</span></span>|<span data-ttu-id="d7596-140">Especifica el grosor del borde que rodea un rango.</span><span class="sxs-lookup"><span data-stu-id="d7596-140">Specifies the weight of the border around a range.</span></span> <span data-ttu-id="d7596-141">Los valores posibles son: `Hairline`, `Thin`, `Medium` y `Thick`.</span><span class="sxs-lookup"><span data-stu-id="d7596-141">The possible values are `Hairline`, `Thin`, `Medium`, `Thick`, , , , , , , , or .</span></span>|

## <a name="response"></a><span data-ttu-id="d7596-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7596-142">Response</span></span>

<span data-ttu-id="d7596-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [WorkbookRangeBorder](../resources/rangeborder.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7596-143">If successful, this method returns a `200 OK` response code and updated [message](../resources/rangeborder.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d7596-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d7596-144">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d7596-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d7596-145">Request</span></span>
<span data-ttu-id="d7596-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d7596-146">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_rangeborder"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/format/borders/{sideIndex}
Content-type: application/json
Content-length: 136

{
  "color": "color-value",
  "style": "style-value",
  "sideIndex": "sideIndex-value",
  "weight": "weight-value"
}
```
##### <a name="response"></a><span data-ttu-id="d7596-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7596-147">Response</span></span>
<span data-ttu-id="d7596-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d7596-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeBorder"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 136

{
  "id": "id-value",
  "color": "color-value",
  "style": "style-value",
  "sideIndex": "sideIndex-value",
  "weight": "weight-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update rangeborder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->