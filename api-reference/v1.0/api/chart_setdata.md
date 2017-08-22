# <a name="chart-setdata"></a><span data-ttu-id="ceee3-101">Chart: setData</span><span class="sxs-lookup"><span data-stu-id="ceee3-101">Chart: setData</span></span>

<span data-ttu-id="ceee3-102">Restablece los datos de origen del gráfico.</span><span class="sxs-lookup"><span data-stu-id="ceee3-102">Resets the source data for the chart.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ceee3-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ceee3-103">Prerequisites</span></span>
<span data-ttu-id="ceee3-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="ceee3-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="ceee3-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ceee3-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="ceee3-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ceee3-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/setData

```
## <a name="request-headers"></a><span data-ttu-id="ceee3-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ceee3-107">Request headers</span></span>
| <span data-ttu-id="ceee3-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="ceee3-108">Name</span></span>       | <span data-ttu-id="ceee3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ceee3-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="ceee3-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="ceee3-110">Authorization</span></span>  | <span data-ttu-id="ceee3-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ceee3-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="ceee3-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ceee3-113">Request body</span></span>
<span data-ttu-id="ceee3-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="ceee3-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="ceee3-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ceee3-115">Parameter</span></span>    | <span data-ttu-id="ceee3-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="ceee3-116">Type</span></span>   |<span data-ttu-id="ceee3-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="ceee3-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ceee3-118">sourceData</span><span class="sxs-lookup"><span data-stu-id="ceee3-118">sourceData</span></span>|<span data-ttu-id="ceee3-119">string</span><span class="sxs-lookup"><span data-stu-id="ceee3-119">string</span></span>|<span data-ttu-id="ceee3-120">Objeto Range correspondiente a los datos de origen.</span><span class="sxs-lookup"><span data-stu-id="ceee3-120">The Range object corresponding to the source data.</span></span>|
|<span data-ttu-id="ceee3-121">seriesBy</span><span class="sxs-lookup"><span data-stu-id="ceee3-121">seriesBy</span></span>|<span data-ttu-id="ceee3-122">string</span><span class="sxs-lookup"><span data-stu-id="ceee3-122">string</span></span>|<span data-ttu-id="ceee3-p102">Opcional. Especifica la manera en que las columnas o las filas se usan como series de datos en el gráfico. Puede ser de una de las siguientes: Auto (valor predeterminado), Rows, Columns.  Valores posibles: `Auto`, `Columns`, `Rows`.</span><span class="sxs-lookup"><span data-stu-id="ceee3-p102">Optional. Specifies the way columns or rows are used as data series on the chart. Can be one of the following: Auto (default), Rows, Columns.  Possible values are: `Auto`, `Columns`, `Rows`.</span></span>|

## <a name="response"></a><span data-ttu-id="ceee3-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ceee3-127">Response</span></span>

<span data-ttu-id="ceee3-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ceee3-p103">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ceee3-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ceee3-130">Example</span></span>
<span data-ttu-id="ceee3-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="ceee3-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="ceee3-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ceee3-132">Request</span></span>
<span data-ttu-id="ceee3-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ceee3-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chart_setdata"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/setData
Content-type: application/json
Content-length: 70

{
  "sourceData": "sourceData-value",
  "seriesBy": "seriesBy-value"
}
```

##### <a name="response"></a><span data-ttu-id="ceee3-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ceee3-134">Response</span></span>
<span data-ttu-id="ceee3-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ceee3-135">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Chart: setData",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->