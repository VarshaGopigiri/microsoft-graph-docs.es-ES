# <a name="update-chartfont"></a><span data-ttu-id="699ba-101">Actualizar chartfont</span><span class="sxs-lookup"><span data-stu-id="699ba-101">Update chartfont</span></span>

<span data-ttu-id="699ba-102">Actualiza las propiedades del objeto chartfont.</span><span class="sxs-lookup"><span data-stu-id="699ba-102">Update the properties of chartfont object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="699ba-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="699ba-103">Prerequisites</span></span>
<span data-ttu-id="699ba-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="699ba-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="699ba-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="699ba-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="699ba-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="699ba-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis/format/font
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/seriesaxis/format/font
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/categoryaxis/format/font
```
## <a name="optional-request-headers"></a><span data-ttu-id="699ba-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="699ba-107">Optional request headers</span></span>
| <span data-ttu-id="699ba-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="699ba-108">Name</span></span>       | <span data-ttu-id="699ba-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="699ba-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="699ba-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="699ba-110">Authorization</span></span>  | <span data-ttu-id="699ba-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="699ba-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="699ba-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="699ba-113">Request body</span></span>
<span data-ttu-id="699ba-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="699ba-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="699ba-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="699ba-117">Property</span></span>     | <span data-ttu-id="699ba-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="699ba-118">Type</span></span>   |<span data-ttu-id="699ba-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="699ba-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="699ba-120">bold</span><span class="sxs-lookup"><span data-stu-id="699ba-120">bold</span></span>|<span data-ttu-id="699ba-121">boolean</span><span class="sxs-lookup"><span data-stu-id="699ba-121">boolean</span></span>|<span data-ttu-id="699ba-122">Representa el estado de negrita de la fuente.</span><span class="sxs-lookup"><span data-stu-id="699ba-122">Represents the bold status of font.</span></span>|
|<span data-ttu-id="699ba-123">color</span><span class="sxs-lookup"><span data-stu-id="699ba-123">color</span></span>|<span data-ttu-id="699ba-124">string</span><span class="sxs-lookup"><span data-stu-id="699ba-124">string</span></span>|<span data-ttu-id="699ba-p103">Representación del código de color HTML del color del texto. Por ejemplo, #FF0000 representa el rojo.</span><span class="sxs-lookup"><span data-stu-id="699ba-p103">HTML color code representation of the text color. E.g. #FF0000 represents Red.</span></span>|
|<span data-ttu-id="699ba-128">italic</span><span class="sxs-lookup"><span data-stu-id="699ba-128">italic</span></span>|<span data-ttu-id="699ba-129">boolean</span><span class="sxs-lookup"><span data-stu-id="699ba-129">boolean</span></span>|<span data-ttu-id="699ba-130">Representa el estado de cursiva de la fuente.</span><span class="sxs-lookup"><span data-stu-id="699ba-130">Represents the italic status of the font.</span></span>|
|<span data-ttu-id="699ba-131">name</span><span class="sxs-lookup"><span data-stu-id="699ba-131">name</span></span>|<span data-ttu-id="699ba-132">string</span><span class="sxs-lookup"><span data-stu-id="699ba-132">string</span></span>|<span data-ttu-id="699ba-133">Nombre de fuente (por ejemplo, "Calibri")</span><span class="sxs-lookup"><span data-stu-id="699ba-133">Font name (e.g. "Calibri")</span></span>|
|<span data-ttu-id="699ba-134">Tamaño</span><span class="sxs-lookup"><span data-stu-id="699ba-134">size</span></span>|<span data-ttu-id="699ba-135">Double</span><span class="sxs-lookup"><span data-stu-id="699ba-135">double</span></span>|<span data-ttu-id="699ba-136">Tamaño de la fuente (por ejemplo, 11).</span><span class="sxs-lookup"><span data-stu-id="699ba-136">Size of the font (e.g. 11)</span></span>|
|<span data-ttu-id="699ba-137">Subrayado</span><span class="sxs-lookup"><span data-stu-id="699ba-137">underline</span></span>|<span data-ttu-id="699ba-138">cadena</span><span class="sxs-lookup"><span data-stu-id="699ba-138">string</span></span>|<span data-ttu-id="699ba-p104">Tipo de subrayado aplicado a la fuente. Valores posibles: `None`, `Single`.</span><span class="sxs-lookup"><span data-stu-id="699ba-p104">Type of underline applied to the font. Possible values are: `None`, `Single`.</span></span>|

## <a name="response"></a><span data-ttu-id="699ba-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="699ba-141">Response</span></span>

<span data-ttu-id="699ba-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartFont](../resources/chartfont.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="699ba-142">If successful, this method returns a `200 OK` response code and updated [ChartFont](../resources/chartfont.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="699ba-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="699ba-143">Example</span></span>
##### <a name="request"></a><span data-ttu-id="699ba-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="699ba-144">Request</span></span>
<span data-ttu-id="699ba-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="699ba-145">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartfont"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis/format/font
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
##### <a name="response"></a><span data-ttu-id="699ba-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="699ba-146">Response</span></span>
<span data-ttu-id="699ba-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="699ba-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartFont"
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