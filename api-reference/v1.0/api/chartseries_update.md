# <a name="update-chartseries"></a><span data-ttu-id="9c5ae-101">Actualizar chartseries</span><span class="sxs-lookup"><span data-stu-id="9c5ae-101">Update chartseries</span></span>

<span data-ttu-id="9c5ae-102">Actualiza las propiedades del objeto chartserie.</span><span class="sxs-lookup"><span data-stu-id="9c5ae-102">Update the properties of chartseries object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9c5ae-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9c5ae-103">Prerequisites</span></span>
<span data-ttu-id="9c5ae-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="9c5ae-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="9c5ae-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9c5ae-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="9c5ae-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9c5ae-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/series(<undefined>)
```
## <a name="optional-request-headers"></a><span data-ttu-id="9c5ae-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="9c5ae-107">Optional request headers</span></span>
| <span data-ttu-id="9c5ae-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="9c5ae-108">Name</span></span>       | <span data-ttu-id="9c5ae-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c5ae-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="9c5ae-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="9c5ae-110">Authorization</span></span>  | <span data-ttu-id="9c5ae-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9c5ae-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="9c5ae-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9c5ae-113">Request body</span></span>
<span data-ttu-id="9c5ae-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="9c5ae-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="9c5ae-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9c5ae-117">Property</span></span>     | <span data-ttu-id="9c5ae-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c5ae-118">Type</span></span>   |<span data-ttu-id="9c5ae-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c5ae-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9c5ae-120">name</span><span class="sxs-lookup"><span data-stu-id="9c5ae-120">name</span></span>|<span data-ttu-id="9c5ae-121">string</span><span class="sxs-lookup"><span data-stu-id="9c5ae-121">string</span></span>|<span data-ttu-id="9c5ae-122">Representa el nombre de una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="9c5ae-122">Represents the name of a series in a chart.</span></span>|

## <a name="response"></a><span data-ttu-id="9c5ae-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9c5ae-123">Response</span></span>

<span data-ttu-id="9c5ae-124">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartSeries](../resources/chartseries.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9c5ae-124">If successful, this method returns a `200 OK` response code and updated [ChartSeries](../resources/chartseries.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="9c5ae-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9c5ae-125">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9c5ae-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9c5ae-126">Request</span></span>
<span data-ttu-id="9c5ae-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9c5ae-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartseries"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/series(<undefined>)
Content-type: application/json
Content-length: 26

{
  "name": "name-value"
}
```
##### <a name="response"></a><span data-ttu-id="9c5ae-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9c5ae-128">Response</span></span>
<span data-ttu-id="9c5ae-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9c5ae-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartSeries"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 26

{
  "name": "name-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chartseries",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->