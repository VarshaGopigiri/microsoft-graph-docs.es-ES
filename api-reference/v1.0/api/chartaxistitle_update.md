# <a name="update-chartaxistitle"></a><span data-ttu-id="489d9-101">Actualizar chartaxistitle</span><span class="sxs-lookup"><span data-stu-id="489d9-101">Update chartaxistitle</span></span>

<span data-ttu-id="489d9-102">Actualiza las propiedades del objeto chartaxistitle.</span><span class="sxs-lookup"><span data-stu-id="489d9-102">Update the properties of chartaxistitle object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="489d9-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="489d9-103">Prerequisites</span></span>
<span data-ttu-id="489d9-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="489d9-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="489d9-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="489d9-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="489d9-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="489d9-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis/title
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/seriesaxis/title
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/categoryaxis/title
```
## <a name="optional-request-headers"></a><span data-ttu-id="489d9-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="489d9-107">Optional request headers</span></span>
| <span data-ttu-id="489d9-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="489d9-108">Name</span></span>       | <span data-ttu-id="489d9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="489d9-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="489d9-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="489d9-110">Authorization</span></span>  | <span data-ttu-id="489d9-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="489d9-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="489d9-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="489d9-113">Request body</span></span>
<span data-ttu-id="489d9-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="489d9-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="489d9-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="489d9-117">Property</span></span>     | <span data-ttu-id="489d9-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="489d9-118">Type</span></span>   |<span data-ttu-id="489d9-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="489d9-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="489d9-120">text</span><span class="sxs-lookup"><span data-stu-id="489d9-120">text</span></span>|<span data-ttu-id="489d9-121">string</span><span class="sxs-lookup"><span data-stu-id="489d9-121">string</span></span>|<span data-ttu-id="489d9-122">Representa el título del eje.</span><span class="sxs-lookup"><span data-stu-id="489d9-122">Represents the axis title.</span></span>|
|<span data-ttu-id="489d9-123">visible</span><span class="sxs-lookup"><span data-stu-id="489d9-123">visible</span></span>|<span data-ttu-id="489d9-124">boolean</span><span class="sxs-lookup"><span data-stu-id="489d9-124">boolean</span></span>|<span data-ttu-id="489d9-125">Valor booleano que especifica la visibilidad del título de un eje.</span><span class="sxs-lookup"><span data-stu-id="489d9-125">A boolean that specifies the visibility of an axis title.</span></span>|

## <a name="response"></a><span data-ttu-id="489d9-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="489d9-126">Response</span></span>

<span data-ttu-id="489d9-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartAxisTitle](../resources/chartaxistitle.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="489d9-127">If successful, this method returns a `200 OK` response code and updated [ChartAxisTitle](../resources/chartaxistitle.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="489d9-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="489d9-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="489d9-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="489d9-129">Request</span></span>
<span data-ttu-id="489d9-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="489d9-130">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="489d9-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="489d9-131">Response</span></span>
<span data-ttu-id="489d9-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="489d9-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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