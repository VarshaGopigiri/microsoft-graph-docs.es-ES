# <a name="update-rangeformat"></a><span data-ttu-id="8f817-101">Update rangeformat</span><span class="sxs-lookup"><span data-stu-id="8f817-101">Update rangeformat</span></span>

<span data-ttu-id="8f817-102">Actualizar las propiedades del objeto rangeformat.</span><span class="sxs-lookup"><span data-stu-id="8f817-102">Update the properties of rangeformat object.</span></span>
## <a name="permissions"></a><span data-ttu-id="8f817-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="8f817-103">Permissions</span></span>
<span data-ttu-id="8f817-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8f817-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8f817-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8f817-106">Permission type</span></span>      | <span data-ttu-id="8f817-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8f817-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8f817-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8f817-108">Delegated (work or school account)</span></span> | <span data-ttu-id="8f817-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f817-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="8f817-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8f817-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8f817-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8f817-111">Not supported.</span></span>    |
|<span data-ttu-id="8f817-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8f817-112">Application</span></span> | <span data-ttu-id="8f817-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8f817-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="8f817-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8f817-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names(<name>)/range/format
PATCH /workbook/worksheets/{id|name}/range(address='<address>')/format
PATCH /workbook/tables/{id|name}/columns/{id|name}/range/format
```
## <a name="optional-request-headers"></a><span data-ttu-id="8f817-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="8f817-115">Optional request headers</span></span>
| <span data-ttu-id="8f817-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="8f817-116">Name</span></span>       | <span data-ttu-id="8f817-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f817-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="8f817-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="8f817-118">Authorization</span></span>  | <span data-ttu-id="8f817-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8f817-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="8f817-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8f817-121">Request body</span></span>
<span data-ttu-id="8f817-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="8f817-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="8f817-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8f817-125">Property</span></span>     | <span data-ttu-id="8f817-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="8f817-126">Type</span></span>   |<span data-ttu-id="8f817-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f817-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8f817-128">columnWidth</span><span class="sxs-lookup"><span data-stu-id="8f817-128">columnWidth</span></span>|<span data-ttu-id="8f817-129">double</span><span class="sxs-lookup"><span data-stu-id="8f817-129">double</span></span>|<span data-ttu-id="8f817-p104">Obtiene o establece el ancho de todas las columnas del rango. Si los anchos de columna no son uniformes, se devolverá null.</span><span class="sxs-lookup"><span data-stu-id="8f817-p104">Gets or sets the width of all colums within the range. If the column widths are not uniform, null will be returned.</span></span>|
|<span data-ttu-id="8f817-132">horizontalAlignment</span><span class="sxs-lookup"><span data-stu-id="8f817-132">horizontalAlignment</span></span>|<span data-ttu-id="8f817-133">string</span><span class="sxs-lookup"><span data-stu-id="8f817-133">string</span></span>|<span data-ttu-id="8f817-p105">Representa la alineación horizontal del objeto especificado. Valores posibles: `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection`, `Distributed`.</span><span class="sxs-lookup"><span data-stu-id="8f817-p105">Represents the horizontal alignment for the specified object. Possible values are: `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection`, `Distributed`.</span></span>|
|<span data-ttu-id="8f817-136">rowHeight</span><span class="sxs-lookup"><span data-stu-id="8f817-136">rowHeight</span></span>|<span data-ttu-id="8f817-137">double</span><span class="sxs-lookup"><span data-stu-id="8f817-137">double</span></span>|<span data-ttu-id="8f817-p106">Obtiene o establece el alto de todas las filas del rango. Si los altos de fila no son uniformes, se devolverá null.</span><span class="sxs-lookup"><span data-stu-id="8f817-p106">Gets or sets the height of all rows in the range. If the row heights are not uniform null will be returned.</span></span>|
|<span data-ttu-id="8f817-140">verticalAlignment</span><span class="sxs-lookup"><span data-stu-id="8f817-140">verticalAlignment</span></span>|<span data-ttu-id="8f817-141">string</span><span class="sxs-lookup"><span data-stu-id="8f817-141">string</span></span>|<span data-ttu-id="8f817-p107">Representa la alineación vertical del objeto especificado. Valores posibles: `Top`, `Center`, `Bottom`, `Justify`, `Distributed`.</span><span class="sxs-lookup"><span data-stu-id="8f817-p107">Represents the vertical alignment for the specified object. Possible values are: `Top`, `Center`, `Bottom`, `Justify`, `Distributed`.</span></span>|
|<span data-ttu-id="8f817-144">wrapText</span><span class="sxs-lookup"><span data-stu-id="8f817-144">wrapText</span></span>|<span data-ttu-id="8f817-145">boolean</span><span class="sxs-lookup"><span data-stu-id="8f817-145">boolean</span></span>|<span data-ttu-id="8f817-p108">Indica si Excel ajusta el texto del objeto. Un valor null indica que el intervalo no tiene una configuración de ajuste uniforme.</span><span class="sxs-lookup"><span data-stu-id="8f817-p108">Indicates if Excel wraps the text in the object. A null value indicates that the entire range doesn't have uniform wrap setting</span></span>|

## <a name="response"></a><span data-ttu-id="8f817-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f817-148">Response</span></span>

<span data-ttu-id="8f817-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [RangeFormat](../resources/rangeformat.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f817-149">If successful, this method returns a `200 OK` response code and updated [RangeFormat](../resources/rangeformat.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="8f817-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8f817-150">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8f817-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8f817-151">Request</span></span>
<span data-ttu-id="8f817-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8f817-152">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_rangeformat"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/format
Content-type: application/json
Content-length: 96

{
  "columnWidth": 99,
  "horizontalAlignment": "horizontalAlignment-value",
  "rowHeight": 99
}
```
##### <a name="response"></a><span data-ttu-id="8f817-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f817-153">Response</span></span>
<span data-ttu-id="8f817-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8f817-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.rangeFormat"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 96

{
  "columnWidth": 99,
  "horizontalAlignment": "horizontalAlignment-value",
  "rowHeight": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update rangeformat",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->