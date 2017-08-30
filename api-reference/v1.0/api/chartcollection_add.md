# <a name="chartcollection-add"></a><span data-ttu-id="70401-101">ChartCollection: add</span><span class="sxs-lookup"><span data-stu-id="70401-101">ChartCollection: add</span></span>

<span data-ttu-id="70401-102">Crea un nuevo gráfico.</span><span class="sxs-lookup"><span data-stu-id="70401-102">Creates a new chart.</span></span>
## <a name="permissions"></a><span data-ttu-id="70401-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="70401-103">Permissions</span></span>
<span data-ttu-id="70401-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="70401-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="70401-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="70401-106">Permission type</span></span>      | <span data-ttu-id="70401-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="70401-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="70401-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="70401-108">Delegated (work or school account)</span></span> | <span data-ttu-id="70401-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="70401-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="70401-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="70401-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="70401-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="70401-111">Not supported.</span></span>    |
|<span data-ttu-id="70401-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="70401-112">Application</span></span> | <span data-ttu-id="70401-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="70401-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="70401-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="70401-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/add

```
## <a name="request-headers"></a><span data-ttu-id="70401-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="70401-115">Request headers</span></span>
| <span data-ttu-id="70401-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="70401-116">Name</span></span>       | <span data-ttu-id="70401-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="70401-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="70401-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="70401-118">Authorization</span></span>  | <span data-ttu-id="70401-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="70401-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="70401-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="70401-121">Request body</span></span>
<span data-ttu-id="70401-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="70401-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="70401-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="70401-123">Parameter</span></span>    | <span data-ttu-id="70401-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="70401-124">Type</span></span>   |<span data-ttu-id="70401-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="70401-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="70401-126">type</span><span class="sxs-lookup"><span data-stu-id="70401-126">type</span></span>|<span data-ttu-id="70401-127">string</span><span class="sxs-lookup"><span data-stu-id="70401-127">string</span></span>|<span data-ttu-id="70401-p103">Representa el tipo de un gráfico.  Valores posibles: `ColumnClustered`, `ColumnStacked`, `ColumnStacked100`, `BarClustered`, `BarStacked`, `BarStacked100`, `LineStacked`, `LineStacked100`, `LineMarkers`, `LineMarkersStacked`, `LineMarkersStacked100`, `PieOfPie`, `etc.`.</span><span class="sxs-lookup"><span data-stu-id="70401-p103">Represents the type of a chart.  Possible values are: `ColumnClustered`, `ColumnStacked`, `ColumnStacked100`, `BarClustered`, `BarStacked`, `BarStacked100`, `LineStacked`, `LineStacked100`, `LineMarkers`, `LineMarkersStacked`, `LineMarkersStacked100`, `PieOfPie`, `etc.`.</span></span>|
|<span data-ttu-id="70401-130">sourceData</span><span class="sxs-lookup"><span data-stu-id="70401-130">sourceData</span></span>|<span data-ttu-id="70401-131">string</span><span class="sxs-lookup"><span data-stu-id="70401-131">string</span></span>|<span data-ttu-id="70401-132">Objeto Range correspondiente a los datos de origen.</span><span class="sxs-lookup"><span data-stu-id="70401-132">The Range object corresponding to the source data.</span></span>|
|<span data-ttu-id="70401-133">seriesBy</span><span class="sxs-lookup"><span data-stu-id="70401-133">seriesBy</span></span>|<span data-ttu-id="70401-134">string</span><span class="sxs-lookup"><span data-stu-id="70401-134">string</span></span>|<span data-ttu-id="70401-p104">Opcional. Especifica la manera en que las columnas o las filas se usan como series de datos en el gráfico.  Valores posibles: `Auto`, `Columns`, `Rows`.</span><span class="sxs-lookup"><span data-stu-id="70401-p104">Optional. Specifies the way columns or rows are used as data series on the chart.  Possible values are: `Auto`, `Columns`, `Rows`.</span></span>|

## <a name="response"></a><span data-ttu-id="70401-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70401-138">Response</span></span>

<span data-ttu-id="70401-139">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Chart](../resources/chart.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="70401-139">If successful, this method returns `200, OK` response code and [Chart](../resources/chart.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="70401-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="70401-140">Example</span></span>
<span data-ttu-id="70401-141">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="70401-141">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="70401-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="70401-142">Request</span></span>
<span data-ttu-id="70401-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="70401-143">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="70401-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70401-144">Response</span></span>
<span data-ttu-id="70401-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="70401-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
