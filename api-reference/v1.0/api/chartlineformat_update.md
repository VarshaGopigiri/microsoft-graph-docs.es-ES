# <a name="update-chartlineformat"></a><span data-ttu-id="753f9-101">Actualizar chartlineformat</span><span class="sxs-lookup"><span data-stu-id="753f9-101">Update chartlineformat</span></span>

<span data-ttu-id="753f9-102">Actualizar las propiedades del objeto chartlineformat.</span><span class="sxs-lookup"><span data-stu-id="753f9-102">Update the properties of chartlineformat object.</span></span>
## <a name="permissions"></a><span data-ttu-id="753f9-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="753f9-103">Permissions</span></span>
<span data-ttu-id="753f9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="753f9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="753f9-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="753f9-106">Permission type</span></span>      | <span data-ttu-id="753f9-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="753f9-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="753f9-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="753f9-108">Delegated (work or school account)</span></span> | <span data-ttu-id="753f9-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="753f9-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="753f9-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="753f9-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="753f9-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="753f9-111">Not supported.</span></span>    |
|<span data-ttu-id="753f9-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="753f9-112">Application</span></span> | <span data-ttu-id="753f9-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="753f9-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="753f9-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="753f9-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/seriesaxis/format/line
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/categoryaxis/format/line
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/seriesaxis/majorgridlines/format/line
```
## <a name="optional-request-headers"></a><span data-ttu-id="753f9-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="753f9-115">Optional request headers</span></span>
| <span data-ttu-id="753f9-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="753f9-116">Name</span></span>       | <span data-ttu-id="753f9-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="753f9-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="753f9-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="753f9-118">Authorization</span></span>  | <span data-ttu-id="753f9-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="753f9-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="753f9-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="753f9-121">Request body</span></span>
<span data-ttu-id="753f9-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="753f9-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="753f9-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="753f9-125">Property</span></span>     | <span data-ttu-id="753f9-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="753f9-126">Type</span></span>   |<span data-ttu-id="753f9-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="753f9-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="753f9-128">color</span><span class="sxs-lookup"><span data-stu-id="753f9-128">color</span></span>|<span data-ttu-id="753f9-129">string</span><span class="sxs-lookup"><span data-stu-id="753f9-129">string</span></span>|<span data-ttu-id="753f9-130">Código de color HTML que representa el color de las líneas del gráfico.</span><span class="sxs-lookup"><span data-stu-id="753f9-130">HTML color code representing the color of lines in the chart.</span></span>|

## <a name="response"></a><span data-ttu-id="753f9-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="753f9-131">Response</span></span>

<span data-ttu-id="753f9-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartLineFormat](../resources/chartlineformat.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="753f9-132">If successful, this method returns a `200 OK` response code and updated [ChartLineFormat](../resources/chartlineformat.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="753f9-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="753f9-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="753f9-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="753f9-134">Request</span></span>
<span data-ttu-id="753f9-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="753f9-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartlineformat"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/axes/seriesaxis/format/line
Content-type: application/json
Content-length: 28

{
  "color": "color-value"
}
```
##### <a name="response"></a><span data-ttu-id="753f9-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="753f9-136">Response</span></span>
<span data-ttu-id="753f9-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="753f9-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartLineFormat"
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