# <a name="update-chartfont"></a><span data-ttu-id="6ae76-101">Actualizar chartfont</span><span class="sxs-lookup"><span data-stu-id="6ae76-101">Update chartfont</span></span>

<span data-ttu-id="6ae76-102">Actualizar las propiedades del objeto chartfont.</span><span class="sxs-lookup"><span data-stu-id="6ae76-102">Update the properties of chartfont object.</span></span>
## <a name="permissions"></a><span data-ttu-id="6ae76-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="6ae76-103">Permissions</span></span>
<span data-ttu-id="6ae76-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6ae76-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6ae76-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6ae76-106">Permission type</span></span>      | <span data-ttu-id="6ae76-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6ae76-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6ae76-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6ae76-108">Delegated (work or school account)</span></span> | <span data-ttu-id="6ae76-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6ae76-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="6ae76-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6ae76-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6ae76-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ae76-111">Not supported.</span></span>    |
|<span data-ttu-id="6ae76-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6ae76-112">Application</span></span> | <span data-ttu-id="6ae76-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ae76-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6ae76-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6ae76-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/valueAxis/format/font
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/seriesAxis/format/font
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/categoryaxis/format/font
```
## <a name="optional-request-headers"></a><span data-ttu-id="6ae76-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="6ae76-115">Optional request headers</span></span>
| <span data-ttu-id="6ae76-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="6ae76-116">Name</span></span>       | <span data-ttu-id="6ae76-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ae76-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="6ae76-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="6ae76-118">Authorization</span></span>  | <span data-ttu-id="6ae76-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6ae76-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6ae76-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="6ae76-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="6ae76-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="6ae76-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="6ae76-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6ae76-124">Request body</span></span>
<span data-ttu-id="6ae76-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="6ae76-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="6ae76-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6ae76-128">Property</span></span>     | <span data-ttu-id="6ae76-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ae76-129">Type</span></span>   |<span data-ttu-id="6ae76-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ae76-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6ae76-131">bold</span><span class="sxs-lookup"><span data-stu-id="6ae76-131">bold</span></span>|<span data-ttu-id="6ae76-132">booleano</span><span class="sxs-lookup"><span data-stu-id="6ae76-132">boolean</span></span>|<span data-ttu-id="6ae76-133">Representa el estado de negrita de la fuente.</span><span class="sxs-lookup"><span data-stu-id="6ae76-133">Represents the bold status of font.</span></span>|
|<span data-ttu-id="6ae76-134">color</span><span class="sxs-lookup"><span data-stu-id="6ae76-134">color</span></span>|<span data-ttu-id="6ae76-135">cadena</span><span class="sxs-lookup"><span data-stu-id="6ae76-135">string</span></span>|<span data-ttu-id="6ae76-p105">Representación del código de color HTML del color del texto. Por ejemplo, #FF0000 representa el rojo.</span><span class="sxs-lookup"><span data-stu-id="6ae76-p105">HTML color code representation of the text color. E.g. #FF0000 represents Red.</span></span>|
|<span data-ttu-id="6ae76-139">italic</span><span class="sxs-lookup"><span data-stu-id="6ae76-139">italic</span></span>|<span data-ttu-id="6ae76-140">booleano</span><span class="sxs-lookup"><span data-stu-id="6ae76-140">boolean</span></span>|<span data-ttu-id="6ae76-141">Representa el estado de cursiva de la fuente.</span><span class="sxs-lookup"><span data-stu-id="6ae76-141">Represents the italic status of the font.</span></span>|
|<span data-ttu-id="6ae76-142">name</span><span class="sxs-lookup"><span data-stu-id="6ae76-142">name</span></span>|<span data-ttu-id="6ae76-143">cadena</span><span class="sxs-lookup"><span data-stu-id="6ae76-143">string</span></span>|<span data-ttu-id="6ae76-144">Nombre de fuente (por ejemplo, "Calibri")</span><span class="sxs-lookup"><span data-stu-id="6ae76-144">Font name (e.g. "Calibri")</span></span>|
|<span data-ttu-id="6ae76-145">Tamaño</span><span class="sxs-lookup"><span data-stu-id="6ae76-145">size</span></span>|<span data-ttu-id="6ae76-146">doble</span><span class="sxs-lookup"><span data-stu-id="6ae76-146">double</span></span>|<span data-ttu-id="6ae76-147">Tamaño de la fuente (por ejemplo, 11).</span><span class="sxs-lookup"><span data-stu-id="6ae76-147">Size of the font (e.g. 11)</span></span>|
|<span data-ttu-id="6ae76-148">underline</span><span class="sxs-lookup"><span data-stu-id="6ae76-148">underline</span></span>|<span data-ttu-id="6ae76-149">cadena</span><span class="sxs-lookup"><span data-stu-id="6ae76-149">string</span></span>|<span data-ttu-id="6ae76-150">Tipo de subrayado aplicado a la fuente.</span><span class="sxs-lookup"><span data-stu-id="6ae76-150">Returns or sets the type of underline applied to the font.</span></span> <span data-ttu-id="6ae76-151">Los valores posibles son: `None`, `Single`.</span><span class="sxs-lookup"><span data-stu-id="6ae76-151">The possible values are:</span></span>|

## <a name="response"></a><span data-ttu-id="6ae76-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ae76-152">Response</span></span>

<span data-ttu-id="6ae76-153">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [WorkbookChartFont](../resources/chartfont.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ae76-153">If successful, this method returns a `200 OK` response code and updated [message](../resources/chartfont.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6ae76-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ae76-154">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6ae76-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ae76-155">Request</span></span>
<span data-ttu-id="6ae76-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6ae76-156">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartfont"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/axes/valueAxis/format/font
Content-type: application/json
Content-length: 134

{
  "bold": true,
  "color": "color-value",
  "italic": true,
  "name": "name-value",
  "size": 99,
  "underline": "underline-value"
}
```
##### <a name="response"></a><span data-ttu-id="6ae76-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ae76-157">Response</span></span>
<span data-ttu-id="6ae76-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6ae76-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartFont"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 134

{
  "bold": true,
  "color": "color-value",
  "italic": true,
  "name": "name-value",
  "size": 99,
  "underline": "underline-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chartfont",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->