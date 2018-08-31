# <a name="update-chartaxis"></a><span data-ttu-id="34c67-101">Actualizar chartaxis</span><span class="sxs-lookup"><span data-stu-id="34c67-101">Update chartaxis</span></span>

<span data-ttu-id="34c67-102">Actualizar las propiedades del objeto chartaxis.</span><span class="sxs-lookup"><span data-stu-id="34c67-102">Update the properties of chartaxis object.</span></span>
## <a name="permissions"></a><span data-ttu-id="34c67-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="34c67-103">Permissions</span></span>
<span data-ttu-id="34c67-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="34c67-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="34c67-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="34c67-106">Permission type</span></span>      | <span data-ttu-id="34c67-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="34c67-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="34c67-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="34c67-108">Delegated (work or school account)</span></span> | <span data-ttu-id="34c67-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34c67-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="34c67-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="34c67-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="34c67-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="34c67-111">Not supported.</span></span>    |
|<span data-ttu-id="34c67-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="34c67-112">Application</span></span> | <span data-ttu-id="34c67-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="34c67-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="34c67-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="34c67-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/valueAxis
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/seriesAxis
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/categoryaxis
```
## <a name="optional-request-headers"></a><span data-ttu-id="34c67-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="34c67-115">Optional request headers</span></span>
| <span data-ttu-id="34c67-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="34c67-116">Name</span></span>       | <span data-ttu-id="34c67-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="34c67-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="34c67-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="34c67-118">Authorization</span></span>  | <span data-ttu-id="34c67-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="34c67-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="34c67-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="34c67-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="34c67-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="34c67-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="34c67-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="34c67-124">Request body</span></span>
<span data-ttu-id="34c67-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="34c67-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="34c67-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="34c67-128">Property</span></span>     | <span data-ttu-id="34c67-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="34c67-129">Type</span></span>   |<span data-ttu-id="34c67-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="34c67-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="34c67-131">majorUnit</span><span class="sxs-lookup"><span data-stu-id="34c67-131">majorUnit</span></span>|<span data-ttu-id="34c67-132">Json</span><span class="sxs-lookup"><span data-stu-id="34c67-132">Json</span></span>|<span data-ttu-id="34c67-p105">Representa el intervalo entre dos marcas de graduación principales. Puede establecerse en un valor numérico o en una cadena vacía.  El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="34c67-p105">Represents the interval between two major tick marks. Can be set to a numeric value or an empty string.  The returned value is always a number.</span></span>|
|<span data-ttu-id="34c67-136">maximum</span><span class="sxs-lookup"><span data-stu-id="34c67-136">maximum</span></span>|<span data-ttu-id="34c67-137">Json</span><span class="sxs-lookup"><span data-stu-id="34c67-137">Json</span></span>|<span data-ttu-id="34c67-p106">Representa el valor máximo del eje de valores.  Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos).  El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="34c67-p106">Represents the maximum value on the value axis.  Can be set to a numeric value or an empty string (for automatic axis values).  The returned value is always a number.</span></span>|
|<span data-ttu-id="34c67-141">minimum</span><span class="sxs-lookup"><span data-stu-id="34c67-141">minimum</span></span>|<span data-ttu-id="34c67-142">Json</span><span class="sxs-lookup"><span data-stu-id="34c67-142">Json</span></span>|<span data-ttu-id="34c67-p107">Representa el valor mínimo del eje de valores. Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos). El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="34c67-p107">Represents the minimum value on the value axis. Can be set to a numeric value or an empty string (for automatic axis values).  The returned value is always a number.</span></span>|
|<span data-ttu-id="34c67-146">minorUnit</span><span class="sxs-lookup"><span data-stu-id="34c67-146">minorUnit</span></span>|<span data-ttu-id="34c67-147">Json</span><span class="sxs-lookup"><span data-stu-id="34c67-147">Json</span></span>|<span data-ttu-id="34c67-p108">Representa el intervalo entre dos marcas de graduación secundarias. Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos). El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="34c67-p108">Represents the interval between two minor tick marks. "Can be set to a numeric value or an empty string (for automatic axis values). The returned value is always a number.</span></span>|

## <a name="response"></a><span data-ttu-id="34c67-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34c67-151">Response</span></span>

<span data-ttu-id="34c67-152">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [WorkbookChartAxis](../resources/chartaxis.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="34c67-152">If successful, this method returns a `200 OK` response code and updated [message](../resources/chartaxis.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="34c67-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="34c67-153">Example</span></span>
##### <a name="request"></a><span data-ttu-id="34c67-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="34c67-154">Request</span></span>
<span data-ttu-id="34c67-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="34c67-155">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartaxis"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/axes/valueAxis
Content-type: application/json
Content-length: 64

{
  "majorUnit": {
  },
  "maximum": {
  },
  "minimum": {
  }
}
```
##### <a name="response"></a><span data-ttu-id="34c67-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34c67-156">Response</span></span>
<span data-ttu-id="34c67-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="34c67-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartAxis"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 64

{
  "majorUnit": {
  },
  "maximum": {
  },
  "minimum": {
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chartaxis",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->