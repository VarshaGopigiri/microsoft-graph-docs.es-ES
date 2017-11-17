# <a name="update-chartaxistitle"></a><span data-ttu-id="210b8-101">Actualizar chartaxistitle</span><span class="sxs-lookup"><span data-stu-id="210b8-101">Update chartaxistitle</span></span>

<span data-ttu-id="210b8-102">Actualizar las propiedades del objeto chartaxistitle.</span><span class="sxs-lookup"><span data-stu-id="210b8-102">Update the properties of chartaxistitle object.</span></span>
## <a name="permissions"></a><span data-ttu-id="210b8-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="210b8-103">Permissions</span></span>
<span data-ttu-id="210b8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="210b8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="210b8-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="210b8-106">Permission type</span></span>      | <span data-ttu-id="210b8-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="210b8-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="210b8-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="210b8-108">Delegated (work or school account)</span></span> | <span data-ttu-id="210b8-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="210b8-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="210b8-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="210b8-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="210b8-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="210b8-111">Not supported.</span></span>    |
|<span data-ttu-id="210b8-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="210b8-112">Application</span></span> | <span data-ttu-id="210b8-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="210b8-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="210b8-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="210b8-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis/title
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/seriesaxis/title
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/categoryaxis/title
```
## <a name="optional-request-headers"></a><span data-ttu-id="210b8-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="210b8-115">Optional request headers</span></span>
| <span data-ttu-id="210b8-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="210b8-116">Name</span></span>       | <span data-ttu-id="210b8-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="210b8-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="210b8-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="210b8-118">Authorization</span></span>  | <span data-ttu-id="210b8-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="210b8-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="210b8-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="210b8-121">Request body</span></span>
<span data-ttu-id="210b8-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="210b8-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="210b8-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="210b8-125">Property</span></span>     | <span data-ttu-id="210b8-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="210b8-126">Type</span></span>   |<span data-ttu-id="210b8-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="210b8-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="210b8-128">text</span><span class="sxs-lookup"><span data-stu-id="210b8-128">text</span></span>|<span data-ttu-id="210b8-129">string</span><span class="sxs-lookup"><span data-stu-id="210b8-129">string</span></span>|<span data-ttu-id="210b8-130">Representa el título del eje.</span><span class="sxs-lookup"><span data-stu-id="210b8-130">Represents the axis title.</span></span>|
|<span data-ttu-id="210b8-131">visible</span><span class="sxs-lookup"><span data-stu-id="210b8-131">visible</span></span>|<span data-ttu-id="210b8-132">boolean</span><span class="sxs-lookup"><span data-stu-id="210b8-132">boolean</span></span>|<span data-ttu-id="210b8-133">Valor booleano que especifica la visibilidad del título de un eje.</span><span class="sxs-lookup"><span data-stu-id="210b8-133">A boolean that specifies the visibility of an axis title.</span></span>|

## <a name="response"></a><span data-ttu-id="210b8-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="210b8-134">Response</span></span>

<span data-ttu-id="210b8-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartAxisTitle](../resources/chartaxistitle.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="210b8-135">If successful, this method returns a `200 OK` response code and updated [ChartAxisTitle](../resources/chartaxistitle.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="210b8-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="210b8-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="210b8-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="210b8-137">Request</span></span>
<span data-ttu-id="210b8-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="210b8-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartaxistitle"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis/title
Content-type: application/json
Content-length: 45

{
  "text": "text-value",
  "visible": true
}
```
##### <a name="response"></a><span data-ttu-id="210b8-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="210b8-139">Response</span></span>
<span data-ttu-id="210b8-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="210b8-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartAxisTitle"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 45

{
  "text": "text-value",
  "visible": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chartaxistitle",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->