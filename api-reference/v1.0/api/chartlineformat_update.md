# <a name="update-chartlineformat"></a><span data-ttu-id="e403e-101">Actualizar chartlineformat</span><span class="sxs-lookup"><span data-stu-id="e403e-101">Update chartlineformat</span></span>

<span data-ttu-id="e403e-102">Actualizar las propiedades del objeto chartlineformat.</span><span class="sxs-lookup"><span data-stu-id="e403e-102">Update the properties of chartlineformat object.</span></span>
## <a name="permissions"></a><span data-ttu-id="e403e-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="e403e-103">Permissions</span></span>
<span data-ttu-id="e403e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e403e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e403e-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e403e-106">Permission type</span></span>      | <span data-ttu-id="e403e-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e403e-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e403e-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e403e-108">Delegated (work or school account)</span></span> | <span data-ttu-id="e403e-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e403e-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="e403e-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e403e-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e403e-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e403e-111">Not supported.</span></span>    |
|<span data-ttu-id="e403e-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e403e-112">Application</span></span> | <span data-ttu-id="e403e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e403e-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e403e-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e403e-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/seriesAxis/format/line
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/categoryaxis/format/line
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/seriesAxis/majorgridlines/format/line
```
## <a name="optional-request-headers"></a><span data-ttu-id="e403e-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="e403e-115">Optional request headers</span></span>
| <span data-ttu-id="e403e-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="e403e-116">Name</span></span>       | <span data-ttu-id="e403e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e403e-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="e403e-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="e403e-118">Authorization</span></span>  | <span data-ttu-id="e403e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e403e-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e403e-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="e403e-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="e403e-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="e403e-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="e403e-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e403e-124">Request body</span></span>
<span data-ttu-id="e403e-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="e403e-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="e403e-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e403e-128">Property</span></span>     | <span data-ttu-id="e403e-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="e403e-129">Type</span></span>   |<span data-ttu-id="e403e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="e403e-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e403e-131">color</span><span class="sxs-lookup"><span data-stu-id="e403e-131">color</span></span>|<span data-ttu-id="e403e-132">cadena</span><span class="sxs-lookup"><span data-stu-id="e403e-132">string</span></span>|<span data-ttu-id="e403e-133">Código de color HTML que representa el color de las líneas del gráfico.</span><span class="sxs-lookup"><span data-stu-id="e403e-133">HTML color code representing the color of lines in the chart.</span></span>|

## <a name="response"></a><span data-ttu-id="e403e-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e403e-134">Response</span></span>

<span data-ttu-id="e403e-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [WorkbookChartLineFormat](../resources/chartlineformat.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e403e-135">If successful, this method returns a `200 OK` response code and updated [message](../resources/chartlineformat.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e403e-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e403e-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e403e-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e403e-137">Request</span></span>
<span data-ttu-id="e403e-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e403e-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartlineformat"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/axes/seriesAxis/format/line
Content-type: application/json
Content-length: 28

{
  "color": "color-value"
}
```
##### <a name="response"></a><span data-ttu-id="e403e-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e403e-139">Response</span></span>
<span data-ttu-id="e403e-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e403e-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartLineFormat"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 28

{
  "color": "color-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chartlineformat",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->