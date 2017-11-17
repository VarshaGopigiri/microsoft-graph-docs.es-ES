# <a name="chartcollection-add"></a><span data-ttu-id="47a2f-101">ChartCollection: add</span><span class="sxs-lookup"><span data-stu-id="47a2f-101">ChartCollection: add</span></span>

<span data-ttu-id="47a2f-102">Crea un nuevo gráfico.</span><span class="sxs-lookup"><span data-stu-id="47a2f-102">Creates a new chart.</span></span>
## <a name="permissions"></a><span data-ttu-id="47a2f-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="47a2f-103">Permissions</span></span>
<span data-ttu-id="47a2f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="47a2f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="47a2f-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="47a2f-106">Permission type</span></span>      | <span data-ttu-id="47a2f-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="47a2f-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="47a2f-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="47a2f-108">Delegated (work or school account)</span></span> | <span data-ttu-id="47a2f-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="47a2f-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="47a2f-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="47a2f-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="47a2f-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="47a2f-111">Not supported.</span></span>    |
|<span data-ttu-id="47a2f-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="47a2f-112">Application</span></span> | <span data-ttu-id="47a2f-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="47a2f-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="47a2f-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="47a2f-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/add

```
## <a name="request-headers"></a><span data-ttu-id="47a2f-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="47a2f-115">Request headers</span></span>
| <span data-ttu-id="47a2f-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="47a2f-116">Name</span></span>       | <span data-ttu-id="47a2f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="47a2f-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="47a2f-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="47a2f-118">Authorization</span></span>  | <span data-ttu-id="47a2f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="47a2f-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="47a2f-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="47a2f-121">Request body</span></span>
<span data-ttu-id="47a2f-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="47a2f-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="47a2f-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="47a2f-123">Parameter</span></span>    | <span data-ttu-id="47a2f-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="47a2f-124">Type</span></span>   |<span data-ttu-id="47a2f-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="47a2f-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="47a2f-126">type</span><span class="sxs-lookup"><span data-stu-id="47a2f-126">type</span></span>|<span data-ttu-id="47a2f-127">string</span><span class="sxs-lookup"><span data-stu-id="47a2f-127">string</span></span>|<span data-ttu-id="47a2f-p103">Representa el tipo de un gráfico.  Valores posibles: `ColumnClustered`, `ColumnStacked`, `ColumnStacked100`, `BarClustered`, `BarStacked`, `BarStacked100`, `LineStacked`, `LineStacked100`, `LineMarkers`, `LineMarkersStacked`, `LineMarkersStacked100`, `PieOfPie`, `etc.`.</span><span class="sxs-lookup"><span data-stu-id="47a2f-p103">Represents the type of a chart.  Possible values are: `ColumnClustered`, `ColumnStacked`, `ColumnStacked100`, `BarClustered`, `BarStacked`, `BarStacked100`, `LineStacked`, `LineStacked100`, `LineMarkers`, `LineMarkersStacked`, `LineMarkersStacked100`, `PieOfPie`, `etc.`.</span></span>|
|<span data-ttu-id="47a2f-130">sourceData</span><span class="sxs-lookup"><span data-stu-id="47a2f-130">sourceData</span></span>|<span data-ttu-id="47a2f-131">string</span><span class="sxs-lookup"><span data-stu-id="47a2f-131">string</span></span>|<span data-ttu-id="47a2f-132">Objeto Range correspondiente a los datos de origen.</span><span class="sxs-lookup"><span data-stu-id="47a2f-132">The Range object corresponding to the source data.</span></span>|
|<span data-ttu-id="47a2f-133">seriesBy</span><span class="sxs-lookup"><span data-stu-id="47a2f-133">seriesBy</span></span>|<span data-ttu-id="47a2f-134">string</span><span class="sxs-lookup"><span data-stu-id="47a2f-134">string</span></span>|<span data-ttu-id="47a2f-p104">Opcional. Especifica la manera en que las columnas o las filas se usan como series de datos en el gráfico.  Valores posibles: `Auto`, `Columns`, `Rows`.</span><span class="sxs-lookup"><span data-stu-id="47a2f-p104">Optional. Specifies the way columns or rows are used as data series on the chart.  Possible values are: `Auto`, `Columns`, `Rows`.</span></span>|

## <a name="response"></a><span data-ttu-id="47a2f-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="47a2f-138">Response</span></span>

<span data-ttu-id="47a2f-139">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Chart](../resources/chart.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="47a2f-139">If successful, this method returns `200 OK` response code and [Chart](../resources/chart.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="47a2f-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="47a2f-140">Example</span></span>
<span data-ttu-id="47a2f-141">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="47a2f-141">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="47a2f-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="47a2f-142">Request</span></span>
<span data-ttu-id="47a2f-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="47a2f-143">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="47a2f-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="47a2f-144">Response</span></span>
<span data-ttu-id="47a2f-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="47a2f-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
