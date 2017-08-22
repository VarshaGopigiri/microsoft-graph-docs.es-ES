# <a name="chartcollection-add"></a><span data-ttu-id="059f1-101">ChartCollection: add</span><span class="sxs-lookup"><span data-stu-id="059f1-101">ChartCollection: add</span></span>

<span data-ttu-id="059f1-102">Crea un gráfico.</span><span class="sxs-lookup"><span data-stu-id="059f1-102">Creates a new chart.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="059f1-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="059f1-103">Prerequisites</span></span>
<span data-ttu-id="059f1-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="059f1-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="059f1-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="059f1-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="059f1-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="059f1-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/add

```
## <a name="request-headers"></a><span data-ttu-id="059f1-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="059f1-107">Request headers</span></span>
| <span data-ttu-id="059f1-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="059f1-108">Name</span></span>       | <span data-ttu-id="059f1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="059f1-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="059f1-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="059f1-110">Authorization</span></span>  | <span data-ttu-id="059f1-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="059f1-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="059f1-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="059f1-113">Request body</span></span>
<span data-ttu-id="059f1-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="059f1-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="059f1-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="059f1-115">Parameter</span></span>    | <span data-ttu-id="059f1-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="059f1-116">Type</span></span>   |<span data-ttu-id="059f1-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="059f1-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="059f1-118">type</span><span class="sxs-lookup"><span data-stu-id="059f1-118">type</span></span>|<span data-ttu-id="059f1-119">string</span><span class="sxs-lookup"><span data-stu-id="059f1-119">string</span></span>|<span data-ttu-id="059f1-p102">Representa el tipo de un gráfico.  Valores posibles: `ColumnClustered`, `ColumnStacked`, `ColumnStacked100`, `BarClustered`, `BarStacked`, `BarStacked100`, `LineStacked`, `LineStacked100`, `LineMarkers`, `LineMarkersStacked`, `LineMarkersStacked100`, `PieOfPie`, `etc.`.</span><span class="sxs-lookup"><span data-stu-id="059f1-p102">Represents the type of a chart.  Possible values are: `ColumnClustered`, `ColumnStacked`, `ColumnStacked100`, `BarClustered`, `BarStacked`, `BarStacked100`, `LineStacked`, `LineStacked100`, `LineMarkers`, `LineMarkersStacked`, `LineMarkersStacked100`, `PieOfPie`, `etc.`.</span></span>|
|<span data-ttu-id="059f1-122">sourceData</span><span class="sxs-lookup"><span data-stu-id="059f1-122">sourceData</span></span>|<span data-ttu-id="059f1-123">string</span><span class="sxs-lookup"><span data-stu-id="059f1-123">string</span></span>|<span data-ttu-id="059f1-124">Objeto Range correspondiente a los datos de origen.</span><span class="sxs-lookup"><span data-stu-id="059f1-124">The Range object corresponding to the source data.</span></span>|
|<span data-ttu-id="059f1-125">seriesBy</span><span class="sxs-lookup"><span data-stu-id="059f1-125">seriesBy</span></span>|<span data-ttu-id="059f1-126">string</span><span class="sxs-lookup"><span data-stu-id="059f1-126">string</span></span>|<span data-ttu-id="059f1-p103">Opcional. Especifica la manera en que las columnas o las filas se usan como series de datos en el gráfico.  Valores posibles: `Auto`, `Columns`, `Rows`.</span><span class="sxs-lookup"><span data-stu-id="059f1-p103">Optional. Specifies the way columns or rows are used as data series on the chart.  Possible values are: `Auto`, `Columns`, `Rows`.</span></span>|

## <a name="response"></a><span data-ttu-id="059f1-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="059f1-130">Response</span></span>

<span data-ttu-id="059f1-131">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Chart](../resources/chart.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="059f1-131">If successful, this method returns `200, OK` response code and [Chart](../resources/chart.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="059f1-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="059f1-132">Example</span></span>
<span data-ttu-id="059f1-133">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="059f1-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="059f1-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="059f1-134">Request</span></span>
<span data-ttu-id="059f1-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="059f1-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartcollection_add"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/add
Content-type: application/json
Content-length: 94

{
  "type": "ColumnStacked",
  "sourceData": "A1:B1",
  "seriesBy": "Auto"
}
```

##### <a name="response"></a><span data-ttu-id="059f1-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="059f1-136">Response</span></span>
<span data-ttu-id="059f1-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="059f1-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chart"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 52

{
  "id": "id-value",
  "height": 99,
  "left": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartCollection: add",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
