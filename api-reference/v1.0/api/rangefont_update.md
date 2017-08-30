# <a name="update-rangefont"></a><span data-ttu-id="8402c-101">Update rangefont</span><span class="sxs-lookup"><span data-stu-id="8402c-101">Update rangefont</span></span>

<span data-ttu-id="8402c-102">Actualizar las propiedades del objeto rangefont.</span><span class="sxs-lookup"><span data-stu-id="8402c-102">Update the properties of rangefont object.</span></span>
## <a name="permissions"></a><span data-ttu-id="8402c-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="8402c-103">Permissions</span></span>
<span data-ttu-id="8402c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8402c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8402c-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8402c-106">Permission type</span></span>      | <span data-ttu-id="8402c-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8402c-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8402c-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8402c-108">Delegated (work or school account)</span></span> | <span data-ttu-id="8402c-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8402c-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="8402c-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8402c-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8402c-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8402c-111">Not supported.</span></span>    |
|<span data-ttu-id="8402c-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8402c-112">Application</span></span> | <span data-ttu-id="8402c-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8402c-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="8402c-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8402c-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names(<name>)/range/format/font
PATCH /workbook/worksheets/{id|name}/range(<address>)/format/font
PATCH /workbook/tables/{id|name}/columns/{id|name}/range/format/font
```
## <a name="optional-request-headers"></a><span data-ttu-id="8402c-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="8402c-115">Optional request headers</span></span>
| <span data-ttu-id="8402c-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="8402c-116">Name</span></span>       | <span data-ttu-id="8402c-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="8402c-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="8402c-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="8402c-118">Authorization</span></span>  | <span data-ttu-id="8402c-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8402c-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="8402c-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8402c-121">Request body</span></span>
<span data-ttu-id="8402c-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="8402c-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="8402c-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8402c-125">Property</span></span>     | <span data-ttu-id="8402c-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="8402c-126">Type</span></span>   |<span data-ttu-id="8402c-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="8402c-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8402c-128">bold</span><span class="sxs-lookup"><span data-stu-id="8402c-128">bold</span></span>|<span data-ttu-id="8402c-129">boolean</span><span class="sxs-lookup"><span data-stu-id="8402c-129">boolean</span></span>|<span data-ttu-id="8402c-130">Representa el estado de negrita de la fuente.</span><span class="sxs-lookup"><span data-stu-id="8402c-130">Represents the bold status of font.</span></span>|
|<span data-ttu-id="8402c-131">color</span><span class="sxs-lookup"><span data-stu-id="8402c-131">color</span></span>|<span data-ttu-id="8402c-132">string</span><span class="sxs-lookup"><span data-stu-id="8402c-132">string</span></span>|<span data-ttu-id="8402c-p104">Representación del código de color HTML del color del texto. Por ejemplo, #FF0000 representa el rojo.</span><span class="sxs-lookup"><span data-stu-id="8402c-p104">HTML color code representation of the text color. E.g. #FF0000 represents Red.</span></span>|
|<span data-ttu-id="8402c-136">italic</span><span class="sxs-lookup"><span data-stu-id="8402c-136">italic</span></span>|<span data-ttu-id="8402c-137">boolean</span><span class="sxs-lookup"><span data-stu-id="8402c-137">boolean</span></span>|<span data-ttu-id="8402c-138">Representa el estado de cursiva de la fuente.</span><span class="sxs-lookup"><span data-stu-id="8402c-138">Represents the italic status of the font.</span></span>|
|<span data-ttu-id="8402c-139">name</span><span class="sxs-lookup"><span data-stu-id="8402c-139">name</span></span>|<span data-ttu-id="8402c-140">string</span><span class="sxs-lookup"><span data-stu-id="8402c-140">string</span></span>|<span data-ttu-id="8402c-141">Nombre de fuente (por ejemplo, "Calibri")</span><span class="sxs-lookup"><span data-stu-id="8402c-141">Font name (e.g. "Calibri")</span></span>|
|<span data-ttu-id="8402c-142">Tamaño</span><span class="sxs-lookup"><span data-stu-id="8402c-142">size</span></span>|<span data-ttu-id="8402c-143">Double</span><span class="sxs-lookup"><span data-stu-id="8402c-143">double</span></span>|<span data-ttu-id="8402c-144">Tamaño de fuente</span><span class="sxs-lookup"><span data-stu-id="8402c-144">Font size.</span></span>|
|<span data-ttu-id="8402c-145">underline</span><span class="sxs-lookup"><span data-stu-id="8402c-145">underline</span></span>|<span data-ttu-id="8402c-146">string</span><span class="sxs-lookup"><span data-stu-id="8402c-146">string</span></span>|<span data-ttu-id="8402c-p105">Tipo de subrayado aplicado a la fuente. Valores posibles: `None`, `Single`, `Double`, `SingleAccountant`, `DoubleAccountant`.</span><span class="sxs-lookup"><span data-stu-id="8402c-p105">Type of underline applied to the font. Possible values are: `None`, `Single`, `Double`, `SingleAccountant`, `DoubleAccountant`.</span></span>|

## <a name="response"></a><span data-ttu-id="8402c-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8402c-149">Response</span></span>

<span data-ttu-id="8402c-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [RangeFont](../resources/rangefont.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8402c-150">If successful, this method returns a `200 OK` response code and updated [RangeFont](../resources/rangefont.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="8402c-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8402c-151">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8402c-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8402c-152">Request</span></span>
<span data-ttu-id="8402c-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8402c-153">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_rangefont"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/format/font
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
##### <a name="response"></a><span data-ttu-id="8402c-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8402c-154">Response</span></span>
<span data-ttu-id="8402c-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8402c-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.rangeFont"
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
  "description": "Update rangefont",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->